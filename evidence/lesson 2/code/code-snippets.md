# Lesson 02 Code Snippets

Core JWT verification flow in `DVSA-ORDER-MANAGER/order-manager.js`:

```js
var auth_header = (headers.Authorization || headers.authorization || "");
var jwt = auth_header.replace(/^Bearer\s+/i, "").trim();

if (!jwt) {
  return callback(null, resp(401, { status: "err", msg: "missing authorization" }));
}

verifyCognitoJwt(jwt).then((claims) => {
  var user = claims.username || claims["cognito:username"] || claims.sub;
  if (!user) {
    return callback(null, resp(401, { status: "err", msg: "missing subject" }));
  }
```

Compatibility fix for `get_order.py`:

```python
is_admin = str(event.get("isAdmin", "false")).strip().lower() == "true"
```

Screenshot: `get-order-runtime-compat-fix.png`

# Lesson 09 Code Snippets

Vulnerable dependency usage:

```js
const serialize = require("node-serialize");
var req = serialize.unserialize(event.body);
var headers = serialize.unserialize(event.headers);
```

Fixed parsing:

```js
var req = typeof event.body === "string" ? JSON.parse(event.body) : (event.body || {});
var headers = event.headers || {};
```

Screenshot: `order-manager-json-parse-fix.png`

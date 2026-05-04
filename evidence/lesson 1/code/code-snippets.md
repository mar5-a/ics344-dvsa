# Lesson 01 Code Snippets

Vulnerable parsing:

```js
var req = serialize.unserialize(event.body);
var headers = serialize.unserialize(event.headers);
```

Fixed parsing:

```js
var req = typeof event.body === "string" ? JSON.parse(event.body) : (event.body || {});
var headers = event.headers || {};
```

Screenshot: `order-manager-json-parse-fix.png`

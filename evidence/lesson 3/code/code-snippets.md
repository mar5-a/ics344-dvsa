# Lesson 03 Code Snippets

Practical fix used in this deployment:

```js
var req = typeof event.body === "string" ? JSON.parse(event.body) : (event.body || {});
var headers = event.headers || {};
```

This blocks the demonstrated path to `DVSA-ADMIN-GET-RECEIPT`.

Defense-in-depth note: `DVSA-ADMIN-GET-RECEIPT` should also enforce explicit admin authorization before generating signed URLs.

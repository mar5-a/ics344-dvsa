# Lesson 10 Code Snippets

Fix pattern in `order-manager.js`:

```js
lambda_client.send(command).then((lambda_response) => {
  if (lambda_response.FunctionError) {
    return callback(null, resp(500, { status: "err", msg: "internal error" }));
  }

  let data;
  try {
    data = JSON.parse(Buffer.from(lambda_response.Payload).toString());
  } catch (e) {
    return callback(null, resp(500, { status: "err", msg: "internal error" }));
  }

  return callback(null, {
    statusCode: 200,
    headers: { "Access-Control-Allow-Origin": "*" },
    body: JSON.stringify(data)
  });
}).catch((e) => {
  console.log("Lambda invoke failed:", e);
  return callback(null, resp(500, { status: "err", msg: "internal error" }));
});
```

Screenshot:

- `order-manager-function-error-mask-fix.png`

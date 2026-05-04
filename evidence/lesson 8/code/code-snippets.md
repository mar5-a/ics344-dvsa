# Lesson 08 Code Snippets

Vulnerable state check:

```python
if response["Item"]["orderStatus"] >= 200:
```

Fixed state check:

```python
if response["Item"]["orderStatus"] != 100:
```

Conditional update protection:

```python
response = table.update_item(
   Key={"orderId": orderId, "userId": userId},
   UpdateExpression="SET address = :address",
   ConditionExpression="orderStatus = :open",
   ExpressionAttributeValues={
       ":address": address,
       ":open": 100
   }
)
```

Screenshots:

- `status-validation-fix.png`
- `status-list-reference.png`
- `reject-late-update-fix.png`
- `conditional-update-fix.png`

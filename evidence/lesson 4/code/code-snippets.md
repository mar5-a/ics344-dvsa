# Lesson 04 Code Snippets

Expected receipt object format:

```text
YYYY/MM/DD/orderId_userId.raw
```

Validation added in `send_receipt_email.py`:

```python
parts = key.split("/")
if len(parts) != 4:
    print("Invalid receipt key format:", key)
    return {"status": "err", "msg": "invalid receipt key"}

order = parts[3]
if not order.endswith(".raw") or "_" not in order:
    print("Invalid receipt filename:", order)
    return {"status": "err", "msg": "invalid receipt filename"}

orderId, userId = order.replace(".raw", "").split("_", 1)
if not orderId or not userId:
    print("Invalid receipt identifiers:", order)
    return {"status": "err", "msg": "invalid receipt identifiers"}
```

Screenshots:

- `send-receipt-key-validation-fix.png`
- `send-receipt-key-validation-fix-detail.png`

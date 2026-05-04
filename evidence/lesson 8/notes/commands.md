# Lesson 08 Commands

Requests captured and replayed through Burp Repeater.

Billing request shape:

```json
{"action":"billing","order-id":"<ORDER_ID>"}
```

Immediate update request shape:

```json
{"action":"update","order-id":"<ORDER_ID>","items":{"1012":5}}
```

Expected vulnerable response:

```json
{"status":"ok","msg":"cart updated"}
```

Expected post-fix response:

```json
{"status":"err","msg":"too late to update order"}
```

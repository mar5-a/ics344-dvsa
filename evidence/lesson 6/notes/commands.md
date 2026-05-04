# Lesson 06 Commands

Direct Lambda flood pattern:

```bash
seq 1 40 | xargs -n1 -P40 -I{} aws lambda invoke \
  --function-name DVSA-ORDER-BILLING \
  --payload file://dvsa-billing-payload.json \
  --cli-binary-format raw-in-base64-out \
  "out-{}.json"
```

Temporary API Gateway throttle proof:

```bash
aws apigateway update-stage \
  --rest-api-id 2w2y6rr71e \
  --stage-name dvsa \
  --patch-operations \
    op=replace,path='/*/*/throttling/rateLimit',value='1' \
    op=replace,path='/*/*/throttling/burstLimit',value='2'
```

Restore:

```bash
aws apigateway update-stage \
  --rest-api-id 2w2y6rr71e \
  --stage-name dvsa \
  --patch-operations \
    op=replace,path='/*/*/throttling/rateLimit',value='10' \
    op=replace,path='/*/*/throttling/burstLimit',value='20'
```

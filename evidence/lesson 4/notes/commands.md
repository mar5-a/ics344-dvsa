# Lesson 04 Commands

```bash
export RECEIPTS_BUCKET="dvsa-receipts-bucket-992382806779-us-east-1"
touch ~/empty

aws s3 cp ~/empty "s3://$RECEIPTS_BUCKET/2026/05/04/l4-test.raw" --region us-east-1

aws s3 cp ~/empty "s3://$RECEIPTS_BUCKET/2026/05/04/null_;echo L4_PROOF >&2;echo x.raw" --region us-east-1

aws logs tail /aws/lambda/DVSA-SEND-RECEIPT-EMAIL --since 15m --region us-east-1

aws s3 ls "s3://$RECEIPTS_BUCKET/2026/05/04/" --region us-east-1
```

Post-fix verification with an external/test profile:

```bash
aws s3 cp ~/empty "s3://$RECEIPTS_BUCKET/2026/05/04/l4-after-fix.raw" --region us-east-1 --profile TEST_PROFILE
```

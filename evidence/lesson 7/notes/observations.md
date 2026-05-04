# Lesson 07 Observations

- `DVSA-SEND-RECEIPT-EMAIL` had broad IAM permissions beyond its receipt email task.
- Policy evidence included broad SES, S3, and DynamoDB permissions.
- IAM Policy Simulator showed unnecessary S3 and DynamoDB actions as allowed.
- CloudWatch/CloudTrail showed actual use was much narrower than attached policy scope.
- Fix is to replace broad policies with least-privilege resource-specific permissions.

Screenshots:

- `../screenshots/01-receipt-function-role.png`
- `../screenshots/02-attached-broad-policies.png`
- `../screenshots/03-policy-details.png`
- `../screenshots/04-policy-simulator-dynamodb-allowed.png`
- `../screenshots/05-policy-simulator-s3-allowed.png`
- `../screenshots/06-cloudtrail-actual-usage.png`

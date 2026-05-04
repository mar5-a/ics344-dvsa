# Lesson 07 Commands

Manual console flow used for this lesson:

1. Open `Lambda -> Functions -> DVSA-SEND-RECEIPT-EMAIL`.
2. Open `Configuration -> Permissions`.
3. Open the execution role.
4. Review attached policies.
5. Open `IAM -> Policy Simulator`.
6. Select identity type `Roles`.
7. Select the receipt function role.
8. Test DynamoDB actions: `GetItem`, `PutItem`, `Scan`, `DeleteItem`.
9. Test S3 actions: `GetObject`, `PutObject`.
10. Trigger the function by completing an order.
11. Review CloudWatch Logs and CloudTrail event history.

Evidence sources:

```text
IAM role policies
IAM Policy Simulator
CloudWatch Logs
CloudTrail Event History
```

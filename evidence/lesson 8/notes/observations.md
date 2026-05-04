# Lesson 08 Observations

- DVSA allowed an order update after billing had already been processed.
- The root issue was improper order state validation and non-atomic update logic.
- Status `120` meant paid, but the vulnerable code only blocked `orderStatus >= 200`.
- Fix enforced `orderStatus == 100` for updates and added DynamoDB conditional updates.
- Post-fix update after billing returned `too late to update order`.

Screenshots:

- `../screenshots/01-billing-request.png`
- `../screenshots/02-update-after-billing-response.png`
- `../screenshots/03-order-confirmation-receipt.png`
- `../screenshots/04-dynamodb-order-evidence.png`
- `../screenshots/05-post-fix-rejected.png`

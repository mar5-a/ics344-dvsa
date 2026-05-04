# Lesson 05 Observations

- A regular user could invoke `DVSA-ADMIN-UPDATE-ORDERS`.
- The admin update changed order state without completing the billing path.
- CloudWatch confirmed the admin function executed.
- Post-fix behavior rejected the same non-admin request.

Screenshots:

- `../screenshots/01-order-created-before-exploit.png`
- `../screenshots/02-admin-update-invoke-command.png`
- `../screenshots/03-admin-update-invoke-success.png`
- `../screenshots/04-order-updated-after-exploit.png`
- `../screenshots/05-cloudwatch-admin-update-logs.png`
- `../screenshots/06-post-fix-rejected.png`

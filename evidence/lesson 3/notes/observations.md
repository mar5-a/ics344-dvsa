# Lesson 03 Observations

- Injected code invoked `DVSA-ADMIN-GET-RECEIPT`.
- The admin function generated a signed S3 receipt download URL.
- The URL exposed receipt data outside the intended authorization boundary.
- Removing the Lesson 1 injection path blocked this demonstrated leak path.

Screenshots:

- `../screenshots/01-receipt-leak-command.png`
- `../screenshots/02-cloudwatch-receipt-leak.png`
- `../screenshots/03-leaked-receipt-file.png`

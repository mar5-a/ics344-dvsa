# Lesson 04 Observations

- Uploading `l4-test.raw` to the receipts bucket succeeded.
- The uploaded `.raw` object triggered `DVSA-SEND-RECEIPT-EMAIL`.
- CloudWatch showed `IndexError: list index out of range` at `userId = order.split("_")[1].replace(".raw", "")`, proving the Lambda processed the manually uploaded object key.
- S3 listing showed the uploaded `.raw` object and generated `.txt` output for the crafted key.
- Fix evidence includes blocked public access and object key validation.

Screenshots:

- `../screenshots/01-s3-upload-success.png`
- `../screenshots/02-cloudwatch-lambda-trigger-error.png`
- `../screenshots/03-s3-object-listing-and-txt-output.png`
- `../screenshots/04-block-public-access-fix.png`
- `../screenshots/05-post-fix-access-denied.png`

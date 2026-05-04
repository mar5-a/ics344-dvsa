# Lesson 07 Code Snippets

Vulnerable policy pattern:

```json
{
  "Effect": "Allow",
  "Action": "dynamodb:*",
  "Resource": "*"
}
```

Least-privilege example:

```json
{
  "Effect": "Allow",
  "Action": ["dynamodb:GetItem"],
  "Resource": "arn:aws:dynamodb:us-east-1:ACCOUNT:table/DVSA-ORDERS-DB"
}
```

Other reductions:

```json
{
  "Action": ["s3:GetObject"],
  "Resource": "arn:aws:s3:::dvsa-receipts-bucket/*"
}
```

```json
{
  "Action": ["ses:SendEmail"],
  "Resource": "*"
}
```

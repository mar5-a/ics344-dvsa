# Lesson 01 Observations

- Client response showed an error, but the backend still executed the injected payload.
- CloudWatch showed `FILE READ SUCCESS: You are reading the contents of my hacked file!`.
- After replacing unsafe deserialization with `JSON.parse`, the same payload no longer produced the injected log line.

Screenshots:

- `../screenshots/01-exploit-request-generic-error.png`
- `../screenshots/02-cloudwatch-file-read-success.png`
- `../screenshots/03-post-fix-cloudwatch-no-injected-log.png`

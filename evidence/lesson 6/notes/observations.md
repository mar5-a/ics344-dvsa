# Lesson 06 Observations

- Parallel Lambda invokes produced `TooManyRequestsException` and `ConcurrentInvocationLimitExceeded`.
- Account concurrency was limited to `ConcurrentExecutions: 10`.
- Parallel HTTP billing traffic produced mixed `200`, `500`, and `502` responses.
- After temporary API Gateway throttling, the test produced `429`, proving edge throttling.

Screenshots:

- `../screenshots/01-environment-and-token-setup.png`
- `../screenshots/02-lambda-flood-command-output.png`
- `../screenshots/03-concurrent-invocation-limit-errors.png`
- `../screenshots/04-api-gateway-throttle-verification.png`

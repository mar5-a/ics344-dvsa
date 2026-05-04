# Lesson 10 Observations

- Malformed authenticated requests returned raw Lambda error objects.
- Responses exposed `errorType`, `errorMessage`, stack traces, file paths, and line numbers.
- Affected downstream functions included `get_order.py` and `order_complete.py`.
- Fix belongs in `DVSA-ORDER-MANAGER`, where child Lambda `FunctionError` payloads are masked before returning to the client.
- Post-fix response returned generic `internal error` without stack trace details.

Screenshots:

- `../screenshots/01-get-missing-order-id-stack-trace.png`
- `../screenshots/02-complete-missing-order-id-stack-trace.png`
- `../screenshots/03-post-fix-internal-error.png`

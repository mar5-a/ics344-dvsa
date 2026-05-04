# Lesson 09 Observations

- Vulnerable dependency: `node-serialize`.
- `serialize.unserialize()` accepted attacker-controlled serialized function payloads.
- CloudWatch confirmed backend code execution.
- The dependency usage was removed from the request path and replaced with `JSON.parse`.

Screenshots:

- `../screenshots/01-exploit-request-generic-error.png`
- `../screenshots/02-cloudwatch-file-read-success.png`

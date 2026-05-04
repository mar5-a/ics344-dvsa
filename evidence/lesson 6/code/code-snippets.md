# Lesson 06 Code Snippets

No application code change was required for the demonstrated mitigation.

Configuration changed:

```text
API Gateway stage: dvsa
Method settings: */*
Temporary proof throttle: rate 1, burst 2
Restored tested throttle: rate 10, burst 20
```

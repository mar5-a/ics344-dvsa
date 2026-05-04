# Lesson 05 Code Snippets

Minimal authorization fix in `DVSA-ADMIN-UPDATE-ORDERS`:

```python
is_admin = event.get("isAdmin", False)
if str(is_admin).lower() != "true":
    return {"status": "err", "msg": "forbidden"}
```

Screenshots:

- `admin-update-exploit-payload.png`
- `admin-update-is-admin-fix.png`

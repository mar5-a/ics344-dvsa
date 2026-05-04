# Lesson 02 Observations

- User B identity: `2428d4f8-20a1-709e-3bd4-872c632a9fd0`.
- User C identity: `b46884b8-e021-7062-41f7-8c470a17a758`.
- Forged token returned User C order data, including order id `88d36144-dea7-4043-91fd-3c6e374a491c`.
- After JWT verification was added, the forged token returned `{ "status": "err", "msg": "invalid token" }`.
- A fresh valid User B token still worked after the fix.

Screenshots:

- `../screenshots/01-baseline-token-b-orders.png`
- `../screenshots/02-forged-token-victim-order-list.png`
- `../screenshots/03-victim-order-details.png`
- `../screenshots/04-post-fix-forged-token-rejected.png`
- `../screenshots/05-post-fix-token-b-still-works.png`

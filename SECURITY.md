# Security Guidelines

- Never commit secrets, tokens, passwords or production connection strings.
- Use environment variables and a secret manager.
- Require TLS for all network communication.
- Validate authentication and authorization server-side.
- Apply least privilege to database/cloud roles.
- Keep private social data private by default.
- Do not log sensitive fitness/health data unless operationally necessary and protected.
- Use encryption at rest for persistent stores and backups where supported.

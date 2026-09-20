# FitFlow Technology Stack Summary

## Recommendation

| Area | Technology | Why |
|---|---|---|
| Frontend | Flutter | Shared iOS/Android/web UI with strong code reuse and good performance. |
| Main backend | NestJS | Structured TypeScript services, REST, WebSocket and microservice support. |
| AI service | FastAPI | Python AI/ML ecosystem and fast inference API development. |
| Database | PostgreSQL | Strong transactions, relationships, analytics and JSONB flexibility. |
| Cache | Redis | Low-latency cache, rate limits and pub/sub. |
| Authentication | Amazon Cognito | OAuth/OIDC, MFA, managed scale and AWS integration. |
| Media | S3/object storage | Efficient storage for meal photos and exercise media. |

The architecture intentionally uses NestJS and FastAPI together: NestJS owns FitFlow business rules and real-time product behavior, while FastAPI owns AI inference.

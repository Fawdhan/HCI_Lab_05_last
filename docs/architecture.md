# FitFlow High-Level Architecture

The client layer uses Flutter for mobile and web. Amazon Cognito handles authentication. Requests enter through an HTTPS API/load-balancing layer and are routed to the NestJS application backend or real-time gateway. NestJS owns user profiles, workouts, progress, nutrition, community, privacy and notification logic. FastAPI is isolated as the AI microservice for personalized workout generation and meal/nutrition inference.

PostgreSQL is the authoritative data store. Redis provides caching, rate limiting and pub/sub. Object storage holds meal images and exercise media. A queue/worker layer supports slow background work.

## Critical Flows

### Personalized workout
Flutter -> Cognito -> NestJS -> PostgreSQL + FastAPI -> NestJS -> Flutter.
The AI response includes explanation metadata so the UI can support “Why this workout?”, Edit and Generate New Plan.

### Community challenge
Flutter -> NestJS -> PostgreSQL/Redis -> WebSocket gateway -> eligible clients.
Visibility rules are enforced server-side for Private/Friends/Public sharing.

### Nutrition tracking
Flutter camera -> object storage -> NestJS -> FastAPI -> user confirmation -> PostgreSQL -> updated dashboard.

# FitFlow Redesign

FitFlow is a user-centered fitness application redesign created for IT3060 - Human Computer Interaction. The redesign continues the work from Labs 01-04 and supports personalized AI workouts, fast workout logging, progress feedback, camera-first nutrition tracking, community challenges, privacy controls, and clear user control over AI recommendations.

## Selected Technology Stack

- Frontend: Flutter (Dart) for iOS, Android and web
- Main backend: Node.js + NestJS (TypeScript)
- AI service: Python + FastAPI
- Primary database: PostgreSQL
- Cache / real-time coordination: Redis
- Authentication: Amazon Cognito
- Media storage: Object storage such as Amazon S3
- Real-time layer: NestJS WebSocket Gateway + Redis pub/sub
- Async processing: Queue + worker services

## Architecture

See `docs/architecture.png` and `docs/architecture.md`.

## Repository Structure

- `frontend/` - Flutter application workspace
- `backend/` - NestJS application backend
- `ai-service/` - FastAPI AI inference service
- `docs/` - architecture, comparison matrix, technology summary and ADRs
- `.github/workflows/` - CI workflow placeholder

## Core FitFlow Flows

1. Personalized workout generation with goal, level, time and equipment preferences.
2. AI recommendation explanation, edit and regenerate controls.
3. Active workout logging with immediate completion feedback.
4. Progress dashboards with charts, goals, streaks and achievements.
5. Community challenges with private/friends/public visibility controls.
6. Camera-first meal logging with barcode/manual alternatives and user confirmation.

## Security Note

FitFlow is designed around TLS, managed identity, server-side authorization, least privilege, encrypted storage, privacy-by-default sharing, audit logging and data minimization. HIPAA/GDPR compliance is not automatic and depends on the deployed services, contracts, policies and configuration.

## First Commit / Push

```bash
git init
git add .
git commit -m "Initial FitFlow redesign architecture and technology decisions"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/fitflow-redesign.git
git push -u origin main
```

After pushing, add the final repository URL to the Lab Exercise 05 report.

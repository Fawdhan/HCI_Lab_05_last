# ADR-001: FitFlow Cross-Platform and Service Architecture

- Status: Accepted for Lab Exercise 05 proposal
- Date: 2026-09-20

## Context
FitFlow requires iOS/Android/web delivery, responsive workout interactions, AI personalization, nutrition image processing, social real-time features, secure health/fitness data handling and maintainability for a mid-sized team.

## Decision
Use Flutter for clients; NestJS for the main backend and WebSocket layer; FastAPI for AI inference; PostgreSQL as the system of record; Redis for cache/pub-sub; Amazon Cognito for identity; object storage for media; and asynchronous queue/worker support for slow tasks.

## Rationale
The hybrid stack keeps one cross-platform UI, separates business logic from AI workloads, provides strong relational/transactional data handling and allows real-time and AI workloads to scale independently.

## Consequences
Positive: high code reuse, modular scaling, strong AI integration and clearer security boundaries.
Trade-offs: multiple runtimes (Dart/TypeScript/Python), more deployment components and a need for service monitoring.

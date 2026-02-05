# Presentation Outline

1. Problem & Goals
2. Solution Overview (JA/UZ bilingual, project/task/calendar)
3. Architecture (Django + DRF + React + Celery)
   - Flexible Backend: Supports both PostgreSQL (Prod) and SQLite (Dev)
   - Async Tasks: Celery with Redis (or Eager mode for local dev without Redis)
4. Data Model Highlights
5. API Demo (projects, tasks, calendar, notifications)
6. UI Demo (projects, tasks, calendar, settings)
7. Translation Workflow (offline fallback)
8. Background Scheduler (notifications)
9. Tests & QA
10. Deployment & Infrastructure
    - Docker-less development support
    - Git & GitHub Integration
    - Ready for Render/Vercel deployment
11. Next Steps

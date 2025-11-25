# hiring-fullstack-todo

A compact full‑stack TODO application used for hiring assessment. Includes a backend API, frontend client, and example database/migrations. This README describes project layout, how to run locally, and common scripts.

## Features
- CRUD tasks (create, read, update, delete)
- Basic input validation and error handling
- Tests for API and/or UI

## Tech stack (example)
- Backend: Node.js, Express 
- Frontend: React (Vite)
- Database:  MongoDB
- Tooling: npm or yarn, Jest/Testing Library, Docker (optional)

## Repository layout
- backend/ — API server, routes, controllers, models
- frontend/ — SPA, components, services
- .env.example — example environment variables
- README.md — this file


## Prerequisites
- Node.js >= 14
- npm or yarn
- Database engine if not using an embedded DB

## Quick start (local)

1. Clone
  ```
  git clone <repo-url>
  cd hiring-fullstack-todo
  ```

2. Backend
  ```
  cd backend
  cp .env.example .env        # edit .env as needed
  npm install                 # or yarn
  npm run migrate             # run migrations (if applicable)
  npm run seed                # seed DB (optional)
  npm run dev                 # starts backend in dev mode
  ```
  Common scripts: start, dev, migrate, seed, test

3. Frontend
  ```
  cd frontend
  cp .env.example .env        # update API_URL if needed
  npm install                 # or yarn
  npm run dev                 # starts local dev server
  ```
  Common scripts: start/dev, build, test

4. Open the app
  - Frontend: http://localhost:3000 (or configured port)
  - Backend: API endpoints at http://localhost:4000 (or configured port)

## Environment variables (.env.example)
```
# Backend
PORT=4000
DATABASE_URL=postgres://user:pass@localhost:5432/todo_db
JWT_SECRET=change_me

# Frontend
VITE_API_URL=http://localhost:4000
```
Rename/copy `.env.example` to `.env` and update values.

## Testing
- Backend unit/integration:
  ```
  cd backend
  npm test
  ```
- Frontend:
  ```
  cd frontend
  npm test
  ```

## Docker (optional)
Provide a docker-compose.yml to run backend, frontend, and DB. Typical commands:
```
docker-compose up --build
```

## API docs
Include endpoint list in backend/README.md:
- POST /auth/login
- POST /auth/register
- GET /tasks
- POST /tasks
- GET /tasks/:id
- PUT /tasks/:id
- DELETE /tasks/:id

## Deployment
1. Build frontend: `cd frontend && npm run build`
2. Serve static build from backend or deploy separately (Netlify, Vercel, S3+CloudFront)
3. Ensure env vars and DB are configured in production

## Contributing
- Create feature branches from main
- Follow existing code style and lint rules

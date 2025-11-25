# backend — API server

Simple Node.js API server for the full‑stack TODO app. This document covers setup, structure, environment, and common commands for the server package.

## Features
- REST endpoints for TODOs (CRUD)
- Input validation and basic error handling
- Database access via an ORM/Query layer

## Recommended stack
- Node.js (>=16)
- Framework: Express
- DB: MongoDB, Mongoose as ORM
- Lint: ESLint + Prettier

## Repo layout (backend)
- backend/
    - src/
        - index.ts (start server)
        - app.ts (Express app)
        - routes/
        - controllers/
        - services/
        - models/        # for Mongoose (MongoDB)
        # If using a SQL database, you may use Prisma as ORM instead of Mongoose
        - middleware/ (auth, error handler, validation)
        - tests/
    - .env.example
    - package.json
   
## Prerequisites
- Node.js >= 16
- npm or yarn
- (optional) Docker for containerized DB

## Environment (.env)
PORT=3000
MONGO_URI 
```

## Quick start (local)
1. Install dependencies
```bash
cd backend
npm install
# or
yarn
```
2. Run in development
```bash
npm run dev
# or
yarn dev
```
4. Run tests
```bash
npm test
```

## Typical scripts (package.json)
- dev — start server in development with hot reload (nodemon / ts-node-dev)
- start — run built production server (node index.js)
- build — compile TypeScript to JavaScript
- seed — seed initial data
- test — run unit/integration tests
- lint — run ESLint
Example:
```json
"scripts": {
    "dev": "ts-node-dev --respawn src/index.ts",
    "build": "tsc",
    "start": "node dist/index.js",
    "seed": "ts-node src/seed.ts",
    "test": "jest --runInBand",
    "lint": "eslint . --ext .ts"
}
```

## API basics
- Base: GET/POST/PUT/DELETE /api/todos

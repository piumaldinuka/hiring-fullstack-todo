# Client — Hiring Fullstack Todo

A minimal README for the client app of the "hiring-fullstack-todo" project. Adjust specifics (framework, scripts, env names) to match the actual code.

## Project
Single-page client application for the TODO app used in the hiring exercise. Responsible for user interface, communicating with the server API, and local client-side validation/state.

## Tech stack (example)
- Framework: React  
- Bundler: Vite or Create React App  
- Language: TypeScript  
- Styling: CSS / Tailwind / styled-components  
- Linting: ESLint, Prettier

## Requirements
- Node.js >= 16
- npm / yarn / pnpm
- Backend API running (see repo root for server README)

## Setup

Clone repo and open client folder:
```bash
cd /path/to/hiring-fullstack-todo/client
npm install
# or
yarn
# or
pnpm install
```

## Environment variables
Create a .env file (copy .env.example if present). Typical variables:
```
VITE_API_URL=http://localhost:4000/api
# or for CRA:
REACT_APP_API_URL=http://localhost:4000/api
```
Adjust names to match the actual code.

## Common scripts
(Replace with actual scripts in package.json)
```bash
# dev server with hot reload
npm run dev
# or
npm start

# build production bundle
npm run build

# preview production build (if available)
npm run preview

# run tests
npm test

# lint and format
npm run lint
npm run format
```

## Development workflow
1. Start backend API.
2. Set API URL in .env.
3. Run the dev script.
4. Open browser at http://localhost:3000 (or port printed in console).

## Features (example)
- List, create, edit, delete TODO items
- Mark items complete/incomplete
- Client-side form validation
- Pagination / filtering / search (if implemented)
- Real-time updates via WebSocket (if implemented)

## API contract (summary)
Client expects the backend to expose endpoints such as:
- GET /todos — list todos
- POST /todos — create todo
- GET /todos/:id — get single todo
- PUT /todos/:id — update todo
- DELETE /todos/:id — delete todo

Adjust paths and request/response shapes to match server implementation.

## Troubleshooting
- CORS errors: ensure server allows client origin or proxy is configured.
- 401/403: check auth tokens and env variables.
- Port conflicts: change PORT or use the displayed dev server port.

## Contributing
- Follow linting and formatting rules.
- Add tests for new behavior.
- Document new env vars and scripts.

## License
Specify project license in repo root (e.g., MIT). Update this file accordingly.

---
Tailor the above to match actual package.json, framework, and environment variable names present in the client code.
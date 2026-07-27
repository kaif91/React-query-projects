# Lazy Days Spa

A full-stack demo application for a fictional spa booking site. Users can browse staff & treatments, sign in, view/schedule/cancel appointments, and manage their profile — all backed by a real Express API and modeled with **TanStack (React) Query**.

This is a monorepo with three parts:

- **`client/`** – the React single-page app (Vite + TypeScript + Chakra UI + React Query)
- **`server/`** – the Express + TypeScript API and JSON "database" that the client talks to
- **`shared/`** – TypeScript types shared between client and server

See each subfolder's own README for detailed setup instructions:

- [`client/README.md`](./client/README.md)
- [`server/README.md`](./server/README.md)

## What it does

- Displays spa **staff** and **treatments**, filterable by treatment/staff member.
- Lets a user **sign in / sign out** (JWT-based auth) and view/manage **their own appointments**.
- Supports **scheduling and cancelling** appointments, with optimistic UI updates via React Query mutations.
- Uses **Mock Service Worker (msw)** in the client for some flows/tests, alongside a real Express server for others.
- Demonstrates advanced React Query patterns: query keys/factories, prefetching, pagination, background refetching, optimistic updates, and dependent queries.

## Technologies used

**Client**
- [React 18](https://react.dev/) + [TypeScript](https://www.typescriptlang.org/)
- [Vite](https://vitejs.dev/)
- [TanStack React Query v5](https://tanstack.com/query/latest) + [React Query Devtools](https://tanstack.com/query/latest/docs/framework/react/devtools)
- [Chakra UI](https://v2.chakra-ui.com/) – component library/styling
- [React Router v6](https://reactrouter.com/)
- [Axios](https://axios-http.com/) – HTTP client
- [Formik](https://formik.org/) – forms
- [Day.js](https://day.js.org/) – date handling
- [fast-json-patch](https://www.npmjs.com/package/fast-json-patch) – JSON patch diffs for updates
- [MSW (Mock Service Worker)](https://mswjs.io/) – API mocking
- [Vitest](https://vitest.dev/) + [Testing Library](https://testing-library.com/) – testing

**Server**
- [Node.js](https://nodejs.org/) + [Express](https://expressjs.com/) + [TypeScript](https://www.typescriptlang.org/)
- [express-jwt](https://www.npmjs.com/package/express-jwt) / [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken) – authentication
- [Babel](https://babeljs.io/) – TS/JS transpilation for running the server
- JSON file–based storage (see `server/db`)

## Setup

Install and run each part separately (in two terminals):

```bash
# Terminal 1 - API server
cd server
npm install
cp .env_template .env
npm start          # http://localhost:3030

# Terminal 2 - client app
cd client
npm install
npm run dev         # http://localhost:5173 (default Vite port)
```

The client is configured to talk to the server, so start the server first. See the individual `client/README.md` and `server/README.md` for full details, environment variables, and test commands.

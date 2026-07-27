# Lazy Days Spa – Client

The React front end for the "Lazy Days Spa" app.

## What it does

- Home page listing the spa's **staff** and **treatments**.
- **Sign in / sign out** with JWT-based auth (`src/auth`), persisting the user in local storage.
- **Appointments** calendar showing available and booked slots, with the ability to schedule/cancel your own appointments (`src/components/appointments`).
- **User profile** page for viewing/updating your own account and appointments (`src/components/user`).
- Data fetching, caching, background refetching, prefetching, and optimistic mutations all implemented with **TanStack React Query** (`src/react-query` holds the shared query client and key factories).
- **Mock Service Worker (msw)** used to mock API responses for local development/tests, alongside the real Express server in `../server`.
- Styled with **Chakra UI**; navigation via **React Router**.

## Technologies used

- React 18 + TypeScript
- Vite
- TanStack React Query v5 + React Query Devtools
- Chakra UI
- React Router v6
- Axios
- Formik
- Day.js
- fast-json-patch
- MSW (Mock Service Worker)
- Vitest + Testing Library (unit/component tests)
- ESLint + Prettier

## Prerequisites

- Node.js (version matching `.nvmrc`) and npm
- The API server running (see [`../server/README.md`](../server/README.md)) — the client expects it at `http://localhost:3030`

## Setup

```bash
npm install
```

## Running the app

```bash
npm run dev     # or: npm start
```

The app will be available at the URL printed by Vite (typically http://localhost:5173).

## Other scripts

- `npm run build` – production build
- `npm run preview` – preview the production build locally
- `npm run lint` – run ESLint
- `npm test` – run the Vitest test suite

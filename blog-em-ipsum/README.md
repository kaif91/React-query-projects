# Blog 'em Ipsum

A small React demo app that fetches and displays a paginated list of blog posts (title + body) from a public "lorem ipsum" style JSON API, and lets you click into a post to view its details and comments.

## What it does

- Fetches a page of blog posts from `https://jsonplaceholder.typicode.com/posts` using **TanStack (React) Query**.
- Renders posts in a paginated list (`Posts.jsx`) with **Previous/Next** controls.
- **Prefetches** the next page of posts in the background so pagination feels instant.
- Clicking a post loads its **detail view** (`PostDetail.jsx`), including the post body and its comments, fetched on demand and cached by React Query.
- Includes **React Query Devtools** for inspecting cache/query state while developing.

## Technologies used

- [React 18](https://react.dev/)
- [Vite](https://vitejs.dev/) – dev server & build tool
- [TanStack React Query v5](https://tanstack.com/query/latest) – server-state fetching, caching, pagination & prefetching
- [React Query Devtools](https://tanstack.com/query/latest/docs/framework/react/devtools)
- ESLint (with `@tanstack/eslint-plugin-query`) for linting

## Prerequisites

- Node.js (version matching `.nvmrc`) and npm

## Setup

```bash
# from this folder
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

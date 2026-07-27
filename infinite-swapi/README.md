# Infinite SWAPI

A React demo app that implements **infinite scrolling** over the [Star Wars API (SWAPI)](https://swapi.dev/), loading additional pages of data automatically as the user scrolls.

## What it does

- Fetches paginated data from the SWAPI (`people` and `species` endpoints) using **TanStack (React) Query**'s `useInfiniteQuery`.
- Uses `react-infinite-scroller` to automatically request the next page as the user scrolls to the bottom of the list.
- Ships two independent infinite-list features:
  - `src/people/InfinitePeople.jsx` – infinite list of Star Wars characters.
  - `src/species/InfiniteSpecies.jsx` – infinite list of Star Wars species (currently the one rendered in `App.jsx`).
- Includes **React Query Devtools** for inspecting cache/query state (pages, fetch status) while developing.

## Technologies used

- [React 18](https://react.dev/)
- [Vite](https://vitejs.dev/) – dev server & build tool
- [TanStack React Query v5](https://tanstack.com/query/latest) – `useInfiniteQuery` for paginated/infinite data fetching
- [react-infinite-scroller](https://www.npmjs.com/package/react-infinite-scroller) – scroll-triggered pagination
- [React Query Devtools](https://tanstack.com/query/latest/docs/framework/react/devtools)
- ESLint for linting

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

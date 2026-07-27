# Lazy Days Spa Server

### A server for the "Lazy Days Spa" app"

## What it does

- Exposes a REST API (Express) consumed by the `client` app: staff, treatments, and appointments.
- Handles **authentication**: sign up / sign in, issuing and validating **JWTs** (`express-jwt` / `jsonwebtoken`), with passwords hashed via `pbkdf2`.
- Persists data as JSON files under `db/` (simple file-based "database"), read/written via `src/db-func`.
- Supports scheduling/cancelling appointments and updating user profiles for authenticated users, enforced via auth middleware (`src/middlewares`).
- Written in TypeScript, transpiled/run through Babel (`src/index.cjs` bootstraps the server).

## Technologies used

- [Node.js](https://nodejs.org/) + [Express](https://expressjs.com/)
- [TypeScript](https://www.typescriptlang.org/) (via Babel presets, not `tsc`, for runtime transpilation)
- [express-jwt](https://www.npmjs.com/package/express-jwt) / [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken) – auth
- [pbkdf2](https://www.npmjs.com/package/pbkdf2) – password hashing
- [cors](https://www.npmjs.com/package/cors), [body-parser](https://www.npmjs.com/package/body-parser)
- [dayjs](https://day.js.org/) – date handling
- [dotenv](https://www.npmjs.com/package/dotenv) – environment variables
- JSON files as the data store (`db/`)

## Installing

1. Run `npm install`
2. `cp .env_template .env`
3. Optional, only necessary if you're going to deploy: update `.env` to contain your own secret string (can just mash the keyboard for a long random string)

## Starting the server

Run `npm start`. The server will be found at [http://localhost:3030]

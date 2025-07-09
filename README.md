# NLW Agents

NLW Agents is a backend project developed during a Rocketseat event. It provides a Fastify-based API with TypeScript, using Drizzle ORM for database access and Zod for schema validation.

## Tech Stack

- **Node.js** + **TypeScript**
- **Fastify** (API server)
- **Drizzle ORM** (Database ORM)
- **PostgreSQL** (Database)
- **Zod** (Validation)
- **Biome** (Code formatting/linting)

## Project Structure

- `src/server.ts` — Main server entry point
- `src/http/routes/` — API route handlers
- `src/db/schema/` — Database schema definitions
- `src/db/migrations/` — Database migrations
- `src/db/seed.ts` — Database seeding script
- `drizzle.config.ts` — Drizzle ORM configuration

## Setup Instructions

1. **Clone the repository**
2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Configure environment variables:**
   - Copy `.env.example` to `.env` and fill in the required values (e.g., `PORT`, `DATABASE_URL`).
4. **Run database migrations:**
   ```bash
   npx drizzle-kit migrate:push
   ```
5. **(Optional) Seed the database:**
   ```bash
   npm run db:seed
   ```
6. **Start the development server:**
   ```bash
   npm run dev
   ```

## Scripts

- `npm run dev` — Start server in development mode
- `npm start` — Start server in production mode
- `npm run db:seed` — Seed the database

## Configuration

- **Database:** Configure the `DATABASE_URL` in your `.env` file for PostgreSQL connection.
- **Port:** Set the `PORT` variable in `.env` to specify the server port.

---

Developed during a Rocketseat event 🚀

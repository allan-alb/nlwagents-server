# NLW Agents — Audio Q&A Application

NLW Agents is an innovative Q&A backend application that allows users to send audio messages, which are automatically transcribed, stored in a vector database, and later used to generate answers for user questions. This enables users to build a knowledge base from their own voice notes and retrieve information through natural language queries.

## What Does the Application Do?

- **Audio Upload & Transcription:** Users can upload audio files. The application transcribes the audio into text using advanced speech-to-text technology.
- **Vector Database Storage:** Transcriptions are embedded and stored in a vector database, enabling efficient semantic search and retrieval.
- **Question Answering:** Users can ask questions at any time. The system searches the vector database for relevant information and generates answers using state-of-the-art language models.

This workflow makes it easy to capture, organize, and query knowledge using just your voice.

## Tech Stack

- **Node.js** + **TypeScript**
- **Fastify** — API server
- **Drizzle ORM** — Database ORM
- **PostgreSQL** — Relational database
- **Zod** — Schema validation
- **Biome** — Code formatting/linting
- **Vector Database** — For semantic search (e.g., Pinecone, Qdrant, or similar)
- **Speech-to-Text Service** — For audio transcription (e.g., Google Speech-to-Text, Whisper, or Gemini)
- **LLM Integration** — For answer generation (e.g., Gemini, OpenAI GPT)

## Project Structure

- `src/server.ts` — Main server entry point
- `src/http/routes/` — API route handlers (audio upload, question creation, etc.)
- `src/db/schema/` — Database schema definitions
- `src/db/migrations/` — Database migrations
- `src/db/seed.ts` — Database seeding script
- `drizzle.config.ts` — Drizzle ORM configuration

## Setup Instructions

> **Note**: Make sure you have **Node.js v22.16.0 or higher** installed.

1. **Clone the repository**
2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Configure environment variables:**
   - Copy `.env.example` to `.env` and fill in the required values (e.g., `PORT`, `DATABASE_URL`, vector DB/API keys, transcription/LLM API keys).
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

- **Database:** Set `DATABASE_URL` in your `.env` file for PostgreSQL connection.
- **Vector DB & APIs:** Provide credentials for your vector database and any external APIs (speech-to-text, LLM) in `.env`.
- **Port:** Set the `PORT` variable in `.env` to specify the server port.

---

Developed during a Rocketseat event 🚀

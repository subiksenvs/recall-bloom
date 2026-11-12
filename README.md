# Recall Bloom

An adaptive flashcard garden for small daily study loops.

## Features
- SQLite-backed decks and flashcards with edit-independent review history.
- Due queue using a lightweight spaced-repetition interval schedule.
- Again, Hard, Good, and Easy grading; study analytics; create and delete cards.
- Optional AI-generated card drafts, with a no-key demo fallback.

## Run
Requires Node.js 24+ (uses the built-in `node:sqlite` module).

```sh
npm install
cp .env.example .env
npm start
```

Visit http://127.0.0.1:8791. Set `OPENAI_API_KEY` in `.env` for generated card drafts. Review AI drafts for accuracy before studying.

## API
`GET /api/decks`, `GET /api/cards`, `POST /api/cards`, `DELETE /api/cards/:id`, `POST /api/cards/:id/grade`, `GET /api/stats`, `POST /api/generate`.

Stack: Express 5, Node.js, built-in SQLite, responsive browser client.

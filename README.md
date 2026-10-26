# TrueService

A small web app for recording local service providers with their price quotes and quality ratings, then searching them by service type and location. It is for people collecting quotes for jobs like moving, plumbing, or electrical work.

## Features

- Add a provider with name, service type, location, price quote, and a 1 to 5 rating
- Search by service type (exact match) and location (partial match)
- Shows the average price and average rating for the results
- Lists results with the highest-rated providers first
- Saves providers to a local `data.json` file

## Getting started

Requires Node.js.

```bash
npm install
npm start
```

Then open http://localhost:3013 in a browser. `npm run dev` runs the same server.

## How it works

- `index.html` contains the add-provider form and the search view, and calls the API on port 3013.
- `server.js` is an Express server that serves the page and exposes `POST /api/providers` and `GET /api/providers?service=&location=`.
- Providers are stored in `data.json` in the project folder, which is created on first run and ignored by git.
- `utils.js` contains validation helpers that `server.js` does not use yet.

## Status

Prototype. Ratings and prices are whatever users enter; nothing is verified, and there are no accounts or input validation.

## License

MIT, see [LICENSE](LICENSE).

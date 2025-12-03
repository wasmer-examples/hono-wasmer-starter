# Hono WinterCG Worker + Wasmer

This example shows how to run a minimalist **Hono** application inside a **WinterCG-compatible worker** on **Wasmer Edge**.

## Demo

`https://<your-subdomain>.wasmer.app/` (deploy to get a live worker endpoint)

## How it Works

All logic lives in `src/index.ts`:

* `const app = new Hono()` creates the router.
* `app.get("/", c => c.text("Hello Hono!"))` responds with plain text for the root route.
* `export default app` exposes the handler so WinterCG (and Wasmer Edge) can serve it.

Wrangler is used during development to simulate the worker environment locally.

## Running Locally

```bash
npm install
npm run dev
```

Wrangler will watch `src/index.ts` and serve the worker at `http://127.0.0.1:8787/`.

## Deploying to Wasmer (Overview)

1. Build the worker bundle (Wasmer Edge accepts the ESM output from Wrangler or esbuild).
2. Deploy the project with `wasmer deploy` or through the Wasmer dashboard.
3. Visit `https://<your-subdomain>.wasmer.app/` to see the “Hello Hono!” response.

```txt
npm install
npm run dev
```

```txt
npm run deploy
```


This is a [Hono](https://hono.dev) project bootstrapped with `create-hono` (with some minor adaptations for Wasmer).

## Getting Started

First, run the development server:

```bash
npm run dev
```

You can run the Hono example using Wasmer (check out the [install guide](https://docs.wasmer.io/install)):

```bash
wasmer run wasmer-examples/hono-wasmer-starter --net
```

> [!TIP]
> You can also run `wasmer run . --net` in the root of this repo

Open [http://localhost:3000](http://localhost:3000) with your browser to see your Hono app.

## Deploy on Wasmer Edge

The easiest way to deploy your Hono app is to use the [Wasmer Edge](https://wasmer.io/products/edge).

Live example: https://hono-wasmer-starter.wasmer.app/

First, you'll need to run `npm run build`, and then, to deploy to Wasmer Edge:

```bash
wasmer deploy
```

> [!NOTE]
> You will need to have Wasmer installed (check out [the docs to install the Wasmer CLI](https://docs.wasmer.io/install)!). 
> You will also need to change the namespace in `wasmer.toml` to your own namespace and app name in `app.yaml` to your own app name.

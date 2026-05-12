# Cafe Management System (Microservices)

This repository contains a **microservices-based** Cafe Management System.

## Vercel deployment

Because the project is composed of multiple Node services, Vercel support may require extra configuration. A basic `vercel.json` has been added at the repo root.

### Required approach
- Vercel will deploy the Node entrypoints it finds under each service.
- In this repo snapshot, each microservice directory contains a `Dockerfile` but the JS sources (e.g. `index.js`) and each service’s `package.json` were not present.

### What to do before deploying
1. Ensure each service directory contains:
   - `package.json`
   - JS entry file (commonly `index.js`)
2. Commit those files.
3. Re-deploy on Vercel.

If you want a working Vercel app, the recommended option is to deploy **only** `api-gateway` as the entry service and keep other services behind it (or bundle them another way), because Vercel’s multi-service setups require all entrypoints to exist.


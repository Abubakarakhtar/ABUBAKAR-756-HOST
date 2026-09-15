# ABUBAKAR 756 HOST — STAGE 3

Stage 3 connects the Worker backend to the Cloudflare Pages API. Cloudflare API tokens must stay server-side as Worker secrets.

## Secrets
- CLOUDFLARE_API_TOKEN: Cloudflare token with Pages Write permission
- CLOUDFLARE_ACCOUNT_ID: your Cloudflare account ID
- DEPLOY_SECRET: optional private secret used by the frontend request

## Worker
Deploy `worker/worker.js` with `worker/wrangler.toml`. Then put the Worker URL in the dashboard.

## Important
Stage 3 is a functional HTML deployment prototype. Asset ZIP/folder deployment, update keys, project listing, delete/update and polished dashboard are planned for later stages.

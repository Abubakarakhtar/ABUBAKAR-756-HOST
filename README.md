# ABUBAKAR 756 HOST — Stage 4

Stage 4 adds ZIP/static-file uploads and Cloudflare Pages Direct Upload through a secure Worker.

## 1. Worker secrets
Set these secrets on the Worker:
- CLOUDFLARE_API_TOKEN — token with Pages Write permission
- CLOUDFLARE_ACCOUNT_ID — your Cloudflare account ID
- DEPLOY_SECRET — optional shared secret for your frontend

Never put the Cloudflare API token in `index.html` or `app.js`.

## 2. Deploy the Worker
From the `worker` folder with Wrangler:
`wrangler deploy`

Or create a Worker in the Cloudflare dashboard and upload `worker.js`, then add the secrets under Worker Settings > Variables and Secrets.

## 3. Use the Stage 4 site
Enter the Worker URL, project name, and optional Deploy Secret. Choose ZIP upload or HTML mode. A ZIP must contain `index.html` at its root.

Stage 4 upload limit is 8 MB total and 20,000 files. Cloudflare's Pages API supports direct-upload manifests and asset upload; this build uses that flow.

## 4. Security
Do not share your Cloudflare API token. If it is ever exposed, revoke/rotate it immediately.

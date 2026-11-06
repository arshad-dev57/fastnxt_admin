# FastNxt Admin

Platform console for FastNxt operators. View registered schools and subscription status.

## Allowed login

Only accounts listed on the **API** via env vars can sign in:

```bash
PLATFORM_ADMIN_EMAILS=
PLATFORM_ADMIN_PASSWORD=
PLATFORM_COOKIE_NAME=bisons_platform_session
```

## How API calls work (no CORS)

The browser talks only to this Next app (`/backend-api/...`).  
`app/backend-api/[...path]` proxies to Railway using server-only `API_URL`.  
You do **not** need to add the admin Vercel URL to backend `CORS_ORIGINS`.

## Local setup

```bash
npm install
# .env.local → API_URL=http://localhost:5000/api
npm run dev
```

## Vercel env

```bash
API_URL=https://YOUR-RAILWAY-API.up.railway.app/api
```

Server-only (no `NEXT_PUBLIC_`). Redeploy after changing it.

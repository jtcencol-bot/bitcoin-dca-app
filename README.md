# Bitcoin DCA Calculator (CAD)

Static web app for CAD-based BTC DCA + dip-buy tracking.

## Privacy
- No personal defaults are preloaded.
- Data stays in browser localStorage unless user imports/exports manually.

## Local run
```bash
cd bitcoin-dca-app
python3 -m http.server 8787
# open http://localhost:8787
```

## Deploy (Cloudflare Pages)
1. Push this folder to a GitHub repo.
2. In Cloudflare Pages: Create project -> Connect repo.
3. Build command: (leave empty)
4. Build output directory: `/`
5. Deploy.

## Deploy (Vercel)
```bash
cd bitcoin-dca-app
npx vercel --prod
```

## Backout / Kill switch
- Cloudflare Pages: Project -> Settings -> Disable production deployment OR Delete project.
- Vercel: Project -> Settings -> Domains (remove domain) or Project -> Delete.
- Also revoke any custom domain DNS record to hard stop public access.

## Notes
- Price history uses CryptoCompare endpoints from the browser.
- If rate-limited later, move fetch to a tiny serverless proxy endpoint with caching.

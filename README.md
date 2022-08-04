# Bug report (Vite 3)

When the initial render fails because of a missing import, fixing the issue does not automatically re-render the page. It needs to be force-refreshed manually.

To reproduce:
- Install dependencies with `pnpm install`
- Run `pnpm dev` and open the http://localhost:5173
- Notice the error caused by the invalid import in `counter.js` as expected
- Remove the invalid import
- **BUG:** The page should reload and render successfully

This does not happen with Vite 2 (tested with v2.9.14).

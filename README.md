# UNSC Chit Marking Desk (Vercel)

Static page (`index.html`) plus one serverless function (`api/mark.js`) that sends each chit to the Claude API and returns the grades. The final mark is computed in the page with fixed rules, so it always stays within 0.1–1 (normal) or 1–5 (substantive).

## Deploy

1. On vercel.com: Add New → Project → import the `nandani-svg/unsc` GitHub repo.
2. Leave **Root Directory** as the repo root. Framework preset: **Other**. Leave build settings empty.
3. Add environment variables:
   - `ANTHROPIC_API_KEY`: your key from console.anthropic.com (required)
   - `ACCESS_CODE`: any password; the page asks for it so strangers can't spend your credits (recommended)
4. Deploy. If you add or change a variable later, redeploy for it to take effect.

The marks register is kept in the browser that marked the chits. Download the CSV as a backup.
- `claude-artifact/index.html` is the claude.ai Artifact version (uses the viewer's Claude account instead of an API key).

# Miraj & Partners All in One Store – Website with AI assistant

Files
- `index.html` – the website (shop assistant chat button included)
- `api/chat.js` – the AI assistant server function (runs on Vercel)
- `api/_catalogue.js` – shop details and a small backup list (the products already shown on the website)
- `package.json` – tells Vercel to use Node 18 or newer

What the AI does
- Customer asks about a product: the AI checks the shop's private stock sheet and replies "Yes, available. For price, please contact us on WhatsApp 03159027799 or call 03424077562."
- It never gives prices and never shares the product list, price list or catalogue. Requests for the list are refused before the AI is even called, and the AI only ever sees the few items that match the customer's question.

Set up (in Vercel, Settings, Environment Variables)
1. `ANTHROPIC_API_KEY` – your key from https://console.anthropic.com
2. `PRODUCT_SHEET_URL` – the "Publish to web" CSV link of your Google Sheet stock list
Redeploy after adding them.

Keep private
- Never put the API key or the sheet link in GitHub, index.html or any file. Only in Vercel's Environment Variables.
- The stock list is not shown anywhere on the website.

Optional (Vercel Environment Variables)
- `ANTHROPIC_MODEL` – change the AI model (default `claude-haiku-5-5`)
- `ALLOWED_ORIGINS` – only allow these websites to use the AI, for example `https://miraj-partners-all-in-one-store.vercel.app`

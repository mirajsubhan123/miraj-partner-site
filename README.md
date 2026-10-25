# Miraj & Partners All in One Store – Website with AI assistant

Files
- `index.html` – the website (shop assistant chat button included)
- `api/chat.js` – the AI assistant server function (runs on Vercel)
- `api/_catalogue.js` – shop details and product list the AI knows (ask Claude for a new copy when products change)
- `package.json` – tells Vercel to use Node 18 or newer

How the AI turns on
1. Upload all files (including the `api` folder) to the GitHub repository.
2. Deploy the repository on Vercel (https://vercel.com, Add New, Project, Import).
3. In Vercel: Settings, Environment Variables, add `ANTHROPIC_API_KEY` with your key from https://console.anthropic.com, then redeploy.
4. Open your `...vercel.app` link. The chat button now says it is an AI assistant.

Never put the API key in GitHub or in index.html. It belongs only in Vercel's Environment Variables.

If the AI is not available, the chat falls back to the built-in product search, so customers always get an answer.

Optional settings (Vercel Environment Variables)
- `ANTHROPIC_MODEL` – change the AI model (default `claude-haiku-5-5`)
- `ALLOWED_ORIGINS` – only allow these websites to use the AI, for example `https://miraj-partners.vercel.app,https://mirajsubhan123.github.io`

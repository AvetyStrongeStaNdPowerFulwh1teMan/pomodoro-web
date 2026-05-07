# Pomodoro Timer (single HTML file)

Single static page (`index.html`) with inline CSS and JavaScript. No build step.

## Security model

What this code does:
- Stores productivity stats in browser `localStorage` only.
- Uses no `fetch`, XHR, WebSocket, or external `<script src>`.
- Contains no API keys or backend credentials in repository files.

What this code does not guarantee:
- Hosting platforms (GitHub/Vercel) still receive normal web request metadata (IP, user-agent, logs).
- Browser extensions on a user device can access what the browser can access.
- If someone adds network code in future commits, behavior changes.

## Safe publishing checklist

- Never commit `.env`, private keys (`.pem`), tokens, or credentials.
- Keep this project static-only unless network behavior is reviewed first.
- Re-run secret scan before release (for example: `gitleaks` or GitHub secret scanning).

## Run

Open `index.html` directly in a browser, or host as static files.

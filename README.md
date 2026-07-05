# Rocommand

> One endpoint. Every Discord webhook relayed.

Rocommand is a lightweight proxy for Discord webhooks.

Instead of exposing your real Discord webhook URL to your game, script, or application, you send requests to a Rocommand endpoint. Rocommand securely forwards the request to Discord while handling retries and rate limits for you.

Perfect for Roblox games, bots, automation, and any application that sends lots of webhook requests.

## Why?

Using Discord webhooks directly has a few downsides:

- Your webhook URL is exposed to anyone with access to your code.
- Bursts of requests can hit Discord rate limits.
- If your webhook is leaked, it can be abused.
- Rotating webhooks means updating every script using them.

Rocommand solves this by placing a relay in front of your webhook.

```
Your App
     │
     ▼
Rocommand Proxy
     │
     ▼
Discord Webhook
```

Your application never knows the real Discord webhook URL.

## Features

- 🔒 Hide your real Discord webhook URL
- 🚀 Automatic Discord rate-limit handling
- 🔁 Retries failed requests automatically
- ⚡ Drop-in replacement for Discord webhooks
- 📦 No code changes besides replacing the URL
- 🗄️ Stateless design — no webhook database

## How it works

1. Add your Discord webhook in the dashboard.
2. Rocommand generates a proxy URL.
3. Replace your Discord webhook URL with the proxy URL.
4. Continue sending the exact same JSON payloads.

Nothing else changes.

## Example

Before:

```lua
local webhook = "https://discord.com/api/webhooks/..."
```

After:

```lua
local webhook = "https://rocommand.elementfx.com/wh/abc123..."
```

Everything else stays exactly the same.

## Use Cases

- Roblox server logs
- Moderation logs
- Analytics events
- Error reporting
- Game notifications
- Bot integrations
- Internal automation

## Website

https://rocommand.elementfx.com

---

Built to make Discord webhooks safer and more reliable.
<img width="1893" height="942" alt="image" src="https://github.com/user-attachments/assets/cf5d79fa-560a-4fc4-94fd-469aa237eddd" />
<img width="1902" height="939" alt="image" src="https://github.com/user-attachments/assets/9a235cdc-79aa-4edf-977a-b4b50886443d" />

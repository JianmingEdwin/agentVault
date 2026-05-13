[README.md](https://github.com/user-attachments/files/27716466/README.md)
# AgentVault — AI Blockchain Agent (GitHub Pages Edition)

A single-file AI-powered blockchain wallet agent dashboard.  
**One file. Zero build step. Deploy in 2 minutes.**

---

## What it does

- Creates AI agents powered by **real Claude AI** (claude-sonnet-4)
- Generates two simulated wallet addresses per agent
- Live chat with Claude — the agent knows your wallets and chain
- Supports Ethereum, Polygon, BSC, Solana, Avalanche
- Persists agent state in `localStorage` across page refreshes
- Export agent data as JSON
- Works entirely from a single `index.html` file

---

## Deploy to GitHub Pages (Step-by-Step)

### Step 1 — Create a new GitHub repository

1. Go to [github.com](https://github.com) and sign in
2. Click the **+** button → **New repository**
3. Name it anything, e.g. `agentvault`
4. Set it to **Public**
5. Click **Create repository**

---

### Step 2 — Upload the file

**Option A — GitHub web UI (easiest)**

1. Inside your new repo, click **"uploading an existing file"**
2. Drag and drop `index.html` onto the page
3. Click **Commit changes**

**Option B — Git command line**

```bash
git clone https://github.com/YOUR_USERNAME/agentvault.git
cd agentvault
cp /path/to/index.html .
git add index.html
git commit -m "Deploy AgentVault"
git push origin main
```

---

### Step 3 — Enable GitHub Pages

1. In your repo, click **Settings** (top menu)
2. Scroll down to **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Choose branch: **main**, folder: **/ (root)**
5. Click **Save**

GitHub will show a green banner:
> "Your site is published at `https://YOUR_USERNAME.github.io/agentvault/`"

This takes about **1–2 minutes**.

---

### Step 4 — Open the app and use it

1. Visit `https://YOUR_USERNAME.github.io/agentvault/`
2. Select a blockchain from the dropdown
3. (Optional) Enter an agent name
4. Click **"Create AI Agent"**
5. Watch the AI reasoning log as Claude initializes your agent
6. Chat with your agent in the chat panel below

---

## Important: API Key Note

The app calls the Anthropic Claude API directly from the browser.  
The API is billed by Anthropic to your account.

**For personal demo use, this works fine.**  
For a public-facing production app, proxy API calls through a backend
(e.g. Cloudflare Workers, Vercel Functions) so your key is not exposed
in network requests.

---

## File Structure

```
agentvault/
└── index.html    ← The entire app (HTML + CSS + JS in one file)
└── README.md     ← This file
```

---

## Features

| Feature | Detail |
|---|---|
| AI Engine | Claude claude-sonnet-4 via Anthropic API |
| Wallet Generation | Simulated addresses (demo only) |
| Chat Memory | Last 20 messages sent as context |
| State Persistence | Browser localStorage |
| Deployment | Zero build step — pure static HTML |
| Blockchains | Ethereum, Polygon, BSC, Solana, Avalanche |

---

## Security Warning

> ⚠ This is a **demo application**.
> - Wallet addresses are **simulated** — not real blockchain addresses
> - Do **not** send real funds to generated addresses
> - For production use, move API calls to a secure backend

---

## License

MIT

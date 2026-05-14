# Matthew — Coding AI

A no-limits coding AI powered by Claude claude-sonnet-4-20250514.

## Files

```
matthew-ai/
├── index.html        ← frontend UI
├── api/
│   └── chat.js       ← Vercel Edge Function (proxies to Anthropic)
├── vercel.json       ← routing config
└── package.json
```

## Deploy to Vercel

### 1. Install Vercel CLI (if you haven't)
```bash
npm i -g vercel
```

### 2. Deploy
```bash
cd matthew-ai
vercel
```
Follow the prompts — pick a project name, leave everything else default.

### 3. Add your Gemini API key (free!)
After deploying, go to:
**Vercel Dashboard → Your Project → Settings → Environment Variables**

Add:
- **Name:** `GEMINI_API_KEY`
- **Value:** your key from https://aistudio.google.com/apikey
- **Environment:** Production, Preview, Development

Then redeploy:
```bash
vercel --prod
```

### 4. Done!
Your Matthew AI is live at `https://your-project.vercel.app`

---

## Get a Free Gemini API Key
1. Go to https://aistudio.google.com/apikey
2. Sign in with your Google account
3. Click **Create API key**
4. Copy it into Vercel env vars above

No credit card required. The free tier includes 1,500 requests/day with Gemini 2.0 Flash.

# PromptCraft — AI-Powered Prompt Generator

> Generate 6 categorised, ready-to-use AI prompts for any topic instantly — powered by OpenRouter's free LLM API.

---

## 🌐 Live Demo

🔗 **[promptcraft.vercel.app](https://promptcraft.vercel.app)** *(replace with your actual Vercel URL)*

---

## 📌 What is PromptCraft?

Most people don't know how to talk to AI effectively. They type vague questions and get vague answers.

**PromptCraft** solves this — you type any topic you want to learn or build, and it instantly generates **6 high-quality, categorised AI prompts** you can copy and paste into ChatGPT, Claude, Gemini, or any AI chatbot.

---

## ✨ Features

- 🤖 **AI-generated prompts** — powered by OpenRouter free LLM API
- 📂 **6 prompt categories** — Beginner, Intermediate, Advanced, Project, Concept, Interview
- 🪟 **Modal popup results** — no scrolling needed, results appear front and center
- ⚡ **Quick pick chips** — Python, React, ML, DSA, SQL, Git, REST API, Cybersecurity
- 📋 **One-click copy** — copy any prompt to clipboard instantly
- 🔗 **Try in ChatGPT** — opens ChatGPT with the prompt pre-filled
- 💾 **API key persistence** — saved in browser localStorage, no re-entry needed
- 📱 **Fully responsive** — works on mobile, tablet, and desktop
- 🆓 **100% free** — uses OpenRouter's free model tier, zero cost

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Structure and markup |
| CSS3 | Styling, animations, responsive layout |
| JavaScript (Vanilla ES6+) | App logic, API calls, DOM manipulation |
| OpenRouter API | Free LLM inference (prompt generation) |
| Vercel | Hosting and deployment |

---

## 🚀 Getting Started

### Step 1 — Get a Free OpenRouter API Key

1. Go to [openrouter.ai](https://openrouter.ai)
2. Sign up for a free account
3. Navigate to **Keys** → click **Create Key**
4. Copy your key — it starts with `sk-or-v1-...`

> Free tier gives you enough credits to demo and use the app without any cost.

### Step 2 — Run Locally

No installation or build step needed. Just:

```bash
# Clone the repo
git clone https://github.com/your-username/promptcraft.git

# Open directly in browser
cd promptcraft
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

### Step 3 — Use the App

1. Paste your OpenRouter API key → click **Save Key**
2. Type any topic (e.g. `Learn Python`, `Build a REST API`)
3. Click **Generate Prompts**
4. A modal pops up with 6 ready-to-use prompts
5. Click **Copy prompt** or **Try in ChatGPT**

---

## 📁 Project Structure

```
promptcraft/
│
└── index.html       # Complete app — HTML + CSS + JS in one file
└── README.md        # Project documentation
```

> The entire application lives in a single `index.html` file. No frameworks, no dependencies, no build tools required.


## 🔑 API Details

- **Provider:** [OpenRouter](https://openrouter.ai)
- **Model:** `openrouter/free` (auto-routes to best available free model)
- **Endpoint:** `https://openrouter.ai/api/v1/chat/completions`
- **Cost:** $0 — free tier only
- **Rate limit:** 20 requests/min · 50 requests/day (free tier)

### How the API is called

```javascript
const response = await fetch('https://openrouter.ai/api/v1/chat/completions', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': `Bearer ${API_KEY}`,
  },
  body: JSON.stringify({
    model: 'openrouter/free',
    messages: [{ role: 'user', content: prompt }],
    max_tokens: 1200
  })
});
```

---

## ☁️ Deployment (Vercel)

This project is deployed on [Vercel](https://vercel.com) for free.

### Deploy your own in 2 minutes:

**Option A — Drag & Drop (easiest)**
1. Go to [vercel.com](https://vercel.com) → Sign up
2. Click **Add New Project**
3. Drag and drop your project folder
4. Done — you get a live URL instantly ✅

**Option B — Via GitHub**
1. Push this repo to GitHub
2. Go to [vercel.com](https://vercel.com) → **Add New Project**
3. Import your GitHub repository
4. Click **Deploy**
5. Every future `git push` auto-deploys ✅

---

## ⚠️ Troubleshooting

| Error | Cause | Fix |
|---|---|---|
| `401 Unauthorized` | Wrong API key | Re-enter your key from openrouter.ai/keys |
| `429 Too Many Requests` | Rate limit hit | Wait 1 minute and try again |
| Modal shows no prompts | JSON parse error | Retry — the free model occasionally returns malformed JSON |
| Key not saving | localStorage blocked | Allow cookies/storage in your browser settings |

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👨‍💻 Author

Built by **NEMMADI RAJ KUMAR** as a college project — VIGNAN UNIVERSITY, 2024–26.

---

## 🙏 Acknowledgements

- [OpenRouter](https://openrouter.ai) — for providing free LLM API access
- [Vercel](https://vercel.com) — for free hosting and deployment
- [Google Fonts](https://fonts.google.com) — Syne & DM Sans typefaces
- [Meta AI](https://ai.meta.com) — LLaMA models powering the free tier

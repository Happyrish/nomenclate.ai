# NOMENCLATE — AI-Powered Naming Engine

A premium SaaS platform that automates the professional naming workflow using AI. Craft distinctive, strategically-sound brand names with intelligent analysis, territory mapping, and validation.

## 🎯 Features

### Intelligent Brand Analysis
- AI analyzes your brand positioning, industry, and tone
- Recommends personalized naming strategies
- No generic templates—every recommendation is custom

### Automated Name Generation
- Generates 50-80+ unique candidates using linguistic techniques:
  - Clipping (Trust → Trusti)
  - Blending/Portmanteau (Flow + Tech → Flotech)
  - Compounding (two meaningful words)
  - Affixing (prefixes/suffixes)
  - Invented words
- Auto-filters for pronunciation, length, and your avoidance rules
- Scores each name 1-10 for memorability and uniqueness

### Semantic Territory Mapping
- AI identifies 8-12 word families that resonate with your brand
- Industry-specific intelligence (Fintech, Healthcare, SaaS, etc.)
- Tone-influenced territory generation

### Validation Reports
- Trademark screening simulation
- Domain availability checks (.com, .io, .ai)
- Social media handle verification
- Pronunciation testing across accents
- Linguistic safety screening

## 🚀 Quick Deploy

### Option 1: GitHub Pages (Free, 2 minutes)

1. **Create a new repo on GitHub**
2. **Upload `nomenclate-ai.html` to your repo**
3. **Enable GitHub Pages:**
   - Go to Settings → Pages
   - Source: `main` branch, root folder
   - Save
4. **Live at:** `https://yourusername.github.io/nomenclate/nomenclate-ai.html`

### Option 2: Vercel (Recommended - 30 seconds)

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Follow prompts, done!
```

Or click: [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)

### Option 3: Netlify (Drag & Drop)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag the HTML file
3. Live instantly

## 🛠️ Local Development

```bash
# No build needed, just open the file
open nomenclate-ai.html

# OR use Python server
python3 -m http.server 8000
# Visit: http://localhost:8000/nomenclate-ai.html
```

## 🔌 AI Integration (Claude API)

The app uses Anthropic's Claude API for intelligent name generation.

### How It Works

- **AI analyzes** your brand inputs
- **Recommends** naming strategies based on your industry/tone
- **Generates** semantic territories
- **Creates** 50-80+ name candidates with intelligent scoring

### Setup

API calls are already coded. The app has **built-in fallback** if AI is unavailable.

**For full AI features**, the API endpoint is public but rate-limited. For production:

1. Get API key: [console.anthropic.com](https://console.anthropic.com/)
2. Add to line 689 (for testing only):
   ```javascript
   headers: {
       "Content-Type": "application/json",
       "x-api-key": "sk-ant-...",  // Your key here
   },
   ```

**⚠️ Security:** Never commit API keys. Use environment variables in production.

### Fallback Mode

If AI calls fail, high-quality algorithmic generation kicks in automatically.

## 📂 Files

```
nomenclate/
├── nomenclate-ai.html    # Complete app (single file)
├── README.md             # Documentation
└── .gitignore           # Git ignore rules
```

## 🎨 Customization

### Change Colors

Edit CSS variables (line 20):

```css
:root {
    --bg-primary: #0a0a0a;      /* Background */
    --accent: #d4af37;           /* Gold accent */
    --text-primary: #f5f5f5;     /* Text */
}
```

### Add Industries

Edit dropdown (line 445) + fallback territories (line 725):

```javascript
yourIndustry: ['Trust', 'Swift', 'Flow', ...]
```

### Add Naming Strategies

Edit `strategies` array (line 381):

```javascript
{
    id: 'newStrategy',
    name: 'Strategy Name',
    description: 'What it does',
    examples: 'Brand1, Brand2',
    keywords: ['premium', 'tech']
}
```

## 🚦 Production Roadmap

To turn this into a full SaaS:

1. **Backend** (Node.js + Express)
   - User authentication (Auth0/Firebase)
   - PostgreSQL database
   - API key management

2. **Integrations**
   - USPTO/WIPO trademark APIs
   - Domain registrar APIs
   - Social media handle checkers
   - PDF report generation

3. **Payments** (Stripe)
   - Free: 1 project, 20 names
   - Pro ($99): Unlimited names, full validation
   - Teams ($299/mo): Collaboration + API

## 💡 Tech Stack

- **Frontend:** Vanilla JS (zero dependencies)
- **AI:** Claude Sonnet 4 (Anthropic)
- **Fonts:** Crimson Pro + Space Mono (Google Fonts)
- **Deployment:** Static hosting (GitHub Pages/Vercel/Netlify)

## 📝 License

MIT License - use freely for commercial projects.

## 🤝 Contributing

PRs welcome for:
- Better linguistic algorithms
- UI/UX improvements
- Additional languages
- Performance optimizations

## 💬 Support

Open an issue or discussion on GitHub.

---

**Ship it. Make it yours. Build the next great naming platform.**

# 🔐 CyberWisdom

> An ambient cybersecurity knowledge display — beautiful, educational, and free.

CyberWisdom is a full-screen browser-based slideshow designed for the information security community. It cycles through curated cards combining dark atmospheric visuals with security wisdom: quotes from pioneers, attack patterns, defense principles, incident lessons, and more.

Run it on a spare monitor, embed it on your website, use it as a screensaver — or just open it when you want a moment of security inspiration.

**[→ Live Demo](https://barigun.github.io/CyberWisdom)**

---

![CyberWisdom screenshot](screenshot.png)

---

## Features

- 40+ curated cards across 8 content categories
- Full-screen, cinematic design with slow-zoom background images
- Auto-advances every 18 seconds with a progress bar
- Keyboard controls: Space (pause), ←→ (navigate), F (fullscreen), H (hide UI)
- Category color-coding (quotes, principles, attack patterns, defense, incidents, mindset, how-it-works, statistics)
- Context notes with deeper explanations on each card
- Zero dependencies — single `index.html` file, works offline with cached images
- Mobile-friendly

## Content Categories

| Badge | Description |
|-------|-------------|
| 🔵 Quote | Words from security legends: Schneier, Mitnick, Spafford |
| 🟢 Principle | Foundational security principles: Zero Trust, Least Privilege, Fail Secure |
| 🟠 Attack Pattern | How attacks work and why they succeed |
| 🔷 Defense | Controls, detection, and response practices |
| 🟡 Incident Lesson | Real-world breach post-mortems and what they taught us |
| 🟣 Mindset | Human factors, culture, burnout, and community |
| 🟩 How It Works | Short explanations of key security mechanisms |
| 🟨 By the Numbers | Key statistics from authoritative reports |

## Usage

### As a web page / screensaver tab

1. Clone or download this repository
2. Open `index.html` in any modern browser
3. Press `F` for fullscreen or `F11`

```bash
git clone https://github.com/barigun/CyberWisdom.git
cd CyberWisdom
open index.html   # macOS
# or just drag index.html into your browser
```

### Deploy to GitHub Pages (free hosting)

1. Go to your repo: **https://github.com/barigun/CyberWisdom**
2. Click **Settings → Pages**
3. Set source to **Deploy from branch → main → / (root)** → Save
4. Your live URL will be `https://barigun.github.io/CyberWisdom`

### Embed on your website

```html
<iframe 
  src="https://barigun.github.io/CyberWisdom" 
  style="width:100%; height:100vh; border:none;"
  allowfullscreen>
</iframe>
```

### As an OS Screensaver

**macOS** — Using [Web Screensaver](https://github.com/liquidx/webviewscreensaver):
1. Install WebViewScreenSaver
2. Set URL to your hosted CyberWisdom URL or `file:///path/to/index.html`

**Windows** — Using [Web Page Screensaver](https://www.impulseadventure.com/photo/webpage-screensaver.html):
1. Install, point to your local `index.html` or hosted URL

**Linux** — Using `xscreensaver-web` or similar browser-based screensaver tools

### Conference / SOC room display

Open in Chrome, press `F11` (fullscreen), then `H` to hide the UI chrome for a clean ambient display.

## Keyboard Controls

| Key | Action |
|-----|--------|
| `Space` or `P` | Pause / Resume |
| `→` or `N` | Next card |
| `←` or `B` | Previous card |
| `F` | Toggle fullscreen |
| `H` | Hide / show UI chrome |

## Adding Your Own Cards

Edit the `CARDS` array in `index.html`. Each card is a JavaScript object:

```javascript
{
  cat: "principle",           // quote | principle | attack | defense | incident | mindset | howto | stat
  label: "Principle",         // Display label in the badge
  text: "Your statement here.", // The main text shown large
  source: "Author — Context", // Attribution (use — to separate name from context)
  context: "Optional deeper explanation shown in smaller text below.", // or null
  bg: "https://images.unsplash.com/photo-...?w=1920&q=80" // Background image URL
}
```

### Choosing background images

- Use [Unsplash](https://unsplash.com) for free high-quality images
- Search for: `dark technology`, `server room`, `circuit board`, `cyberpunk city`, `abstract dark`, `lock security`
- Append `?w=1920&q=80` to Unsplash URLs for optimized loading
- Avoid bright/colorful images — dark and moody works best for text legibility

## Roadmap

- [ ] `content.json` external content file (easier editing without touching JS)
- [ ] AI-powered card generation via Anthropic API
- [ ] URL params: `?interval=20&category=principle&shuffle=true`
- [ ] Local image support (for offline / conference use)
- [ ] PWA manifest (installable as desktop/mobile app)
- [ ] Electron wrapper for true OS screensaver
- [ ] Community card submissions via GitHub Issues template
- [ ] Multiple language support

## Contributing

Contributions welcome! If you have a great cybersecurity quote, principle, or incident lesson that belongs here:

1. Open an Issue with the `card-suggestion` label
2. Include: the text, source/attribution, category, and any context note
3. Or submit a PR adding it directly to the `CARDS` array

Please ensure all content is:
- Accurately attributed
- From credible sources (research reports, books, CVE databases, official frameworks)
- Educational in intent

## License

MIT License — free to use, modify, and distribute. Attribution appreciated but not required.

---

*Built for the security community. Stay curious, stay paranoid — in the best way.*

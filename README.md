# CoolWiki

A beautifully designed, single-file Wikipedia client built with pure HTML, CSS, and JavaScript. No frameworks, no build tools — just open it in a browser.

![Dark Theme](https://img.shields.io/badge/theme-dark%20%7C%20light-gold)
![Single File](https://img.shields.io/badge/build-single%20file-brightgreen)
![No Dependencies](https://img.shields.io/badge/dependencies-none-blue)

---

## ✨ Features

- **Article Feed** — Daily featured article and trending Wikipedia articles on the home screen
- **Full Article View** — Clean, distraction-free reading with hero images and rich formatting
- **Search** — Real-time Wikipedia search with debounced input
- **Saved Articles** — Bookmark articles for offline reading via `localStorage`
- **Random Article** — Discover something new instantly with the dice button
- **Math Rendering** — LaTeX/KaTeX support for mathematical content
- **Multi-language** — Switch between EN, ES, FR, DE, JA, and ZH Wikipedia editions
- **Dark / Light Theme** — Toggle between modes; preference is persisted
- **Data Saver Mode** — Hide images to reduce bandwidth on mobile
- **Adjustable Font Size** — Small, Medium, Large, X-Large reading sizes

## 🎨 Design

CoolWiki uses a custom *Dark Literary Luxury* design system:

- **Fonts:** Cormorant Garamond (display), Newsreader (reading), DM Mono (UI)
- **Palette:** Deep charcoal backgrounds with gold accents (`#C4964A`)
- **Motion:** Silk-eased animations (`cubic-bezier(0.16, 1, 0.3, 1)`)
- **Nav:** Floating frosted-glass pill with bottom navigation
- **Texture:** Subtle SVG film grain overlay

## 🚀 Getting Started

No installation required.

```bash
# Clone the repo
git clone https://github.com/your-username/coolwiki.git

# Open in your browser
open index.html
```

Or just download `index.html` and open it directly — it's entirely self-contained.

> **Note:** CoolWiki fetches data from the [Wikipedia REST API](https://en.wikipedia.org/api/rest_v1/) and [Wikimedia Feed API](https://api.wikimedia.org/wiki/Feed_API). An internet connection is required to load content; saved articles are available offline.

## 📁 File Structure

```
coolwiki/
└── index.html      # The entire app — HTML, CSS, and JS in one file
└── fevicon.png     # App favicon (optional)
```

## 🔧 Customization

All design tokens live in the `:root` CSS block at the top of `index.html`. You can change the color palette, fonts, and spacing without touching any JavaScript.

```css
:root {
    --bg:      #0D0C0A;   /* background */
    --gold:    #C4964A;   /* accent color */
    --font-display: 'Cormorant Garamond', serif;
    /* ... */
}
```

## 📱 Browser Support

Works in all modern browsers. Optimized for mobile with:
- `viewport-fit=cover` for notch-safe layout
- `env(safe-area-inset-bottom)` padding
- Touch-friendly tap targets
- `overscroll-behavior` for native-feel scrolling

## 🗂️ API Sources

| Data | Endpoint |
|------|----------|
| Featured feed | `https://api.wikimedia.org/feed/v1/wikipedia/{lang}/featured/{date}` |
| Article content | `https://{lang}.wikipedia.org/api/rest_v1/page/summary/{title}` |
| Full article HTML | `https://{lang}.wikipedia.org/api/rest_v1/page/mobile-html/{title}` |
| Search | `https://{lang}.wikipedia.org/w/api.php?action=query&list=search` |

## 📄 License

[MIT](LICENSE) — free to use, modify, and distribute.

---

> *"The world's knowledge, dressed for the occasion."*

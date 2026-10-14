# NACUAANC Website

The official website for the **North America Colleges and Universities Alumni Alliance, Northern California Chapter** (北美高校联盟北加州分会 / 北加高校联盟).

## Tech Stack
* **Framework**: Astro (v6)
* **Styling**: Tailwind CSS (v4)
* **Internationalization**: Custom lightweight i18n routing
* **Deployment**: Cloudflare Pages

## Features
* 🌐 **Full i18n Support**: Supports Simplified Chinese (`zh-CN`, default), English (`en`), and Traditional Chinese (`zh-TW`).
* 🎨 **Premium Aesthetic**: Responsive layout with modern dark-mode navy & slate palettes and custom typography.
* 👥 **Leadership Roster**: Highlights chapter leadership (President Michael Huo, Vice President Jerry Zhang).
* 🤝 **Community Focus**: Clear sections for events, activities, and contact channels (`contact@nacuaanc.org`, `michael@nacuaanc.org`).
* ❤️ **VI Support**: Visually references support by the **VI AI for Good Foundation**.

## File Structure
```
├── src/
│   ├── components/
│   │   ├── Header.astro         # Navbar with EN/简/繁 language toggle
│   │   ├── Footer.astro         # Footer with parent organization & support credits
│   │   └── pages/
│   │       └── HomeContent.astro# Shared responsive homepage layout
│   ├── i18n/
│   │   ├── locales.ts           # Supported language declarations
│   │   ├── ui.ts                # Translation dictionary (en, zh-CN, zh-TW)
│   │   └── utils.ts             # Routing and localized path generators
│   ├── layouts/
│   │   └── BaseLayout.astro     # Global layout, metadata, & SEO configurations
│   ├── pages/
│   │   ├── index.astro          # Root page (renders Simplified Chinese)
│   │   ├── en/                  # English pages
│   │   └── zh-TW/               # Traditional Chinese pages
│   └── styles/
│       └── global.css           # Global typography & Tailwind styles
├── public/
│   └── images/
│       └── logo.png             # Circular emblem logo badge
├── astro.config.mjs             # Astro configuration (targeting nacuaanc.org)
└── package.json                 # Build dependencies & scripts
```

## Local Development
Install dependencies:
```bash
npm install
```

Start dev server:
```bash
npm run dev
```

Build production static bundle:
```bash
npm run build
```

## Cloudflare Pages Deployment
1. Go to the **Cloudflare Dashboard** -> **Workers & Pages**.
2. Click **Create Application** -> **Pages** -> **Connect to Git**.
3. Choose the `viaiforgood/nacuaanc` repository.
4. Set the build settings:
   * **Framework Preset**: `Astro`
   * **Build Command**: `npm run build`
   * **Build Output Directory**: `dist`
5. Save and Deploy!

<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />

# Clara Veiga Portfolio

**A modern, minimalist portfolio for contemporary visual artist Clara Veiga.**

[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![Vite](https://img.shields.io/badge/Vite-6-646CFF?logo=vite&logoColor=white)](https://vitejs.dev)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com)

</div>

---

## Overview

This is a bilingual (English & Portuguese) single-page application (SPA) that showcases Clara Veiga's artistic works, exhibitions, press coverage, curriculum vitae, and a contact form for inquiries. It was originally created with [Google AI Studio](https://ai.studio/apps/a79fceeb-4d4d-4d08-b9a7-fdb024f9d4e3).

---

## Features

- **About** – Artist biography accompanied by a curated photo gallery.
- **Works** – A browsable grid of selected artworks with title, year, medium, and inquiry links.
- **Press** – A list of press items, articles, and interviews from international publications.
- **CV** – Full curriculum vitae including education, exhibitions, residencies, awards, and collections.
- **Contact** – Inquiry form with email, WhatsApp, and Instagram contact options.
- **Bilingual UI** – Seamless English ↔ Portuguese language switching via a context-based i18n system.
- **Smooth Animations** – Page transitions and hover effects powered by the Motion library.
- **Responsive Design** – Mobile-first layout that scales to tablet and desktop.
- **Error Boundary** – Graceful error handling with an in-page recovery option.

---

## Tech Stack

| Layer | Technology |
|---|---|
| UI Framework | [React 19](https://react.dev) |
| Language | [TypeScript 5.8](https://www.typescriptlang.org) |
| Build Tool | [Vite 6](https://vitejs.dev) |
| Routing | [React Router DOM 7](https://reactrouter.com) |
| Styling | [Tailwind CSS 4](https://tailwindcss.com) |
| Animations | [Motion 12](https://motion.dev) |
| Icons | [Lucide React](https://lucide.dev) |
| Server | [Express 4](https://expressjs.com) |
| Database | [better-sqlite3](https://github.com/WiseLibs/better-sqlite3) |
| AI Integration | [Google Gemini (`@google/genai`)](https://ai.google.dev) |

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org) (LTS recommended)
- A [Google Gemini API key](https://aistudio.google.com/app/apikey)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/mbergo/Portifolio.git
cd Portifolio

# 2. Install dependencies
npm install

# 3. Configure environment variables
cp .env.example .env.local
```

Open `.env.local` and set your API key:

```env
GEMINI_API_KEY=your_gemini_api_key_here
```

### Running in Development

```bash
npm run dev
```

The app will be available at [http://localhost:3000](http://localhost:3000) with Hot Module Replacement (HMR) enabled.

---

## Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start Vite dev server on port 3000 |
| `npm run build` | Build an optimized production bundle |
| `npm run preview` | Locally preview the production build |
| `npm run clean` | Remove the `dist` directory |
| `npm run lint` | Run TypeScript type-checking (`tsc --noEmit`) |

---

## Project Structure

```
Portifolio/
├── src/
│   ├── components/
│   │   └── Navbar.tsx          # Navigation bar with language switcher
│   ├── pages/
│   │   ├── About.tsx           # Artist bio + image gallery
│   │   ├── Works.tsx           # Artwork grid
│   │   ├── Press.tsx           # Press coverage list
│   │   ├── CV.tsx              # Curriculum vitae
│   │   └── Contact.tsx         # Inquiry / contact form
│   ├── App.tsx                 # Root router & layout
│   ├── main.tsx                # React entry point
│   ├── LanguageContext.tsx     # i18n context provider
│   ├── data.ts                 # Artworks, press, and CV data
│   └── index.css               # Tailwind + global styles
├── index.html                  # HTML shell
├── vite.config.ts              # Vite configuration
├── tsconfig.json               # TypeScript configuration
├── package.json                # Dependencies & scripts
├── metadata.json               # Project metadata
└── .env.example                # Environment variable template
```

---

## Deployment

The app can be deployed to any static hosting provider after running `npm run build`. The `dist/` folder contains the production-ready output.

It is also available as a hosted AI Studio app:  
[https://ai.studio/apps/a79fceeb-4d4d-4d08-b9a7-fdb024f9d4e3](https://ai.studio/apps/a79fceeb-4d4d-4d08-b9a7-fdb024f9d4e3)

---

## Contact

**Clara Veiga** – Contemporary Visual Artist  
📧 [clara.veiga@artist.com](mailto:clara.veiga@artist.com)  
📸 [@claraveiga.studio](https://instagram.com/claraveiga.studio)  
🌍 Based between Lisbon and São Paulo

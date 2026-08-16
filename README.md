# Your Portfolio

A simple portfolio site built with [Astro](https://astro.build). Astro is a
website framework where every page is its own file under `src/pages/`, and
that file's path becomes the page's URL. There's very little JavaScript
involved here on purpose — most files are just HTML with a small amount of
templating.

## Project structure

```
portfolio/
├── public/
│   ├── global.css       ← all the site's styling (colors, fonts, spacing)
│   └── resume.pdf        ← replace with your real resume (same filename!)
├── src/
│   ├── layouts/
│   │   └── Layout.astro  ← shared header/footer wrapper for every page
│   └── pages/
│       ├── index.astro           ← homepage ("/")
│       ├── resume.astro          ← "/resume"
│       ├── contact.astro         ← "/contact"
│       └── projects/
│           ├── project-1.astro   ← "/projects/project-1"
│           ├── project-2.astro   ← "/projects/project-2"
│           ├── project-3.astro   ← "/projects/project-3"
│           └── project-4.astro   ← "/projects/project-4"
├── astro.config.mjs
├── package.json
└── tsconfig.json
```

Anything in `public/` is served exactly as-is, like a normal folder of files
on a website — that's why `global.css` and `resume.pdf` live there.

Everything in `src/pages/` becomes a page automatically. If you ever want a
5th project, copy `project-4.astro`, rename it `project-5.astro`, edit the
text inside, and it's live at `/projects/project-5` — no extra setup needed.

## Running it on your computer

You'll need [Node.js](https://nodejs.org) installed (any recent version).
Then, from inside the `portfolio` folder:

```bash
npm install     # downloads Astro and its dependencies (only needed once)
npm run dev     # starts a local server, usually at http://localhost:4321
```

Leave that terminal window running and open the URL it prints in your
browser. Any time you save a file, the page refreshes automatically, so you
can edit and see the result immediately.

## What to edit

Every spot that needs your personal info is marked `EDIT THIS` or
`[Your Name]`. Search for those across the project and replace them:

1. **`src/layouts/Layout.astro`** — replace `[Your Name]` in the logo and footer.
2. **`src/pages/index.astro`** — your name, summary, and the 4 project titles/blurbs.
3. **`src/pages/projects/project-1.astro`** (and 2, 3, 4) — the details of each project.
4. **`src/pages/resume.astro`** — nothing to edit here; just replace `public/resume.pdf`
   with your real resume, keeping the exact filename `resume.pdf`.
5. **`src/pages/contact.astro`** — your real email and LinkedIn URL.

Colors and fonts all live in one place, `public/global.css`, at the top in a
section marked `TOKENS` — change the hex codes there to change the whole
site's color scheme.

## Deploying it so others can see it

Once you're happy with it, you can put it online for free with a host like
[Vercel](https://vercel.com), [Netlify](https://netlify.com), or
[GitHub Pages](https://pages.github.com). The general steps are:

1. Push this project to a GitHub repository.
2. Connect that repository to Vercel or Netlify (they auto-detect Astro).
3. They'll run `npm run build` for you and give you a live URL.

Astro has a short guide for each host here: https://docs.astro.build/en/guides/deploy/

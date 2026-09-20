# The Classical Pantheon

Complete source code for [The Classical Pantheon](https://thegreekandromangods.com), a searchable archive of Greek and Roman divinities.

## Open and edit in Visual Studio Code

Requirements:

- Node.js 22.13 or newer
- pnpm 11.19.0
- Git

```bash
git clone https://github.com/Bvdlaan/classical-pantheon.git
cd classical-pantheon
corepack enable
corepack prepare pnpm@11.19.0 --activate
pnpm install --frozen-lockfile
code .
```

Start the local development server:

```bash
pnpm dev
```

Create a production build:

```bash
pnpm build
```

## Repository structure

- `app/` — homepage, layout and deity routes
- `components/` — search, profiles, navigation and reusable interface components
- `db/` — deity content, image records and schema files
- `public/art/` — all website artwork
- `public/sitemap.xml` and `public/robots.txt` — SEO files
- `.github/workflows/deploy-pages.yml` — automatic GitHub Pages deployment

## GitHub Pages

Every push to `main` runs a static production build and publishes the result through GitHub Pages. In GitHub, open **Settings → Pages** and select **GitHub Actions** as the source if it is not selected automatically.

The workflow supports the standard project URL:

`https://bvdlaan.github.io/classical-pantheon/`

For a custom domain, add the domain in **Settings → Pages** and set the repository variable `GITHUB_PAGES_BASE_PATH` to `ROOT`.

## Content changes

The deity records are stored in `db/sheet-data.ts`. Associated artwork and attribution data are defined in `db/sculptures.ts`, with image files in `public/art/`.

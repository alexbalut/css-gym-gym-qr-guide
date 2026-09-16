# CSS Gym Gym QR Guide (unofficial demo)

**QR machine-instruction app skinned for a CSS Gym club demo.** Members scan a QR on a machine → bilingual (EN/FR) how-to guide. Staff manage machines, download QRs, print floor sheets, and review ROI insights.

> **Unofficial demo mockup for pitching only.** Not affiliated with CSS Gym or any parent company. Does **not** use official logo image assets — text wordmark only. Brand colors (`#00897B` / `#0A1614`) are approximate pitch tokens.

Seeded demo gym: **Coop Sportive Santé**. `/` is the **demo-ready member product UI** — not a marketing landing page.

Sibling (generic GymQR Guide): [gym-machine-qr-guide](https://github.com/alexbalut/gym-machine-qr-guide)

## Disclaimer

This repository is an **unofficial product demo**. CSS Gym® and related marks belong to their respective owners. Do not represent this app as an official CSS Gym product. No official logos are bundled.

## Quick start

```bash
cd css-gym-gym-qr-guide
cp .env.example .env
npm install
npx prisma db push
npm run seed
npm run dev
```

Or one-shot setup:

```bash
npm install && npm run setup && npm run dev
```

Open [http://localhost:3000](http://localhost:3000) — member gym home for **Coop Sportive Santé** (Machines / Workout / Progress / Scan).

## Demo credentials

| Field    | Value                    |
|----------|--------------------------|
| Email    | `admin@css-gym.demo`        |
| Password | `demo1234`             |
| Gym      | Coop Sportive Santé                |
| Slug     | `css-gym`           |

Seed creates **10 bilingual machines**, sample view counts, and a few open/resolved issues.

## Branding notes

- Surfaces use secondary `#0A1614` with primary accent **`#00897B`**
- Text wordmark **CSS Gym** — no trademarked logo files
- Tagline: “Coop governance gym”

## Key routes

| Route | Description |
|-------|-------------|
| `/` | Gym member home |
| `/scan` | Camera QR scan |
| `/q/[token]` | Machine guide |
| `/m/css-gym/[machineSlug]` | Friendly slug URL |
| `/admin/login` | Staff login |
| `/admin/insights` | Owner ROI dashboard |

## Caveats

- Auth is simple credential + JWT cookie — fine for demo; harden for production.
- SQLite at `prisma/dev.db` — don’t commit it.
- Member workout/progress is browser localStorage only (`css-gym-workout:v1:<slug>`).
- Unofficial branding — do not ship as an official CSS Gym app.

## Photo credits

Demo photos under `public/machines/` are from Unsplash — see [CREDITS.md](./CREDITS.md). Not official CSS Gym assets.

## License / affiliation

This repository is an **unofficial product demo mockup** for pitch purposes. CSS Gym® and related marks belong to their respective owners. Do not represent this app as an official CSS Gym product.

## Repo

https://github.com/alexbalut/css-gym-gym-qr-guide

# BICA TYPING STUDIO

A typing tutor, an arcade and a classroom management system for **BICA Computer Training Centre**. Runs on one lab PC, needs no internet, and keeps every student's measured history in a single file you own.

## Features
- Learn: seven levels and fifty gated lessons
- Practice: timed and fixed-length drills, custom passages and examination mode
- Arcade: twelve typing games
- Challenge: daily and weekly challenges, class leaderboards and personal bests
- Progress: speed and accuracy history, weak-key analysis, achievements and certificates
- Faculty: classes, assignments, tests, reports (CSV + PDF) and certificates
- Admin: users, settings, mastery policy, audit log and backups

## Quick start

Requires Node.js 20 LTS or newer.

```bash
npm ci
npm run seed
npm start
```

Open http://localhost:8080.

For demo accounts, run `npm run seed:demo`. Demo accounts use the password `BicaDemo2026!`; remove demo data before real student use.

## Architecture
- Server: Node.js, Express and SQLite
- Client: native JavaScript ES modules and CSS
- Dependencies: express and better-sqlite3

## Important deployment note
This project currently uses a persistent local SQLite database and a conventional Express server. It is **not a static-only site** and cannot be deployed to Vercel by simply importing the frontend. A cloud deployment needs a compatible persistent backend and database migration/hosting plan.

See `docs/DEPLOYMENT.md`, `docs/ARCHITECTURE.md` and `docs/SECURITY.md` in the complete source package.

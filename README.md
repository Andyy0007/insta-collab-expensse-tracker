<div align="center">

# CollabLedger

### A simpler way for Instagram creators to manage brand collaborations.

Track brand deals, deliverables, deadlines, and payments in one place—so you can spend less time organising spreadsheets and chats, and more time creating.

[**Open the Live App**](https://andyy0007.github.io/insta-collab-expensse-tracker/) · [View Source Code](https://github.com/Andyy0007/insta-collab-expensse-tracker)

![Status](https://img.shields.io/badge/status-live-brightgreen)
![Frontend](https://img.shields.io/badge/frontend-HTML%20%7C%20CSS%20%7C%20JavaScript-blue)
![Backend](https://img.shields.io/badge/backend-Supabase-3ECF8E)
![Database](https://img.shields.io/badge/database-PostgreSQL-336791)
![Hosting](https://img.shields.io/badge/hosting-GitHub%20Pages-222222)

</div>

---

## The idea

The idea came while travelling. I started thinking about a common challenge for Instagram influencers and content creators: as brand collaborations increase, details get scattered across DMs, notes, and spreadsheets. Remembering what needs to be delivered, how much a brand owes, and when a payment is due can quickly become difficult.

I built **CollabLedger** to bring those details together in one simple workspace.

## Features

- **Collaboration management** — organise brands, contacts, deliverables, deal values, and booking dates.
- **Deadline tracking** — keep deliverable and payment due dates visible.
- **Payment tracking** — record payments and monitor outstanding balances.
- **Collaboration status** — follow deals from Confirmed and In progress through Delivered and Completed.
- **Request review** — keep collaboration requests organised with a review status.
- **At-a-glance overview** — quickly review booked value, received payments, and outstanding amounts.
- **Search and filters** — find collaborations without digging through messages.
- **Authentication and persistent storage** — sign in and store workspace data using Supabase.
- **Access controls** — use PostgreSQL Row Level Security (RLS) policies to restrict access to workspace data.

## Tech stack

| Layer | Technology |
| --- | --- |
| Frontend | HTML, CSS, JavaScript |
| Authentication | Supabase Auth |
| Database | Supabase / PostgreSQL |
| Data access security | PostgreSQL Row Level Security (RLS) |
| Hosting | GitHub Pages |
| Version control | Git and GitHub |

## Architecture overview

```text
Creator
  │
  ▼
Web app (HTML, CSS, JavaScript)
  │
  ├── Sign in / Sign up ─────────► Supabase Auth
  │
  └── Authenticated data requests ► PostgreSQL
                                      │
                                      └── RLS policies protect workspace data

Deployment: GitHub repository ─────► GitHub Pages
```

## Getting started

### Use the live app

Open the [live application](https://andyy0007.github.io/insta-collab-expensse-tracker/) and create an account or sign in.

### Run locally

1. Clone the repository:
   ```bash
   git clone https://github.com/Andyy0007/insta-collab-expensse-tracker.git
   ```
2. Open the project folder.
3. Open `index.html` in a modern browser.

The frontend is a static HTML/CSS/JavaScript app. The deployed version uses the configured Supabase project for authentication and database operations.

## Security notes

- Database access is governed by Supabase authentication and Row Level Security policies.
- The browser uses a Supabase publishable key; **never place a Supabase service-role key, database password, or other secret in frontend code**.
- Review RLS policies whenever adding tables or changing data access.
- Use your own account when testing the live application; do not share login credentials.

## Roadmap

Potential improvements as the project evolves:

- Improve mobile usability and accessibility.
- Add exportable reports for collaborations and payments.
- Add optional reminders for deadlines and overdue payments.
- Explore safe, consent-based integrations for importing collaboration details.
- Expand automated tests for authentication, workspace isolation, and database permissions.

## Feedback

Feedback and feature ideas are welcome—especially from creators and managers who handle brand collaborations regularly.

- **Live app:** https://andyy0007.github.io/insta-collab-expensse-tracker/
- **Repository:** https://github.com/Andyy0007/insta-collab-expensse-tracker

---

<div align="center">

Built to solve a small, real-world creator workflow problem. 🚀

</div>

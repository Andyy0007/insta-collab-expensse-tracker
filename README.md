# Insta Collab Expense Tracker

A responsive, browser-based MVP for influencers and managers to review brand collaborations, track reel deliverables and deadlines, monitor payments, and understand revenue.

## Run locally

Open `index.html` in a modern browser. No build tools or dependencies are required.

## MVP features

- Collaboration tracking: brand, deliverable, booking date, deadline, value, and status.
- Approval workflow: new collaborations can be held for review before being added.
- Severity: Critical, Warning, and Normal based on deadlines and outstanding payments.
- Payment tracking: record partial payments and calculate the outstanding amount.
- Revenue summary: total booked value, received, outstanding, and monthly revenue.
- Search and status filters.
- Browser local storage for demo persistence.

## Current limitations

This is a frontend prototype. It uses sample data and local browser storage; it does not yet include authentication, shared workspaces, live Gmail/OAuth integration, a production database, or background email/push notifications. The Gmail action is a placeholder and does not access an inbox.

## Recommended next steps

1. Add authentication, workspace membership, and a PostgreSQL database (for example Supabase) with row-level security.
2. Implement backend APIs and role-based access for creators, managers, and finance users.
3. Add Google OAuth and Gmail API ingestion. Incoming messages should create drafts in the approval inbox and never be auto-approved.
4. Add scheduled reminders for deadlines and contract-based payment due dates.
5. Add audit logs, duplicate-message handling, token encryption, and tenant-isolation tests.

## Security note

Never collect Gmail passwords. Use OAuth with minimum required scopes, store tokens server-side encrypted, and ask for explicit consent before connecting an inbox.

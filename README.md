# CRM — Customer Registry

![Node.js](https://img.shields.io/badge/Node.js-3b3a36?style=flat-square) ![Express](https://img.shields.io/badge/Express-3b3a36?style=flat-square) ![MS SQL Server](https://img.shields.io/badge/MS%20SQL%20Server-3b3a36?style=flat-square) ![JWT](https://img.shields.io/badge/JWT-3b3a36?style=flat-square) ![node-cron](https://img.shields.io/badge/node--cron-3b3a36?style=flat-square) ![Nodemailer](https://img.shields.io/badge/Nodemailer-3b3a36?style=flat-square)


A login-protected web app for a sales team: customers, contact history and call logs in Microsoft SQL Server.

## Features
- Customers with search and filters; per-customer **call log**
- Login with **JWT stored in an httpOnly cookie**, bcrypt passwords, **rate-limited** auth endpoint
- CLI script to create the first admin and new users
- Scheduled jobs (node-cron) with email notifications
- CSV import of existing customer lists
- Runs against local SQL Server, Docker or Azure SQL

```mermaid
flowchart LR
  B[Browser<br/>login · customers · calls] --> E[Express API]
  E --> A[auth middleware<br/>JWT cookie]
  E --> DB[(SQL Server<br/>Users · Customers · CallLogs)]
  CRON[node-cron] --> MAIL[Email digest]
```

---

> **Showcase repository.** This repo presents the project — what it does, how it is built and what it looks like.
> The full source code is private. For a walkthrough or a code sample, get in touch.

**Tural Zamanlı** · Data & Automation Developer · [Portfolio](https://dicapso.github.io) · [GitHub](https://github.com/Dicapso)

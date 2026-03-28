# Leomars Properties ERP Dashboard

A production-grade **real estate portfolio management dashboard** built with React, designed for high-net-worth investors managing multi-region property portfolios across the UK and Dubai.

> **Built entirely with [Claude Code](https://claude.ai/code) by Anthropic** — from architecture to deployment.

---

## Overview

Leomars Properties ERP is a single-page application that consolidates residential and commercial property data into a unified, real-time dashboard. It supports bilingual interfaces (English / Chinese), live currency conversion, lease lifecycle tracking, tenant management, legal case management, and Excel export — all running client-side with zero backend dependencies.

---

## Key Features

### Portfolio Dashboard
- **KPI Cards** — Total properties, regional breakdown (UK / Dubai), annual rent, portfolio value in USD, average monthly rent, total deposits, and lease value
- **Stacked Bar Charts** — Annual rent trends per region with auto-calculated CAGR% overlay (Recharts)
- **Animated Counters** — Smooth count-up transitions on all monetary figures
- **Lease Expiry Timeline** — Visual progress bars with days-remaining alerts

### Property Management
- **CRUD Operations** — Add, edit, and delete properties with full form validation
- **Multi-Year Rent Schedules** — Per-payment breakdowns with configurable payment frequencies (monthly, quarterly, annual)
- **Tenant Lifecycle** — Track current tenants, end tenancies, onboard new tenants with lease renewal workflows
- **Future Tenancy Planning** — Pre-register upcoming tenants before current lease expiry
- **Commercial Multi-Unit Support** — Buildings with individual shop/unit management (separate tenants, rents, contracts per unit)

### Financial Intelligence
- **Live Exchange Rates** — USD/GBP and USD/AED fetched from 6 redundant API sources with automatic failover
- **Dual Currency Display** — Every monetary value shown in local currency + USD equivalent
- **CNY Support** — Chinese Yuan conversion for bilingual users

### Legal & Compliance
- **Lawyer Contact Management** — Dedicated view with one-tap call, email, website, and maps integration
- **Legal Case Tracker** — Full CRUD for legal cases linked to specific properties with status workflow (Open / In Progress / Pending / Closed)

### Data & Export
- **Excel Export** — Download all properties, by region, or individual property as formatted `.xlsx` files (SheetJS)
- **Local Persistence** — All data saved to `localStorage` with versioned schema migration
- **Backup & Restore** — Automatic backups on every save with one-click restore

### UX & Design
- **Dark / Light Mode** — System-aware theme with manual toggle, persisted preference
- **Bilingual (EN / CN)** — Complete Chinese translation with locale-aware formatting
- **Responsive Design** — Mobile-first layout, optimized for phones through ultrawide displays
- **Framer Motion Animations** — Page transitions, card hover effects, modal animations
- **Fintech-Inspired Palette** — Bloomberg / Revolut inspired color system with distinct property color coding

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **Framework** | React 19 |
| **Build Tool** | Vite 7 |
| **Styling** | Tailwind CSS 4 |
| **Charts** | Recharts 3 |
| **Animations** | Framer Motion 12 |
| **Icons** | Lucide React |
| **Excel Export** | SheetJS (xlsx) |
| **Deployment** | Vercel |

---

## Getting Started

### Prerequisites
- Node.js 18+
- npm or yarn

### Installation

```bash
git clone https://github.com/amiradnanptcl-hue/Leomars-Properties-ERP-Dashboard.git
cd Leomars-Properties-ERP-Dashboard
npm install
```

### Development

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Production Build

```bash
npm run build
npm run preview
```

---

## Project Structure

```
src/
  App.jsx          # Main application (single-file architecture)
  main.jsx         # React entry point
  index.css        # Tailwind + custom theme styles
  assets/          # Static assets
public/
  logo.png         # Application logo
index.html         # HTML entry point
vite.config.js     # Vite configuration
```

### Architecture Decision: Single-File SPA

The entire application lives in `App.jsx` (~4,400 lines). This is a deliberate architectural choice for a data-heavy dashboard with tightly coupled components that share state, translations, and formatting utilities. The single-file approach eliminates prop-drilling complexity and keeps the codebase navigable with IDE search.

---

## Deployment

### Vercel (Recommended)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/amiradnanptcl-hue/Leomars-Properties-ERP-Dashboard)

Or via CLI:

```bash
npm i -g vercel
vercel
```

---

## Demo Data

This repository contains **demonstration data only** — all property names, tenant details, addresses, and financial figures are fictional. The dashboard is designed to showcase the application's capabilities for portfolio management at scale.

| Region | Properties | Types |
|--------|-----------|-------|
| UK | 6 | 5 Residential, 1 Commercial |
| Dubai | 9 | 3 Residential, 6 Commercial (including multi-unit buildings) |

---

## License

MIT

---

<p align="center">
  <strong>Designed & Developed by Syed Amir Adnan</strong><br/>
  Queen's Business School, Belfast, Northern Ireland, UK<br/><br/>
  <em>Built with <a href="https://claude.ai/code">Claude Code</a> by Anthropic</em>
</p>

# JUST TRACK SPENDING

Your spending, decoded in your browser. No sign-up. No cloud. No fuss.

**How it works:**

1. `Export your bank / credit card statements as .csv or .xls`
2. `Upload them to the app`
3. `See exactly where your money goes`

[![just-track-spending screenshot](https://github.com/user-attachments/assets/db0e5315-e3ec-41ef-abef-81ad49eed25a)](https://just-track-spending.vercel.app)

**→ [Try it live](https://just-track-spending.vercel.app)**

---

## What is this?

A single HTML file that turns your messy bank exports into a clean spending breakdown — no accounts, no servers, no subscriptions.

Open it, drop in your files, and instantly see where your money actually goes.

## Why this beats a budgeting app

| Budgeting apps | Just Track Spending |
|---|---|
| Requires bank login / OAuth | **Just a CSV upload** |
| Your transactions go to their servers | **Everything stays in your browser** |
| Monthly subscription | **Free forever** |
| Onboarding flows, dashboards, nudges | **Open, upload, done** |
| Breaks when they change their API | **Static file, works offline** |

No vendor lock-in. No privacy trade-offs. No dark patterns.

## Features

- 🔒 **Stays local** — All processing happens in your browser. Your files never leave your machine.
- 🏷️ **Auto-categorises** — Transactions are automatically sorted into categories based on merchant names.
- 📁 **Multi-file support** — Upload statements from multiple banks and cards at once.
- ⚡ **No setup** — No install, no signup, no config. Just open and go.

## Quick Start

```bash
git clone https://github.com/xianxlb/just-track-spending.git
cd just-track-spending
open index.html          # or just drag the file into your browser
```

Or skip cloning entirely — **[use the hosted version](https://just-track-spending.vercel.app)**.

## Supported formats

Most banks let you export transaction history as a `.csv` or `.xls` file. Look for "Download transactions" or "Export statement" in your bank's app or website.

Works with exports from DBS and UOB but feel free to test out other banks.

## Privacy

**Your data never leaves your computer.**

- Transaction files are processed entirely in-browser
- Nothing is uploaded to any server
- No analytics on your financial data
- The only network request is loading the page itself

## Contributing

PRs welcome. If your bank's CSV format isn't parsing correctly, open an issue with a sample (anonymised) export and the column headers.

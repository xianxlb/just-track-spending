# just-track-spending

Track your spending without the fuss. Upload bank statements, get instant insights.

- **Stays local** — All processing happens in your browser. Your data never leaves your computer.
- **Auto-categorises** — Transactions are automatically sorted into categories based on merchant names.
- **No signup required** — Open the app, upload a CSV or Excel file, and start exploring.

## Quick Start

1. **Clone the repo**
   ```bash
   git clone https://github.com/xianxlb/just-track-spending.git
   cd just-track-spending
   ```

2. **Open in your browser**
   ```bash
   open index.html
   ```
   Or simply drag `index.html` into your browser window.

3. **Upload your bank statement**
   - Export a CSV or Excel file from your bank (see "Supported Banks" below)
   - Click "Upload" and select the file
   - Wait a few seconds for categorisation to complete
   - Explore your spending patterns

## What You Get

**Monthly View** — See how much you spent each month at a glance. Spot your highest-spending months and trends over time.

**Category Breakdown** — Understand where your money goes. View top spending categories as a visual breakdown with percentages.

**Recurring Charges** — Automatically detects subscriptions and recurring bills. Shows monthly and annual costs so you know exactly what you're committed to.

## Supported Banks

| Bank | Format | Notes |
|------|--------|-------|
| DBS (Credit Card) | CSV | Export "Transaction History" |
| DBS (Bank Account) | CSV | Export "Transaction History" |
| UOB (Debit Card) | Excel | Export statement directly |
| UOB (One Account) | Excel | Export statement directly |

**Using a different bank?** The parser supports DBS and UOB formats, but you're welcome to submit a PR to add your bank, or modify the keywords in the code to match your bank's transaction format.

## How It Works

The app parses your bank statement and does three things:

1. **Categorises transactions** — Each merchant name is matched against a set of keywords (e.g., "GRAB", "SHOPEE", "RAFFLES MEDICAL"). Matches are grouped into categories like Transport, Shopping, Health, etc.

2. **Detects recurring charges** — Looks for transactions that appear consistently across 2+ months and belong to subscription or bill categories. Useful for spotting monthly costs you might have forgotten about.

3. **Summarises your spending** — Generates monthly totals, category breakdowns, and highlights your highest spending months.

All of this happens in your browser—no server requests, no data collection. Upload your file, explore your data, close the tab when you're done.

## Customisation (Optional)

Want to adjust categories or keywords? The category definitions and merchant matching logic are in `index.html` around lines 980–1050.

For example, to add a new category or add keywords that match your local merchants:

```javascript
{ name: 'YourCategory', color: 'var(--cat-yourcat)', keywords: [
  'MERCHANT_NAME_1', 'MERCHANT_NAME_2',
]},
```

Then add the corresponding CSS variable in the `:root` section:

```css
--cat-yourcat: #YOUR_COLOR;
```

No build step required—just refresh your browser.

## Privacy & Limitations

- **Local processing only** — Files are parsed in your browser using the [SheetJS library](https://sheetjs.com/). Nothing is sent to a server.
- **Works best with 2+ months of data** — The recurring charge detector needs at least two months of transactions to identify patterns.
- **Keyword matching may misclassify** — If a merchant name doesn't match our keywords, it'll be marked "Uncategorized". You can manually recategorise or update the keywords.
- **Browser limitations** — Very large statements (10,000+ transactions) may slow down the app slightly.

## Contributing

Found a bug? Want to add support for another bank? Have a better set of keywords for your region? Pull requests are welcome.

For new bank formats, check out the CSV and XLS parsers in `index.html` (lines 1069–1250) to see how to add your format.

---

Made with ❤️ for people who just want to understand their spending without the fuss.

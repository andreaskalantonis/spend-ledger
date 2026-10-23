# Spend Ledger

Spend Ledger turns bank and credit card statements into a clear picture of where money goes, supplier by supplier and month by month. You upload the PDF or CSV statements your bank already gives you. It reads every transaction and checks it against the bank's own running balance. It then works out who you paid and what kind of spending it was, and builds a history you can plan against.

**Try it:** https://andreaskalantonis.github.io/spend-ledger/

## What it does

- Reads Revolut PDF statements (monthly and multi-currency), American Express PDF statements, and CSV exports from Revolut, Monzo, Amex and most other banks.
- Checks every row against the statement's running balance or printed total, and skips transactions already imported from an overlapping file.
- Matches each payment to a supplier and one of 17 categories. It uses built-in rules plus rules you write yourself.
- Shows spending by month or for a whole year, a register of every supplier, cash flow and savings rate, trips found from foreign-currency spending, and how concentrated spending is across your top suppliers.
- Covers budgets, a month-end forecast, regular payments with alerts for price changes, and a one-page monthly or yearly summary.
- Keeps the original statements, so any transaction opens the page it came from.

## Privacy and safety

- **Your statements stay on your device.** Everything runs in your browser. Statements are never uploaded, and there is no server, account or database. The PDF reader (pdf.js) and fonts load from public code libraries and never see your files.
- **Use your own computer.** Imported data is saved in this browser profile. On a shared computer, remove it afterwards with *Your data → Delete my ledger*.
- **A prototype, not financial advice.** Categories, totals and forecasts are automated and can be wrong.
- **Not affiliated with any bank.** Revolut, American Express and Monzo are named only to describe the statement formats it reads.
- This repository contains no personal data. The app starts empty.

## How it was built

I built Spend Ledger as a product owner directing Claude, Anthropic's AI model, which did the engineering. I set the brief and the order of features. I tested every change against my own statements and decided what counts as correct. More detail is in the app under *About this project*.

It is a single HTML file with plain HTML, CSS and JavaScript, and pdf.js for reading PDFs.

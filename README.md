# Expense calculator

A single HTML page for adding expenses and seeing the total. Open `index.html` in a browser. There is no install, server, or account.

## What you can do

- Add an expense with a name, amount, category, and date
- See the running total and how many expenses you have entered
- Set an optional budget and see what is left, or how far over you are
- Filter by category once two categories have entries
- Remove one expense, or clear the whole ledger
- Switch currency among USD, EUR, GBP, INR, JPY, CAD, and AUD

## How amounts are stored

Each amount is saved as a whole number of minor units (cents for dollars, yen for JPY) and formatted only when it is shown. Totals are a sum of those integers, so `0.10 + 0.20` stays `0.30`.

Changing the currency does not convert existing amounts. `10.00` stays `10.00` in the new currency.

Entries stay in this browser under the local storage key `expense-ledger-v1`. Nothing is uploaded.

## Amount format

- `19.99` or `19,99` for currencies that use decimals
- `1,000` or `1,000.50` when you want thousands separators
- Whole amounts only for yen, such as `1000` or `1,000`

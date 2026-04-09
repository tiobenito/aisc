# Expense Categorizer

**Type:** Skill
**Trigger:** "categorize these expenses" or paste a CSV/list of transactions
**Time saved:** ~30 minutes/month

## What it does

Takes a messy list of expenses -- pasted from a bank statement, CSV export, or just a list you typed out -- and categorizes each one, standardizes the formatting, and produces a clean summary with totals by category.

## How it works

1. Reads the input (pasted text, CSV file, or a file path)
2. Identifies each transaction: date, amount, vendor/description
3. Assigns a category to each one (meals, travel, software, office supplies, etc.)
4. Standardizes date formats and vendor names
5. Outputs a clean table sorted by category
6. Adds a summary section with totals per category and overall spend

## Example output

```
| Date       | Vendor          | Category    | Amount  |
|------------|-----------------|-------------|---------|
| 2026-04-01 | Uber            | Travel      | $24.50  |
| 2026-04-01 | Notion          | Software    | $10.00  |
| 2026-04-02 | Blue Bottle     | Meals       | $6.75   |
| 2026-04-03 | Amazon (cables) | Office      | $18.99  |
| 2026-04-03 | Chipotle        | Meals       | $14.20  |

Summary:
- Meals: $20.95 (2 transactions)
- Travel: $24.50 (1 transaction)
- Software: $10.00 (1 transaction)
- Office: $18.99 (1 transaction)
- Total: $74.44
```

## Where it lives

`~/.claude/skills/expense-categorizer/SKILL.md`

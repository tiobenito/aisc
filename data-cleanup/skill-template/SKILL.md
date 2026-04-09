---
name: clean-data
description: "Clean and standardize messy data files. Use when user says 'clean this data', 'fix this spreadsheet', 'process this CSV', 'clean up this file', 'standardize this data', or provides a messy CSV/data file to clean."
allowed-tools: ["Read", "Write", "Edit", "Bash", "Glob", "Grep"]
---

# Data Cleanup & Report

Take a messy data file and produce a cleaned version plus a summary report.

## Workflow

1. **Read the input file.** Accept CSV, TSV, or pasted tabular data. Identify the columns, data types, and row count.

2. **Diagnose the mess.** Scan for:
   - Inconsistent date formats
   - Duplicate or near-duplicate rows
   - Inconsistent category labels / spelling variants
   - Missing values
   - Formatting inconsistencies (currency symbols, number formats, casing)
   - Typos in repeated fields (names, vendors, categories)

3. **Present the diagnostic.** Show the user a summary of what you found:
   - "I found X date formats, Y potential duplicates, Z missing values..."
   - Ask: "Want me to fix all of this, or do you want to adjust anything first?"

4. **Clean and standardize.** After confirmation:
   - Standardize dates to YYYY-MM-DD
   - Normalize categories to canonical versions
   - Remove duplicates (keep first occurrence, note which were removed)
   - Fill missing values where inferable, flag where not
   - Standardize number formats (strip symbols, consistent decimals)
   - Correct typos in repeated fields
   - Add a "Flags" column noting any changes made to each row

5. **Save the cleaned file** as `cleaned-[original-filename]` in the same directory as the input.

6. **Generate a summary report** with:
   - Overview: row count, date range, key totals
   - Breakdowns by main categories (with totals and percentages)
   - Top entries in key fields (top vendors, top categories, etc.)
   - Anomalies and flags (large outliers, remaining unknowns, items needing review)
   - Cleanup summary (what was fixed and how many of each)

7. **Save the report** as `[original-filename]-report.md` in the same directory.

## Tips

- Always show the diagnostic before cleaning. Don't silently change data.
- When in doubt about a category mapping, ask the user.
- For duplicates, keep the row with more complete data.
- The Flags column is important -- it creates an audit trail so the user can verify changes.
- This skill works on any tabular data, not just expenses. Adapt the report sections to match the data domain (contacts, inventory, survey results, etc.).

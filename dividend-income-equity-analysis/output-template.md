# Output Template

## 1. Executive Summary

### 1A. Key Metrics at a Glance

If rich visualization or card-style layout is available, render these as four metric cards. If not, use this one-row table.

| TTM Net Yield | Normalized Net Yield | Score / Grade | Portfolio Role |
|---:|---:|---:|---|
| | | | |

### 1B. Secondary Summary

- Company:
- Ticker:
- Exchange:
- As-of date:
- Price used:
- TTM gross yield:
- TTM net yield:
- Normalized net yield:
- Withholding rate:
- Withholding basis:
- Broker-observed withholding: Yes / No / Unknown
- Initial view:

## 2. Dividend Snapshot

One-sentence takeaway before the table:

| Metric | Value | Comment |
|---|---:|---|
| TTM DPS | | |
| TTM gross yield | | |
| TTM net yield | | |
| Normalized DPS | | |
| Normalized net yield | | |
| Five-year DPS range | | |
| Latest DPS YoY | | |
| Dividend type | | |
| Coverage status | | |

## 3. Standard Charts or Text Fallback

Follow `visual-output-rules.md`.

If rich visualization is available, render these three charts:

1. DPS Structure Chart.
2. Yield Ladder.
3. Coverage Chart.

If rich visualization is unavailable, provide the plain-text fallback:

- DPS path:
- Yield stack:
- Coverage labels:

Charts are the communication layer. Tables below are the data record.

## 4. Company and Listing Structure

One-sentence takeaway before details.

Describe domicile, issuer type, listing venue, dividend currency, reporting currency, official share count from filings, and whether the security is an H-share, red-chip, ADR, REIT, fund, trust, or ordinary share.

## 5. Dividend Treatment

One-sentence takeaway before details.

Read `withholding-notes.md` and apply the priority rule. Explain the basis for the withholding assumption and any uncertainty.

If withholding is 0%, state once: "Withholding 0% — gross equals net." Do not repeat Withholding / Net DPS / Net Yield columns in every historical row.

## 6. Dividend Trajectory and Yearly Yield

One-sentence takeaway before the table.

Use `visual-output-rules.md`. If the full table would exceed seven columns, split into DPS Structure and Yield / Coverage tables.

### 6A. Per-share DPS Structure

| Fiscal Year | Total DPS | Base DPS | Special / Variable DPS | DPS YoY | Quality Tag | Notes |
|---|---:|---:|---:|---:|---|---|

### 6B. Yield and Coverage

| Fiscal Year | Yield at Current Price | Yield at Year Price | Payout Ratio | FCF / Dividend | Coverage Label | Comment |
|---|---:|---:|---:|---:|---|---|

Add a short Dividend Pattern paragraph after the tables.

## 7. Cash-Flow Coverage Bridge

One-sentence takeaway before the tables.

If the bridge exceeds seven columns, split into cash generation and cash return / funding tables.

### 7A. Cash Generation

| Fiscal Year | Net Income | Operating Cash Flow | Capex | Free Cash Flow | FCF Quality | Comment |
|---|---:|---:|---:|---:|---|---|

### 7B. Cash Return and Funding

| Fiscal Year | Cash Dividends | Buybacks | Share Issuance | Net Debt Change | FCF / Dividend | Funding Source |
|---|---:|---:|---:|---:|---:|---|

Explain whether dividends were funded by operating free cash flow, cash balance, asset sales, debt, equity issuance, or mixed sources. If FCF is estimated as operating cash flow minus capex, label it as estimated.

## 8. Management Capital Allocation

One-sentence takeaway before details.

Summarize dividend policy, buyback policy, leverage target, reinvestment priority, acquisition policy, share issuance, ATM programs, and whether equity issuance coincides with elevated payout.

## 9. Buyback Quality

One-sentence takeaway before details.

Assess share-count change, dilution, valuation discipline, whether buybacks are debt-funded, and whether buybacks are offset by share issuance.

## 10. Three-Year Dividend Runway

One-sentence takeaway before the table.

| Fiscal Year | Scenario | DPS | Net Yield at Current Price | Estimated FCF | Dividend Cash Cost | FCF / Dividend |
|---|---|---:|---:|---:|---:|---:|

If more detail is needed, add this assumptions table:

| Fiscal Year | Scenario | Balance Sheet Impact | Key Assumptions |
|---|---|---|---|

Separate TTM yield from normalized and scenario yield.

## 11. Dividend Trap Checklist

One-sentence takeaway before the table.

List each red flag and the evidence for or against it. Include equity issuance or ATM program concurrent with elevated payout when relevant.

## 12. Visual Summary

Add a compact visual summary:

- DPS path:
- Yield normalization: TTM vs normalized vs bear/base/bull.
- Coverage labels by year: Strong / Adequate / Weak.

If charts were already rendered, keep this section brief and use it as a written recap.

## 13. Score, Required Ratings, and Portfolio Role

One-sentence takeaway before the score table.

Use `scoring.md` and show points by module.

Always output the six required ratings:

- Dividend Quality: High / Medium / Low
- Dividend Safety: Strong / Acceptable / Weak / Unclear
- Withholding Efficiency: High / Medium / Low
- Buyback Quality: Good / Neutral / Poor / Not Applicable
- Three-Year Dividend Outlook: Grow / Stable / Decline / High Uncertainty
- Portfolio Role: Core income / Cyclical income / Opportunistic / Watchlist / Avoid

## 14. Sources and Data Quality

List official filings, announcements, broker records, and third-party cross-checks used. State any missing data or fallback calculations clearly.

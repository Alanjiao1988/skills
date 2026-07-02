# Dividend Income Equity Analysis Skill

This skill is a research workflow for analyzing dividend-paying public companies.

## Scope

The workflow reviews public filings, dividend history, shareholder-return policy, buybacks, financial capacity, withholding treatment, broker-observed dividend cash flow, and future dividend sustainability.

## Investor Assumption

Default assumption: HK resident individual using a normal brokerage account.

## Source Priority

1. Official company filings and annual reports.
2. Exchange announcements and regulator filings.
3. Company investor-relations materials.
4. Earnings-call transcripts.
5. Broker cash statement or activity report when the user provides it.
6. Third-party data only as cross-checks.

## Withholding Priority Rule

Dividend tax treatment must not rely only on listing venue or legal domicile.

Use this order when estimating net dividend yield:

1. Actual broker cash statement for the same investor and same holding channel.
2. Company dividend announcement and tax note.
3. Legal domicile, listing structure, and issuer type.
4. Market-level default assumption.

For mainland-controlled HK-listed issuers, do not assume zero withholding only because the stock trades in Hong Kong. Check legal domicile, dividend announcement wording, HKSCC or custodian treatment, and broker activity.

If the user has observed broker withholding for a stock, use the observed rate in future calculations unless there is later evidence of a change. Current observed-withholding examples from user records include 0941.HK China Mobile and 1919.HK COSCO SHIPPING Holdings.

## Required Sections

1. Company and listing classification.
2. Dividend tax treatment and broker-observed withholding status.
3. Current gross and net dividend yield.
4. Five-year dividend history.
5. Management capital-allocation attitude.
6. Buyback quality.
7. Financial capacity and dividend coverage.
8. Three-year dividend outlook.
9. Risk and dividend-trap checklist.
10. Final research rating.

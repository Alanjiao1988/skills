# skills-dividend-for-HK

A claude.ai Skill for dividend-income stock analysis from the perspective of an HK resident individual using a normal brokerage account.

## Skill Directory

Upload or package this directory as the skill:

```text
dividend-income-equity-analysis/
```

Expected in-skill structure:

```text
dividend-income-equity-analysis/
├── SKILL.md
├── workflow.md
├── withholding-notes.md
├── scoring.md
├── output-template.md
├── schema.json
└── examples/
    └── example-output-skeleton.md
```

## Focus

The skill focuses on:

- Gross and net dividend yield.
- Five-year dividend history.
- Withholding treatment and broker-observed dividend cash flow.
- Management capital allocation and buyback quality.
- Financial coverage and dividend safety.
- Three-year dividend forecast.
- Dividend-trap detection.

## Key Rule

Broker-observed withholding has priority over theoretical classification. If a broker cash statement shows withholding for a stock, future net-yield calculations should use the observed rate unless later evidence shows a change.

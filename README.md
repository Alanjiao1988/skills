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
├── visual-output-rules.md
├── buy-zone.md
├── output-template.md
├── schema.json
└── examples/
    └── example-output-skeleton.md
```

## ChatGPT Custom GPT Support

ChatGPT-specific files are kept outside the skill directory:

```text
gpt-header.md
build-gpt-instructions.sh
chatgpt-custom-gpt-instructions.md
```

Use `gpt-header.md` as the Custom GPT instruction header and upload the canonical skill files as Knowledge.

To generate a single pasteable Custom GPT instruction file:

```bash
bash build-gpt-instructions.sh
```

Do not hand-copy skill rules into the ChatGPT file; update canonical modules under `dividend-income-equity-analysis/` and regenerate.

## Focus

The skill focuses on:

- Gross and net dividend yield.
- TTM yield versus normalized yield.
- Five-year dividend history and dividend trajectory.
- Withholding treatment and broker-observed dividend cash flow.
- Payment-in-lieu versus true dividend cash-line identification.
- Management capital allocation and buyback quality.
- Financial coverage and dividend safety.
- Three-year dividend forecast and dividend runway.
- Expected buy zone using normalized net DPS, required net yield, historical price levels, and historical yield bands.
- Dividend-trap detection.

## Key Rules

- Broker-observed withholding has priority over theoretical classification only when the broker record is a true dividend line.
- Payment-in-lieu records do not constitute withholding-rate evidence.
- TTM yield must be separated from normalized yield.
- Run the dividend-trap checklist before treating any buy-zone output as actionable.
- Buy-zone analysis must use deterministic boundaries from `buy-zone.md`.
- Buy-zone analysis must not use peak-cycle DPS as the base-case anchor unless that DPS is demonstrably sustainable.

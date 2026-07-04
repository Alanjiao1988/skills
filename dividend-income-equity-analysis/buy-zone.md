# Buy Zone Rules

This file defines how to estimate expected buy prices for dividend-income analysis.

The goal is not to produce a single target price. The goal is to translate dividend sustainability and historical valuation into a disciplined buy zone.

## 1. Required Inputs

Use the most current and reliable data available.

Required data:

- Current share price and as-of date.
- Trailing DPS and normalized DPS.
- Bear, base, and bull forecast DPS for the next three years.
- Withholding rate and net DPS.
- Five-year or longer historical price range when available.
- Historical year-end price, average price, or closing-price range.
- Historical gross and net dividend yield range.
- Historical dividend-yield percentiles when data is available.
- Sector, cycle, balance-sheet, and FCF coverage context.
- Dividend Trap Checklist result.

Optional data:

- 52-week high and low.
- Three-year and five-year price high / low / median.
- Drawdown from recent high.
- Market index level or sector index context when relevant.
- Historical valuation multiples such as P/E, P/B, EV/EBITDA, or P/FFO for REITs.

## 2. Core Buy-Price Formula

Use after-tax dividend income as the primary anchor:

```text
Net DPS = Gross DPS x (1 - withholding rate)
Buy Price = Net DPS / Required Net Yield
```

For normalized analysis:

```text
Normalized Buy Price = Normalized Net DPS / Required Net Yield
```

For scenario analysis:

```text
Bear Buy Price = Bear Net DPS / Required Bear Yield
Base Buy Price = Base Net DPS / Required Base Yield
Bull Buy Price = Bull Net DPS / Required Bull Yield
```

Do not use peak-cycle DPS as the base-case buy-price anchor unless the business is demonstrably capable of sustaining that DPS through a cycle.

## 3. Required Net Yield Selection

Choose required net yield from both historical yield and risk level.

Default guide:

| Dividend Profile | Required Net Yield Anchor |
|---|---:|
| Stable, regulated, low-volatility income | 4%-6% |
| Strong bank / telecom / utility with moderate growth | 5%-7% |
| Cyclical but financially strong dividend payer | 7%-10% |
| Formula-based variable dividend or commodity / shipping exposure | 8%-12% |
| Weak visibility, possible cut, or high leverage | Do not set a normal buy price; use special-situation framework |

Adjust required yield upward when:

- Dividend is cyclical or variable.
- FCF coverage is weak or peak-cycle-only.
- Balance sheet is stretched.
- Dividend depends on asset sales, debt, or equity issuance.
- Management has a discretionary or inconsistent payout policy.
- Regulatory, commodity, FX, or refinancing risk is high.

Adjust required yield downward only when:

- Dividend has long-term stability.
- FCF coverage is strong on normalized basis.
- Balance sheet is conservative.
- Dividend policy is clear and credible.
- The company has durable reinvestment or buyback support.

## 4. Deterministic Buy-Zone Boundary Rules

Use these boundary rules so the same inputs produce the same buy-zone output.

Definitions:

```text
N = normalized net DPS
B = bear-case net DPS, or conservative trough net DPS if bear-case DPS is unavailable
r_low = lower bound of required net yield range
r_high = upper bound of required net yield range
P_current = current share price
```

Requirements:

- `r_low` and `r_high` must be expressed as decimals, e.g. 0.06 for 6%.
- `r_high` must be greater than `r_low`.
- Use normalized DPS for fair and accumulation zones.
- Use bear or conservative DPS for strong-buy safety-margin testing.
- If `B` is unavailable, use a conservative haircut to N and label the haircut explicitly.

Boundary formulas:

```text
Too expensive boundary = N / r_low
Fair lower boundary = N / r_high
Fair upper boundary = N / r_low
Accumulation lower boundary = B / r_low
Accumulation upper boundary = N / r_high
Strong buy boundary = B / r_low
```

Zone mapping:

| Zone | Deterministic Boundary | Interpretation |
|---|---|---|
| Too expensive / avoid adding | Price > N / r_low | Normalized yield is below minimum required yield. |
| Fair value / hold | N / r_high < Price <= N / r_low | Normalized yield is within required range but margin of safety is limited. |
| Accumulation zone | B / r_low < Price <= N / r_high | Normalized yield is attractive and bear-case yield is approaching acceptable. |
| Strong buy zone | Price <= B / r_low | Bear-case DPS still meets the minimum required yield. |

If B is greater than N, treat B as invalid and explain the data problem. Bear-case DPS should not exceed normalized DPS.

If the deterministic boundaries overlap or produce nonsensical ranges because DPS is unstable, output "buy zone cannot be responsibly estimated" and list missing or invalid inputs.

## 5. Value-Trap Veto

Value trap is not a price zone. It is a veto condition.

If any major value-trap condition is triggered, all buy zones are suspended until the condition is resolved or explicitly treated as a special situation.

Major veto conditions include:

- Dividend likely to be cut or suspended.
- Normalized FCF / Dividend below 1.0x without a credible recovery path.
- Dividend funded by debt, equity issuance, or asset sales rather than recurring FCF.
- Balance sheet stress or near-term refinancing wall.
- Regulatory restriction or policy change that blocks payout.
- Peak-cycle dividend being used as recurring DPS.
- Equity issuance or ATM program concurrent with elevated payout and unclear capital need.

Required wording when triggered:

```text
Value-trap veto triggered: buy-zone output is suspended. High implied yield should not be treated as an entry signal until the following conditions are resolved: ...
```

## 6. Historical Yield Band Cross-Check

Build a historical yield band when data is available.

| Period | DPS Used | Price Range | Gross Yield Range | Net Yield Range | Yield Percentile | Comment |
|---|---:|---:|---:|---:|---:|---|

Use at least five years when possible. For cyclical sectors, include a full cycle if available.

Interpretation:

- Current yield below historical median: usually not attractive for pure dividend entry unless dividend growth is strong.
- Current yield near historical median: fair zone, not necessarily a margin-of-safety buy.
- Current yield in the top quartile of historical range: potentially attractive, but check whether the market is pricing in a dividend cut.
- Current yield far above history: either rare opportunity or dividend trap. Use FCF coverage and balance sheet to decide.

## 7. Historical Price Context

Use historical price levels as a secondary anchor, not the primary anchor.

| Metric | Price / Level | Current Position | Comment |
|---|---:|---:|---|
| Current price | | | |
| 52-week high | | | |
| 52-week low | | | |
| 3-year median | | | |
| 5-year median | | | |
| Recent drawdown from high | | | |
| Relevant index / sector level | | | |

Historical price can show sentiment and cyclicality, but it does not determine dividend value by itself. A stock can be cheap versus history and still be unattractive if normalized DPS is falling.

## 8. Buy-Zone Table

Every full dividend analysis should include a buy-zone table unless the user explicitly asks not to.

Use this table after applying the value-trap veto.

| Zone | Price Range | Implied Net Yield | DPS Basis | Condition Required | Action View |
|---|---:|---:|---|---|---|
| Too expensive / avoid adding | Price > N / r_low | Below required range | Normalized DPS | Yield below required return | Avoid adding |
| Fair value / hold | N / r_high < Price <= N / r_low | Required range | Normalized DPS | Reasonable yield, limited MOS | Hold / small add only |
| Accumulation zone | B / r_low < Price <= N / r_high | Attractive normalized yield | Normalized + bear DPS | Required yield met with acceptable coverage | Gradual buy |
| Strong buy zone | Price <= B / r_low | Bear-case yield meets minimum requirement | Bear or conservative DPS | Strong coverage and balance sheet required | Higher conviction buy |

Also output a separate line:

```text
Value-trap veto: Not triggered / Triggered / Unclear
```

## 9. Safety-Margin Checks

Before stating a buy zone, check:

- Does the buy price still make sense using bear-case DPS?
- Does the implied yield rely on special or peak-cycle dividends?
- Is FCF / Dividend above 1.0x on normalized basis?
- Would buy price still be reasonable if payout ratio falls to policy floor?
- Is current price already above the fair value range implied by normalized net yield?
- Is the stock cheap because of a temporary cycle issue or because the dividend is likely to be cut?

## 10. Required Output Language

Use disciplined language:

- Use "expected buy zone", "accumulation zone", or "income entry zone" rather than guaranteed target price.
- State the DPS basis used for each price range.
- State whether the buy zone is driven by normalized DPS, bear DPS, or headline TTM DPS.
- Never imply that a high yield alone is a buy signal.
- If data is insufficient, output "buy zone cannot be responsibly estimated" and list the missing inputs.

## 11. Visual Output

When rich visualization is available, add a Buy-Zone Ladder:

- Current price.
- Fair-value zone.
- Accumulation zone.
- Strong buy zone.
- Value-trap veto status.

When rich visualization is unavailable, use a compact text fallback:

```text
Buy-zone ladder: Current 100 | Fair 90-100 | Accumulate 75-90 | Strong buy <75 | Veto: not triggered
```

## 12. Relationship with DDM or Other Valuation Skills

This buy-zone framework is not a full DDM valuation and should not replace a dedicated valuation model.

- This skill sets dividend-income entry zones using net DPS, required yield, historical yield bands, and cash-flow safety.
- If the user asks for intrinsic value, DDM, moat, or reinvestment runway, use or reference the appropriate valuation skill.
- If dividend buy zone and DDM valuation conflict, explain the conflict rather than forcing one answer.

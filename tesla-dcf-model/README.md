# Tesla, Inc.: Integrated 3-Statement Model and DCF

![DCF valuation](screenshots/01-dcf-valuation.png)

**What it does.** Income statement, balance sheet and cash flow are fully linked (FY2023A-25A historicals, FY2026E-30E forecast, US$mm), and the DCF reads its cash flows straight from them. One switch (`Assumptions!B3`) runs Bear / Base / Bull through revenue growth and segment margins. Includes a WACC x terminal-growth sensitivity table and a reverse DCF.

**Key assumption choices**
- **Segment-driven revenue and margins:** auto, energy and services each have their own growth and gross-margin path per scenario (Base auto growth 2% -> 6%, auto GM 18% -> 20%).
- **Cost of capital:** risk-free 5.24% (US 10Y, 29-Sep-2026), beta 1.85, ERP 4.5% -> cost of equity 13.6%, **WACC 13.5%** (debt is <1% of capital). Terminal growth 3.0%.
- **Capex:** FY2026E calibrated to management's ">$20bn" guidance (20.5% of revenue), fading to 9% by FY2030E.
- **SBC is treated as a real cost** (not added back), and working capital runs off days / % of revenue.

**Key outputs**

| Scenario | Value / share | vs $358.54 |
|---|---|---|
| Bear | $13.08 | -96% |
| **Base** | **$19.80** | **-94.5%** |
| Bull | $34.84 | -90% |

Enterprise value (Base) $42.2bn. The reverse DCF shows the market price needs FY2030E free cash flow **~31x** the base case, i.e. the price is paying for robotaxi / Optimus optionality the model does not explicitly forecast.

**Integrity.** The three statements tie to reported Tesla figures (revenue, gross profit, EBIT, net income, CFO, FCF, total assets and liabilities: all differences zero), the balance sheet balances every year, and cash on the BS reconciles to the CF. Status: `ALL CHECKS PASS`.

**Limitations (stated in the model).** 5-year explicit period is short for a business still investing heavily (implied terminal EV/EBITDA only ~3.6x, so treat the value as a conservative floor); no explicit robotaxi/Optimus segment; balance-sheet date (Dec-2025) vs price date (Sep-2026) not rolled forward; share count differs by source.

**More screenshots:** [Assumptions](screenshots/02-assumptions.png) · [Income statement](screenshots/03-income-statement.png) · [Balance sheet](screenshots/04-balance-sheet.png) · [Cash flow](screenshots/05-cash-flow.png) · [Checks](screenshots/06-integrity-checks.png)

**Files:** [PDF export](pdf/Tesla_3-Statement_DCF_Model.pdf) · [Excel model](model/Tesla_3-Statement_DCF_Model.xlsx). Sources are logged on the `Sources` sheet (Tesla Q4/FY2025 Update, FY2025 10-K, market data).

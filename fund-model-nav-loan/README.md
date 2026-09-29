# Fund Model with NAV Loan: Capital Calls, Waterfall, IRR and LP Statement

![Returns summary](screenshots/01-returns-summary.png)

**What it does.** A synthetic $100mm growth fund over 40 quarters: capital calls, management fees and expenses, exits, carried interest, NAV, and investor returns (DPI / RVPI / TVPI, net and gross XIRR). A per-investor LP capital account statement ties back to fund NAV. An optional NAV-loan layer (switch on `Inputs!B35`) runs the fund with and without the facility side by side.

**Key assumption choices**
- **Fund terms:** 5-year investment period, 85% of commitments invested, 2.0% fee on commitments (1.5% of NAV after), 0.15% expenses, 20% carry with no preferred return or catch-up (a deliberate simplification).
- **Portfolio:** 18% gross return p.a.; exits start in quarter 17 at 4% of value, stepping up 1.5% per quarter, remainder liquidated in quarter 40.
- **NAV loan:** single draw in quarter 21, 15% LTV capped at $15mm, 9% cash-pay interest, 1% arrangement fee, 25% cash sweep from exits; net proceeds paid out as a special distribution.

**Key outputs (as of 31-Dec-2028)**

| Metric | With NAV loan | Without |
|---|---|---|
| DPI | 0.80x | 0.74x |
| RVPI | 0.58x | 0.64x |
| TVPI | 1.38x | 1.39x |
| Net IRR | 11.2% | 11.2% |

Gross IRR is 18.0%, so fees, expenses and carry cost **6.8 points** of IRR. The loan ($14.2mm drawn, $1.1mm total cost) pulls distributions forward, but the effect on IRR is small (+0.05 pt) and TVPI falls slightly because interest and fees are a real cost. That is the honest reading: a NAV loan mainly accelerates DPI rather than creating value. Fund-life net IRR 11.8%, final TVPI 1.50x.

**Integrity.** 15 checks including a NAV roll-forward identity, XIRR verified by NPV = 0, LP statement tie-out, loan drawn = repaid, and loan-off equals the no-loan model. Status: `ALL CHECKS PASS`.

**Simplifications (stated in the model).** No preferred return / catch-up / clawback; investors pro rata; single draw and fixed rate, no covenants; flows at quarter-end. All data is synthetic.

**More screenshots:** [Inputs](screenshots/02-inputs.png) · [NAV loan comparison](screenshots/03-nav-loan-comparison.png) · [LP statement](screenshots/04-lp-statement.png) · [Checks](screenshots/05-integrity-checks.png)

**Files:** [PDF export](pdf/Fund_Model_with_NAV_Loan.pdf) · [Excel model](model/Fund_Model_with_NAV_Loan.xlsx)

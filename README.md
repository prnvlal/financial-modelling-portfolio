# Financial Modelling Portfolio

Two Excel models built from scratch, fully linked, with built-in integrity checks, plus an M&A research note and a credit note with a euro DCM pricing model. Excel files don't preview on GitHub, so each model ships with a **PDF export** and **screenshots** alongside the `.xlsx`.

| Model | What it answers | Headline output | Open |
|---|---|---|---|
| **[Tesla: 3-statement model + DCF](tesla-dcf-model/)** | What is Tesla worth on a fundamentals-only DCF, and what would the market price need to believe? | Base $19.40/share vs $358.54 market; reverse DCF needs FY2030E FCF ~32x the base case | [PDF](tesla-dcf-model/pdf/Tesla_3-Statement_DCF_Model.pdf) · [xlsx](tesla-dcf-model/model/Tesla_3-Statement_DCF_Model.xlsx) |
| **[Fund model with NAV loan](fund-model-nav-loan/)** | How do fees, carry and a NAV facility change LP returns (DPI / RVPI / TVPI / IRR)? | Net IRR 11.2% vs gross 18.0%; NAV loan pulls DPI forward but lowers TVPI | [PDF](fund-model-nav-loan/pdf/Fund_Model_with_NAV_Loan.pdf) · [xlsx](fund-model-nav-loan/model/Fund_Model_with_NAV_Loan.xlsx) |
| **[WBD bid research note](wbd-research-note/)** | Which bid should Warner Bros. Discovery accept, and should Netflix raise its offer? | Accept Paramount's $31.00 cash; Netflix should not match (+$8.1bn for a synergy case that does not clearly pay) | [PDF](wbd-research-note/pdf/WBD_Research_Note.pdf) · [docx](wbd-research-note/note/WBD_Research_Note.docx) |
| **[Vodafone credit note + euro DCM model](vodafone-credit-dcm/)** | Where does Vodafone's credit sit after the VodafoneThree buyout, and where would a new euro 10-year price? | Hold, stable BBB; net debt / EBITDAaL 2.4x pro forma; new 10-year ~115bp over Bunds (4.53% yield) | [Note PDF](vodafone-credit-dcm/pdf/Vodafone_Credit_Note.pdf) · [xlsx](vodafone-credit-dcm/model/Vodafone_Credit_DCM_Model.xlsx) |

<a href="tesla-dcf-model/"><img src="tesla-dcf-model/screenshots/01-dcf-valuation.png" width="48%"></a>
<a href="fund-model-nav-loan/"><img src="fund-model-nav-loan/screenshots/01-returns-summary.png" width="48%"></a>

**Conventions in both workbooks:** blue = hard-coded input, black = formula, green = cross-sheet link, yellow = key assumption. Every model has a Checks sheet that must read `ALL CHECKS PASS`.

*Educational portfolio work built from public filings and illustrative assumptions. Not investment advice.*

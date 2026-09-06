# Corporate Governance Toolkit

Seven working compliance tools for Indian corporate governance — statutory deadlines, event-triggered ROC filings, board resolutions, Secretarial Standards, contract risk and SEBI obligations.

**Live: https://abhijithcw.github.io/corporate-governance-toolkit/**

Everything runs in the browser. No signup, no server, no data leaves the page — you can paste a real contract into the risk flagger and nothing is transmitted anywhere.

---

## Why this exists

I'm a BBA LLB (Hons.) graduate reading for the CS Executive. I built these to work through the statutory material properly — not by reading it, but by encoding the actual logic and seeing whether it held.

Encoding a rule forces a precision that reading does not. You can read Section 174 five times and still be vague about whether the one-third rounds up. You cannot write the formula without deciding.

---

## The tools

| # | Tool | What it does |
|---|---|---|
| 00 | **Company Classification** | Start here. Enter paid-up capital, turnover, borrowings and structure; get back what the company actually is — small company, OPC, dormant, Section 8 — and which fourteen obligations switch on or off because of it. Every other tool assumes you already know this. |
| 01 | **Compliance Radar** | Every statutory deadline a private company carries, computed from two anchor dates — incorporation and financial year end. AGM chain, ROC filings, POSH, FLA, with the penalty for each. |
| 02 | **Event Compliance Navigator** | 49 event-triggered filings. Something happened — a director resigned, a charge was created, shares were allotted — and it returns the form, the deadline computed from your date, the provision, the attachments, and a late-filing fee estimate across three separate fee regimes. |
| 03 | **Board Resolution & Minutes Generator** | Twelve common board resolutions with an SS-1 compliant draft minutes entry, and a live Section 174 quorum and notice-period check as you fill it in. |
| 04 | **SS-1 / SS-2 Checker** | Was that meeting actually valid? Checks a board meeting against SS-1 or a general meeting against SS-2 — notice, quorum, cadence, and the minutes deadlines that follow. |
| 05 | **Contract Clause Risk-Flagger** | Paste contract text; get back 24 clause patterns that commonly disadvantage the reviewing party under Indian law, each with a plain-English risk note and a redline to propose. |
| 06 | **SEBI Compliance Checker** | Listed-company filing calendar with real per-day fine rates, the size-linked governance thresholds, and PIT insider trading — including a live trading-window calculation. |

---

## What's actually encoded

**Companies Act, 2013** — Sections 2(85), 10A, 12, 39, 42, 56, 61, 64, 66, 68, 77, 79, 82, 88, 89, 90, 92, 96, 101, 103, 117, 118, 128, 134, 135, 137, 139, 140, 152, 161, 164, 167, 168, 169, 173, 174, 184, 186, 188, 196, 203, 405, 455 — with the rules made under them, including the Registration Offices and Fees Rules and the Prospectus and Allotment of Securities Rules.

**Secretarial Standards** — SS-1 (Meetings of the Board) and SS-2 (General Meetings), issued by the ICSI.

**SEBI** — the LODR Regulations, 2015 and the Prohibition of Insider Trading Regulations, 2015.

**Other** — the Indian Contract Act 1872, the Indian Stamp Act 1899, the Registration Act 1908, the Arbitration and Conciliation Act 1996, the MSMED Act 2006, the CGST Act, the POSH Act 2013, and FEMA/RBI reporting requirements.

---

## On accuracy

This is the part I took most seriously, because a wrong figure in a compliance tool is worse than no tool.

Timelines and penalties were checked against the bare provisions and the rules, not against coaching material. Where a figure could not be verified from a reliable source, the tool says so rather than showing a number that looks confident — two SEBI fine rates and two ROC items are marked that way deliberately.

**Content verified as at September 2026.** That date is on every page, because statutory figures are amended and a tool that doesn't tell you how old it is cannot be trusted. A verification pass in September 2026 corrected several items that most secondary sources still state incorrectly:

- **DIR-3 KYC is no longer annual.** It became triennial, due 30 June, with effect from 31 March 2026. Compliance calendars still showing "30 September, every year" are out of date.
- **A small company is now ₹10 crore paid-up capital and ₹100 crore turnover** (w.e.f. 1 December 2025), not ₹4 crore / ₹40 crore — which cascades into MGT-7A eligibility, board meeting cadence, auditor rotation and Rule 9B.
- **PAS-3 is fifteen days only for private placement** under Section 42(8). Every other allotment is thirty days under Section 39(4), with a different penalty cap.
- **Section 8 companies are not governed by Section 173(5)** — they run on one board meeting per six calendar months under exemption notification G.S.R. 466(E). Start-up private companies *are* in 173(5).
- **SEBI Regulations 27(2) and 13(3) moved from 21 days to 30 days** under the Integrated Filing regime, and Regulation 23(9) is no longer a standalone half-yearly filing.
- **Rule 9B dematerialisation is a rolling 18-month trigger**, not the fixed dates of 30 September 2024 or 30 June 2025 that are still widely quoted — both have passed.

---

## How it was built

Plain HTML, CSS and JavaScript. No framework, no build step, no dependencies. Each tool is a single self-contained file, which is why they load instantly and work offline.

The code was written with the assistance of an AI coding tool (Claude), under my direction. I set the scope, decided what each tool should do, researched and verified every legal provision, and made the design and content decisions. I'm a law graduate rather than a developer — using the tool for the implementation was the point, not something to hide.

---

## Repository structure

```
├── index.html                      landing page
├── company-classification/         00
├── compliance-radar/               01
├── event-compliance/               02
├── board-resolution-generator/     03
├── ss-checker/                     04
├── contract-risk-flagger/          05
├── sebi-compliance-checker/        06
└── thumbnails/                     preview images for the landing page
```

---

## Disclaimer

These are reference tools built for portfolio purposes. **They do not constitute legal advice and do not replace review by a practising Company Secretary or advocate.** They compute against general provisions; they do not know your company's facts, its Articles, or its filing history. The contract risk flagger in particular is a pattern-matching triage aid — it does not read context or understand negation, and it can both miss real risks and flag clauses that are fine.

Confirm anything here against the current provision before relying on it for an actual filing.

---

## Author

**Abhijith** — BBA LLB (Hons.), pursuing CS Executive. Palakkad, Kerala.
Open to Company Secretary traineeship and corporate compliance roles.

- Email: abhijithramadas02@gmail.com
- LinkedIn: https://www.linkedin.com/in/abhijith-c-46ab66143/

© 2026 Abhijith. All rights reserved — see [LICENSE](LICENSE).

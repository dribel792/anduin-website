# Prospectus Roles & Service-Provider Checklist

**Anduin tokenized securities programme — EU base prospectus + final terms**

> **WORKING CHECKLIST — NOT LEGAL ADVICE.** Prepared for internal planning. Every "hard requirement" and every Category A/B/C classification below must be confirmed by prospectus counsel (Liechtenstein FMA route) before the base prospectus is locked. The single most common reason a base prospectus is bounced is putting information in final terms that the base did not flag as optional.

---

## The one rule that governs all of this

Under the **EU Prospectus Regulation (Reg. 2017/1129, Art. 8)** and **ESMA's guidelines on final terms**, final terms can **only** fill in blanks the base prospectus *explicitly left open* (ESMA Category A / B / C fields). You **cannot** introduce a new party or role in final terms that the base prospectus did not contemplate.

> **Therefore, for every multi-party role: park the *optionality* in the base prospectus** ("the Issuer may appoint one or more / additional [role]"), then **name the actual party per Series in the final terms.** This is what lets you name one now and add more later.

Structure is modelled on the two FMA-approved comparables already in market:
- **Ondo Global Markets BVI Limited** — base prospectus approved by Liechtenstein FMA 11 Nov 2025; final terms (e.g. product "QQQon") filed and passported into the EEA.
- **Backed Assets (JE) Limited** ("xStocks") — Liechtenstein FMA base prospectus + per-product final terms.

---

## Checklist

Legend — **Req:** ⬛ Hard requirement / ⬜ Optional or structure-dependent · **Where:** B = Base prospectus / FT = Final terms / OPS = Operational only (not in prospectus)

### 1. Issuer entity
- **Req:** ⬛ Hard
- **Where:** B
- **What we decided:** Newly-incorporated SPV issuer (Ondo uses a BVI Ltd; Backed uses a Jersey Ltd). Holding/option structure to Anduin Holdings sits separately (see `call-option-deed.md`).
- **Who can fill it:** Anduin's own SPV. Needs incorporation + directors + registered agent.
- **When ready:** **Before** base prospectus drafting begins — it is the named party on the cover.

### 2. Dealer / Manager (MiFID-authorised)
- **Req:** ⬛ Hard (at least one)
- **Where:** B names ≥1 + "additional Dealers may accede"; per-issuance Manager → FT
- **What we decided:** Name **one** MiFID firm you have the relationship with in the base via the Dealer Agreement; add more later by accession; the manager for each tranche goes in final terms.
- **Who can fill it:** Any EU MiFID-authorised investment firm acting as dealer/distributor.
- **When ready:** Lead Dealer signed into the **Dealer Agreement before base approval**. Additional dealers anytime after.

### 3. Hedge counterparty
- **Req:** ⬜ Not named in prospectus
- **Where:** OPS (disclose hedging *risk* generically in B)
- **What we decided:** Do **not** name them. Base discloses generically — "the Issuer may enter into back-to-back / hedging arrangements with one or more counterparties." Bybit account just needs to exist operationally.
- **Who can fill it:** Bybit (example) or any exchange/OTC desk where the hedge account is live.
- **When ready:** Account open **before first Series settles**; no prospectus deadline.

### 4. Paying Agent
- **Req:** ⬜ Structure-dependent (may be collapsed into Registrar/Admin)
- **Where:** B names a Principal Paying Agent + "additional paying agents may be appointed"; channel-specific ones → FT
- **What we decided:** Same logic as the Dealer — name an anchor in the base, allow more via final terms **if** you even need a classic one. **Ondo names no separate paying agent** — on-chain settlement + the Administrator/Registrar absorb the function. For sui-generis tokens you can likely collapse this into role #5.
- **Who can fill it:** A paying-agent bank, **or** fold into the Registrar/Administrator (BNY Mellon-type role).
- **When ready:** Decide structure **before base drafting**; name in FT per Series if used.

### 5. Registrar / Administrator
- **Req:** ⬛ Hard (this is the role you actually need, not "transfer agent")
- **Where:** B (anchor) — specific entity can be confirmed in FT
- **What we decided:** This is Ondo's equivalent of the transfer-agent function. **Ondo names The Bank of New York Mellon as Administrator & Registrar.**
- **Who can fill it:** An institutional administrator/registrar (BNY Mellon-class), or the issuer's appointed registrar.
- **When ready:** Engaged **before base approval**.

### 6. Transfer Agent
- **Req:** ⬜ Not needed
- **Where:** — (n/a)
- **What we decided:** **Not required.** These are sui-generis tokens, not under the DLT Pilot Regime — the **on-chain register *is* the transfer layer.** Neither Ondo nor Backed names a classic transfer agent; the Registrar (#5) covers the register.
- **Who can fill it:** N/A — covered by Registrar/Administrator.
- **When ready:** N/A.

### 7. Custodian(s)
- **Req:** ⬛ Hard (you hold the underlying)
- **Where:** B framework; specific custodians per product → FT
- **What we decided:** Underlying held in custody (Backed: Swiss prime broker / custodian bank). **Ondo final terms name Alpaca Securities LLC and BitGo Trust Company, Inc.** as custodians.
- **Who can fill it:** A regulated broker-dealer (securities) and/or qualified custodian (Alpaca / BitGo-class).
- **When ready:** Custody agreements in place **before first Series settles**; named per Series in FT.

### 8. Security Trustee / Security Agent
- **Req:** ⬜ Conditional — hard *if* the tokens are secured/collateralised
- **Where:** B describes the **security framework** (that security may exist, mechanism, ranking/subordination); identity + collateral description per use-case → FT
- **What we decided:** Can live in final terms **provided** the base sets up the framework. **Ondo's base creates a "Security Agent" role; the collateral description sits in final terms** per product — exactly the use-case-to-use-case flexibility you want.
- **Who can fill it:** A corporate security trustee / security-agent firm.
- **When ready:** Framework in base **before approval**; specific agent + collateral per Series in FT.

### 9. Calculation Agent
- **Req:** ⬜ Structure-dependent (needed for tracker / structured payoffs)
- **Where:** B (anchor) + FT per Series
- **What we decided:** Standard for delta-one / tracker products; can be the Issuer or an appointed agent. Flag to counsel whether self-appointment is acceptable.
- **Who can fill it:** Issuer itself or an appointed calculation agent.
- **When ready:** Confirmed **before base approval**.

---

## Timeline (sequencing)

| Phase | What must be ready | Roles locked |
|---|---|---|
| **0 — Pre-structuring** | Issuer SPV incorporated; structure decisions (secured vs unsecured, calc-agent self-appointment, paying-agent collapse) | #1 |
| **1 — Base prospectus drafting** | Lead Dealer signed; Registrar/Admin engaged; security framework drafted; all *optionality* language inserted | #2, #5, #8 (framework), #9 |
| **2 — FMA approval & EEA passporting** | Base prospectus filed with Liechtenstein FMA, approved, notified to target EEA states | (approval gate) |
| **3 — Per-Series (each final terms)** | Name actual Manager, custodians, security agent + collateral, paying agent if used | #2, #3 (ops), #4, #7, #8 (identity) |
| **4 — Ongoing / operational** | Hedge account live; custody live; additional dealers accede as needed | #3, #7, #2 (additions) |

---

## Hard-requirement summary

**Must exist before the base prospectus can be approved:** Issuer (#1), ≥1 Dealer/Manager (#2), Registrar/Administrator (#5), and — if secured — the Security framework (#8).

**Per-Series in final terms:** Manager, Custodian(s), Security Agent + collateral, Paying Agent (if used).

**Operational only, never named in the prospectus:** Hedge counterparty (#3).

**Not needed at all:** Transfer Agent (#6).

---

### Open items for counsel
1. Confirm ESMA Category (A/B/C) for each FT-populated field above — this is the rejection risk.
2. Confirm the paying-agent function can be collapsed into the Registrar/Administrator for a sui-generis token.
3. Confirm calculation-agent self-appointment by the Issuer is acceptable.
4. Pull Ondo's and Backed's actual FMA-approved base prospectuses side-by-side as drafting templates.

**Comparable sources:**
- Ondo GM final terms (QQQon): https://www.mfsa.mt/wp-content/uploads/2026/01/Ondo-Global-Markets-BVI-Limited-Final-Terms-Document-dated-11-November-2025.pdf
- Ondo GM base-prospectus notes: https://docs.ondo.finance/ondo-global-markets/important-notes
- Backed / xStocks legal documentation: https://assets.backed.fi/legal-documentation

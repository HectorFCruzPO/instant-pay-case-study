# Building Instant Pay around nurses: from 36% to 94% adoption

## Bringing earned-pay access into the ESHYFT app

I led the Instant Pay initiative at ESHYFT, a marketplace connecting nursing professionals with facilities that need shifts filled. My role covered client and nurse discovery, vendor evaluation, product strategy, and product and system planning. The work connected the experience nurses wanted with the payment capabilities and operational processes required to deliver it.

We listened to clients and nurses, identified their biggest unmet needs, and used those findings to define our product and technical requirements. Those requirements guided vendor evaluation and determined what ESHYFT needed to build. Instant Pay launched on **December 28, 2025**, with a **36% usage baseline in December**. By the **end of January 2026**, usage reached **79%**—an increase of **43 percentage points in the first month after launch**. By September 2026, **94% of active 1099 nurses used it**.[^impact]

This case study focuses on the original implementation and launch, with subsequent adoption results.

> **Disclosure:** To protect confidential business information, this public case study reports selected percentages and relative changes. Absolute nurse counts, transaction counts, payment volumes, and monetary amounts are omitted.

## Why the earlier Pay On Demand experience needed to change

ESHYFT already offered early access to pay through Fingercheck. That gave us an existing service to evaluate, but it also gave nurses a reference point for what they wanted improved.

The earlier experience had payout restrictions, fragmented setup, and limited visibility into available pay within the nurse app. Nurses wanted more control over accessing their earnings and a clearer understanding of what was available to them.

The opportunity was to bring those needs together in a coherent experience inside ESHYFT. Doing that required evaluating both the provider and the systems around it: onboarding, timecard eligibility, balance calculations, payroll deductions, and reconciliation.

## The problem

We listened to clients and nurses to understand which changes would make the greatest difference. Discovery included a user survey that identified demand for changes to the existing experience. Feedback included approval delays, payout caps, and requests for direct deposit.

The recurring need was control: nurses wanted to understand what they could access and receive their earnings through an experience that fit how they worked.

Our investigation also identified an opportunity in the competitive experiences we reviewed. They did not provide the combination our nurses were asking for. We believed meeting those needs could meaningfully differentiate ESHYFT.

For the business, the question was whether a better experience would lead more nurses to use the product. We also wanted to investigate its relationship with repeat engagement, reactivation, and shifts worked.

## The decision

We chose to let nurse needs define the solution. Our guiding belief was simple: **if we built the best experience for our nurses, they would use it.**

I translated the discovery findings into product and technical requirements and evaluated the existing Fingercheck experience alongside alternatives including Branch and Stripe. The evaluation covered the nurse experience, payout capabilities, integration effort, and fit with payroll and reconciliation. It also helped determine which capabilities a vendor could provide and which ESHYFT needed to build.

The resulting operating model uses Stripe for payouts, with ESHYFT managing the Instant Pay ledger, balances, eligibility, limits, and support visibility.

The goals:

1. Give nurses clear visibility into available earnings and more control over accessing them.
2. Bring setup, payout methods, cash-out, and payment history into the ESHYFT journey.
3. Support that experience with consistent eligibility, balance, deduction, and reconciliation rules.
4. Increase meaningful usage of Instant Pay.

Our measurement planning included weekly Instant Pay-active nurses, defined as nurses who submitted a timecard and used Instant Pay in the same week. This planning definition is distinct from the monthly adoption measure reported below.

## What we built

The implementation connected the nurse-facing experience with the systems required to support payments. I led product and system planning across these areas, working with Engineering, Design, Finance, and Support:

- **Onboarding and setup.** Defined entry points and contextual prompts for new and existing nurses. Nurses who had already saved a payout method needed a relevant next action.
- **Wallet.** Brought available earnings, payout methods, cash-out, and payment history together within the nurse app.
- **Payment requests.** Defined how nurses request a payout, understand the fee, and see the resulting payment status.
- **Eligibility and balances.** Defined which earnings could contribute to available pay, how holds and restrictions affected access, and how changed or rejected timecards should affect the balance.
- **Payroll and deductions.** Addressed the original W-2 requirements around tax calculations, deductions, and obligations remaining for regular payroll.
- **Admin and operations.** Planned payout reporting, deduction exports, reconciliation, and failed-payment review so Finance and Support could trace payments and investigate discrepancies.

**Launch:** December 28, 2025. Usage stood at **36% in December** and reached **79% by the end of January 2026**.[^impact] Earlier planning included W-2 payroll requirements. The adoption comparison uses the December 2025 baseline at launch and the new product's 2026 adoption among active 1099 nurses.

### Before and after

| Experience | Before: Pay On Demand | After: Instant Pay |
| --- | --- | --- |
| Setup | Fragmented setup experience | Setup incorporated into the ESHYFT journey with contextual prompts |
| Earnings visibility | Limited in-app visibility into available pay | Wallet showing earnings available for withdrawal |
| Cash-out | Existing provider-led experience with restrictions raised in discovery | In-app payout request with fee and payment status |
| Payment visibility | Information spread across the earlier experience | Wallet payment history and supporting operational visibility |

*Screenshot pairs to add: setup, balance/Wallet, cash-out, and payment history. Use original launch screens or clearly labeled recreations with fictional data.*

## Managing the risks

A straightforward cash-out experience depended on clear rules underneath it. The original planning addressed:

- **Available-pay accuracy.** Distinguished total earnings from withdrawable funds, accounting for eligibility, deductions, tax calculations, and holds.
- **Changed timecards.** Defined balance handling when earnings changed after a timecard was rejected or corrected, including cases where money had already been withdrawn.
- **Payroll consistency.** Accounted for early withdrawals and deductions in the regular payroll process to avoid paying the same earnings twice.
- **Payment problems.** Included payment statuses, failed-payment review, and operational visibility in the requirements.
- **Reconciliation.** Planned reporting that could connect earnings, the Instant Pay ledger, and payout-provider records.

## Impact

When we launched on **December 28, 2025**, usage stood at **36%**. By the **end of January 2026**, it had reached **79%**—a **43-percentage-point increase in the first month after launch**. By September, it reached **94%**, a total increase of **58 percentage points** over the December launch baseline.[^impact]

| Measure | Result |
| --- | --- |
| December 2025 baseline at launch on December 28 | **36%** |
| End of January 2026: first month after launch | **79%** |
| September 2026 adoption among active 1099 nurses | **94%** |
| Increase from baseline to first month | **+43 percentage points** |
| Total increase from baseline to September | **+58 percentage points** |
| Monthly hours worked per 1099 nurse, January–September | **Approximately +29%** |

### Engagement and retention

Among 1099 nurses whose first paid week fell between December 28, 2025 and March 31, 2026, Instant Pay users had higher observed retention than nurses who never used it. A nurse counted as still active if paid for work in any week from September 6 through October 18, 2026.[^impact]

| Segment | Still active Sep–Oct | Observed retention relative to non-users |
| --- | ---: | ---: |
| Regular users: used Instant Pay in at least half of worked weeks | **36%** | **About 2.3×** |
| Occasional users: used Instant Pay in fewer than half of worked weeks | **45%** | **About 2.8×** |
| Never used Instant Pay | **16%** | Reference group |

Instant Pay users were approximately **two to three times as likely to remain active** in the follow-up period. This is an observed association, rather than proof that Instant Pay caused higher retention. Occasional users had the highest retention, so these results do not establish that more frequent cash-outs improve retention.

### Broader business context

Across January–September 2026, platform monthly active nurses increased **21%** and hours worked increased **42%** compared with the same period in 2025.[^impact]

These trends overlap with the W-2-to-1099 transition and market growth. They provide context for the launch without attributing all platform growth to Instant Pay. The retention groups may also differ in work history, motivation, and other characteristics.

## What I learned

Listening to customers can shape the underlying system as much as the interface. In this project, client and nurse needs helped define the requirements we brought to vendors and the capabilities we needed to build ourselves.

Vendor evaluation was therefore part of product strategy. It required understanding how each option would support the intended nurse experience, integrate with our systems, and work for the teams responsible for payments.

The adoption result reinforced our original belief: building around what nurses valued could create meaningful differentiation. Delivering that experience also required careful attention to the less visible work—eligibility, balances, deductions, and reconciliation.

## What I'd do next

Building on the original launch, I would examine which parts of the experience drove adoption and where nurses still encountered friction. Setup completion, first cash-out, repeat use, and payment-related support contacts would help identify the next opportunities.

I would build on the observed retention differences with analysis that accounts for nurse tenure, work history, and the W-2-to-1099 transition. That would help distinguish the value associated with Instant Pay from differences between the nurses who choose to use it and those who do not.

[^impact]: The project lead confirmed the December 28, 2025 launch date, the 36% December usage baseline at launch, and 79% usage by the end of January 2026. Internal analysis provides the new product's January and September 2026 adoption, engagement, and retention results. Monthly adoption in 2026 is measured among active 1099 nurses; the December baseline reflects usage at launch, before the January 2026 observation. Selected percentages are rounded; absolute business figures are intentionally omitted. Retention uses the cohort and follow-up period described above.
# The Cost of a Roof — AU/NZ Rental Cost Model

Rent goes up faster than costs increase. This interactive tool shows you why — and lets you pull apart every layer of a rental property's cost stack to see where the money actually goes. Adjust interest rates, insurance shocks, council rates, and inflation, then watch how percentage-based charges (like property management fees) amplify every increase before it reaches the tenant.

**[Open the live tool](https://mattybnzl.github.io/rental-cost-modelling/)** — no install, runs in your browser.

## What you can do

- **Choose your region** — NSW, VIC, QLD, SA, WA, or NZ, each with real median rents, property values, and region-specific rules
- **Pick a property type and owner model** — house vs unit, individual landlord vs portfolio investor vs social housing
- **Drag sliders** for interest rates, insurance, council rates, property values, inflation, and market rent — see the cost stack update in real time
- **See "The Gap"** — the central callout showing exactly how much of your rent increase comes from actual costs vs the snowball effect of percentage-based fees
- **Toggle "What if fees were flat?"** — instantly see the rent difference if management fees were a fixed dollar amount
- **Shift cost bearers** — click any cost line to move it between landlord, tenant, and government to explore policy alternatives
- **Load scenario presets** — 2019 baseline, COVID era, 2023 peak, current 2026, QLD cyclone, NZ earthquake
- **View the 5-year plotter** — compare market trajectory against policy proposals (NZ Greens 2% cap, CPI-linked cap, rent freeze)
- **Check rent-to-income** — visual gauge showing housing stress thresholds against regional median household income

## The core idea

Property management fees, insurance premiums, and other percentage-based charges work the same way supply chain markups do. When underlying costs rise, percentage fees are calculated on a larger base — so the dollar amount grows automatically. The tenant pays the compounded result. This isn't about blame — individual landlords, portfolio investors, and property managers are all responding to the same structure.

## Data sources

All figures are sourced from public data verified March 2026 — Domain rental reports, CoreLogic, RBA rates, APRA insurance statistics, state revenue offices, and more. Full source list with 40+ citations available in the repo.

## Status

This tool is **in active development** (currently v3.4). Regions, cost models, and visualisations are still evolving. Planned additions include a Sankey flow diagram and historical timeline mode.

## Feedback welcome

This was built to make rental costs transparent, not to push a position. If the model feels wrong, the numbers seem off, or you'd approach something differently:

- Open an [issue](https://github.com/mattybnzl/rental-cost-modelling/issues)
- Start a [discussion](https://github.com/mattybnzl/rental-cost-modelling/discussions)

Whether you're a tenant, landlord, property manager, or policy nerd — your perspective makes this better.

## Technical

Single self-contained HTML file. No frameworks, no dependencies, no build step. Works offline. Mobile responsive.

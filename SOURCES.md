# The Cost of a Roof — Data Sources

Version: v3.6 (July 2026)

All figures are approximate and representative of typical properties. Data was verified July 2026 (refresh from the March 2026 baseline: RBA 4.35% + per-region NZ rate, AU negative-gearing/CGT reform Act No. 49, banded land tax, 2026 ACCC insurance report, Tiaki Wai live). Sources are categorised by data type.

---

## Median Rents

Weekly median rents by region and property type.

| Region | House | Unit | Source |
|--------|-------|------|--------|
| NSW | $765 | $700 | CoreLogic Hedonic Home Value Index, Domain Rental Report Q4 2025 |
| VIC | $560 | $510 | CoreLogic Hedonic Home Value Index, Domain Rental Report Q4 2025 |
| QLD | $640 | $540 | CoreLogic Hedonic Home Value Index, Domain Rental Report Q4 2025 |
| SA | $540 | $400 | CoreLogic Hedonic Home Value Index, Domain Rental Report Q4 2025 |
| WA | $625 | $505 | CoreLogic Hedonic Home Value Index, Domain Rental Report Q4 2025 |
| NZ | NZ$625 | NZ$575 | Trade Me Property Insights, Stats NZ rental bond data |

## Property Values

Median property values by region and type.

| Region | House | Unit | Source |
|--------|-------|------|--------|
| NSW | $950,000 | $750,000 | CoreLogic, Domain House Price Report |
| VIC | $780,000 | $580,000 | CoreLogic, Domain House Price Report |
| QLD | $700,000 | $500,000 | CoreLogic, Domain House Price Report |
| SA | $650,000 | $420,000 | CoreLogic, Domain House Price Report |
| WA | $720,000 | $480,000 | CoreLogic, Domain House Price Report |
| NZ | NZ$780,000 | NZ$550,000 | REINZ Monthly Property Report, QV.co.nz |

## Median Household Income

Weekly median household income by region.

| Region | $/wk | Source |
|--------|------|--------|
| NSW | $1,829 | ABS Household Income and Wealth, 2022-23 (Cat. 6523.0), adjusted to 2025 |
| VIC | $1,759 | ABS Household Income and Wealth, 2022-23 (Cat. 6523.0), adjusted to 2025 |
| QLD | $1,675 | ABS Household Income and Wealth, 2022-23 (Cat. 6523.0), adjusted to 2025 |
| SA | $1,455 | ABS Household Income and Wealth, 2022-23 (Cat. 6523.0), adjusted to 2025 |
| WA | $1,815 | ABS Household Income and Wealth, 2022-23 (Cat. 6523.0), adjusted to 2025 |
| NZ | NZ$2,107 | Stats NZ Household Economic Survey 2023, adjusted to 2025 |

## Interest Rates

| Parameter | Value | Source |
|-----------|-------|--------|
| Base mortgage rate (AU) | 7.05% | RBA cash rate 4.35% (held 17 Jun 2026, next decision 11 Aug 2026) + typical investor margin |
| Base mortgage rate (NZ) | 5.9% | RBNZ OCR 2.50% (hiked 8 Jul 2026) + NZ investor margin. AU and NZ policy rates diverged, so the rate is now per-region (was a single global 6.8% in v3.5) |
| Portfolio discount | -0.2% | Industry estimate — volume discount for 3+ property portfolios |
| Social housing rate adj | none (0%) | Social housing is government-funded, no commercial mortgage |

## Insurance

| Parameter | Value | Source |
|-----------|-------|--------|
| Base building insurance rate | 0.4% of property value | APRA General Insurance Statistics, Insurance Council of Australia |
| Insurance risk multipliers | 0.8x (SA) to 1.5x (NZ) / 1.35x (QLD) | ACCC Insurance Monitoring (final report 25 Jun 2026), ICA Catastrophe Database. NB: the ACCC's northern-Australia monitoring mandate ended 30 Jun 2026 - a new source is needed for future refreshes |
| QLD cyclone premium note | ~34% above national avg | ACCC final Insurance Monitoring Report, Jun 2026 (north QLD avg >$3,100 vs ~$2,310 rest-of-AU). Reinsurance cyclone pool cut year-1 premiums 11-15% in target zones (Karratha -15%, Cairns -12%, Townsville -3%). Was ~60% per the superseded 2020 ACCC inquiry |
| NZ earthquake risk | 1.5x | EQC/Toka Tu Ake data, Insurance Council of NZ |
| Landlord liability insurance | $420/yr | Market rates for standard landlord insurance policies (Terri Scheer, EBM RentCover) |

## Council Rates

| Region | Annual | Avg increase | Source |
|--------|--------|--------------|--------|
| NSW | $2,400 | ~4%/yr | NSW Office of Local Government rate peg, council rate notices |
| VIC | $2,100 | ~4%/yr | Essential Services Commission rate cap |
| QLD | $2,200 | ~5%/yr | QLD council budget papers, LGAQ data |
| SA | $2,000 | ~4%/yr | SA council budget papers |
| WA | $2,300 | ~4%/yr | WA DLGSC rate data |
| NZ | NZ$4,100 | 8.4%/yr | NZ Dept of Internal Affairs local authority statistics, media reporting (2024-2025). Wellington 47% over 3 years. Water infrastructure costs (Three Waters reform, Tiaki Wai) driving above-CPI increases. Proposed govt cap of 2-4% from 2027 explicitly exempts water charges. |

## Water

| Region | Annual | Who pays | Source |
|--------|--------|----------|--------|
| NSW | $1,100 | Tenant (usage) | Sydney Water, Hunter Water typical residential bills |
| VIC | $1,200 | Landlord | Residential Tenancies Act 1997 (VIC) — landlord pays unless separately metered |
| QLD | $1,000 | Tenant (usage) | QLD Urban Utilities, Unity Water typical bills |
| SA | $900 | Varies | SA Water typical bills, lease-dependent allocation |
| WA | $1,000 | Tenant (usage) | Water Corporation WA typical bills |
| NZ | NZ$800 | Landlord | Residential Tenancies Act 1986 (NZ) — fixed water charges are landlord responsibility. Wellington: Tiaki Wai (separate water entity live since Jul 2026) projected ~NZ$2,418/yr, expected to double by 2036 |

## Stamp Duty / Transfer Duty

| Region | Rate used | Source |
|--------|-----------|--------|
| NSW | 4.5% | NSW Revenue — transfer duty rates (investment property, no FHBG) |
| VIC | 5.5% | State Revenue Office VIC — land transfer duty |
| QLD | 3.5% | QLD Revenue — transfer duty rates |
| SA | 4.0% | RevenueSA — stamp duty rates |
| WA | 4.0% | WA Revenue — transfer duty |
| NZ | 0% | No stamp duty in NZ |

Note: Amortised over 10-year hold period (HOLD_YRS constant).

## Land Tax

As of v3.6 the model uses **full banded scales** (the `LAND_TAX` const), ported verbatim from the Rental Portfolio dashboard's `LAND_TAX` register (each scale read at the state revenue office on 2026-07-08; no 2026-27 budget changes to any residential-investment scale). Entry is inclusive (`>= from`), so QLD is taxable AT its $600k threshold (-> $500) while NSW only above $1.075m. Previously (v3.5 and earlier) a single-threshold flat-rate formula understated VIC ~2x and overstated WA ~2x at typical land values.

| Region | First taxing threshold | Scale | Source (verified 2026-07-08) |
|--------|-----------|------|--------|
| NSW | $1,075,001 | $100 + 1.6%, then 2.0% over $6.571m | Revenue NSW (thresholds frozen since 2024) |
| VIC | $50,000 | $500/$975 flat bands, then 0.3%→2.65% marginal from $300k (COVID debt levy folded in, to 2033) | SRO Victoria |
| QLD | $600,000 | $500 + 1.0%, then 1.65%→2.25% (taxable AT threshold) | Queensland Revenue Office |
| WA | $300,001 | $300 flat to $420k, then 0.25%→2.67% marginal | RevenueWA |
| SA | $833,000 | 0.5% single-threshold **approximation** — March-2026 data, NOT re-verified in the Jul 2026 pass; verify at RevenueSA before relying on SA output | RevenueSA (unverified) |
| NZ | N/A | No land tax (Land Tax Abolition Act 1990) | — |

Land value modelled as 60% of property value. Portfolio investors use a 2.5x land tax multiplier (crude proxy for aggregated holdings on the general scale).

## Property Management Fees

| Region | Rate | Source |
|--------|------|--------|
| NSW | 5.8% | REINSW, industry survey data (Sydney metro typical) |
| VIC | 5.9% | REIV, industry survey data |
| QLD | 7.5% | REIQ — typical QLD management fees |
| SA | 10.0% | Industry survey — SA typically higher due to smaller market |
| WA | 8.7% | REIWA, industry survey data |
| NZ | 8.5% + 15% GST | REINZ — NZ management fees attract GST |

Portfolio investors receive an 18% discount on management fees (0.82 multiplier).

## Other Operating Costs

| Cost | Value | Source |
|------|-------|--------|
| Strata/body corp | $2,800-$6,000/yr (varies by region) | Strata Community Association, Macquarie Bank Strata benchmarks |
| Maintenance | $3,500/yr (individual/portfolio), $4,500/yr (social) | Industry rule-of-thumb: 0.5-1% of property value; social housing higher due to compliance obligations |
| Compliance (smoke alarms, pool, healthy homes) | $500/yr AU, $800/yr NZ | State/territory regulatory compliance costs. NZ higher due to Healthy Homes Standards |
| Admin/accounting | $900/yr | Typical landlord admin, tax preparation, depreciation schedule costs |
| Letting fee (re-leasing) | $650/yr | Average across regions — one week's rent equivalent, averaged over lease term |
| Vacancy allowance | 3% (individual), 2% (portfolio) | SQM Research vacancy rates, industry benchmarks |

## Tenant-Paid Costs

| Cost | Annual | Source |
|------|--------|--------|
| Power/electricity | $2,340 | AER annual retail market report, Canstar Blue energy surveys |
| Internet | $1,040 | WhistleOut, Finder — typical NBN/fibre plan |
| Garden maintenance | $520 | Airtasker/hipages — fortnightly mow + seasonal clean-up |

## Tax Settings

| Parameter | Value | Source |
|-----------|-------|--------|
| Marginal tax rate | 37% | ATO individual tax rates 2025-26 — $120k-$180k bracket (typical investor) |
| Depreciation | 2.5% of building value | ATO — Division 43 capital works deduction (post-1985 buildings) |
| Negative gearing (AU) | Loss offsets other income — being wound back | Treasury Laws Amendment (Tax Reform No. 1) Act 2026 (Act No. 49, Royal Assent 26 Jun 2026). Negative gearing limited to new builds/BTR for contracts after 12 May 2026; established-property contracts after that date lose the salary-offset from the 2027-28 income year; pre-12-May contracts grandfathered. 50% CGT discount simultaneously replaced with cost-base indexation + 30% minimum tax. Modelled via the "established property bought after 12 May 2026" toggle (zeros the AU tax benefit when on) |
| Ring-fencing (NZ) | Rental losses ring-fenced since 2019 | IRD — ring-fencing of residential rental deductions |
| Interest deductibility (NZ) | Restored April 2025 | IRD — interest limitation rules, restored under National-led government |
| Capital growth assumption | 4%/yr | CoreLogic long-run house price growth (nominal), used for capital growth context only |
| LVR assumption | 60% | Typical established investor — some equity built up. New buyers would be 80%+ |

## Policy Scenarios

| Scenario | Parameters | Source |
|----------|------------|--------|
| NZ Greens — 2% rent cap | Max 2%/yr rent increase | RNZ, rnz.co.nz/news/political/590598 |
| CPI-linked cap | Rent rises capped at CPI | General policy concept — variants proposed in AU (VIC, QLD) and NZ |
| Rent freeze | No rent increases for 5 years | General policy concept — variations implemented in Scotland (2022-2024), proposed in AU/NZ |

## Historical Presets

| Preset | Rate change | Insurance | Prop value | Inflation | Pass-through | Basis |
|--------|-------------|-----------|------------|-----------|--------------|-------|
| 2019 Baseline | -1.80% | 0% | 0% | 2% | 100% | RBA pre-COVID rate (~1.0%), CPI ~2% |
| COVID Era | -4.80% | +5% | +15% | 2% | 100% | RBA emergency rate (0.1%), property boom |
| 2023 Peak | +0.20% | +15% | +5% | 7% | 110% | RBA post-hike (~4.35%), high CPI |
| Current 2026 | 0% | 0% | 0% | 4% | 100% | RBA holds, moderate CPI |
| QLD Cyclone | 0% | +80% | 0% | 4% | 120% | North QLD cyclone insurance premiums, ACCC data |
| NZ Earthquake | 0% | +100% | -5% | 4% | 110% | Post-EQ Canterbury/Wellington insurance spikes |

## Reform/Policy References

| Region | Reform | Source |
|--------|--------|--------|
| NSW | No-grounds evictions ended | NSW Residential Tenancies Amendment Act 2024 |
| NSW | Rent increases limited to once per year | NSW Fair Trading |
| NSW | Portable bond scheme introduced | NSW Govt announcement 2024 |
| VIC | No-grounds evictions ended | VIC Residential Tenancies Act amendments 2021 |
| VIC | COVID debt levy on land tax (2024-2033) | SRO Victoria |
| VIC | VRLT expanded statewide Jan 2025 | SRO Victoria — Vacant Residential Land Tax |
| QLD | Rent bidding banned | QLD Housing Legislation Amendment Act 2024 |
| QLD | Minimum housing standards introduced | QLD Residential Tenancies Authority |
| SA | Major tenancy reform 2024 | SA Residential Tenancies (Miscellaneous) Amendment Act 2024 |
| WA | Pet rights legislation | WA Residential Tenancies Amendment Act 2024 |
| NZ | Letting fee ban (2019) | NZ Residential Tenancies Amendment Act 2019 |
| NZ | Healthy Homes standards mandatory | MBIE Healthy Homes Standards (compliance from Jul 2025) |
| NZ | Bright-line test reduced to 2 years | IRD — Taxation (Annual Rates etc) Act 2024 |
| NZ | Interest deductibility restored (April 2025) | IRD — interest limitation rules |

---

## Notes

- AU figures are in AUD, NZ figures are in NZD
- "Typical" means representative of a median-priced property in that region — actual costs vary significantly by suburb, property age, and condition
- Insurance risk multipliers are relative to a national baseline (1.0x = national average)
- Council rates are indicative — actual rates depend on council area, property valuation, and rating category
- Tax calculations are simplified — actual tax outcomes depend on individual circumstances
- Data was assembled from publicly available sources in March 2026. Some figures (particularly rents and property values) change quarterly

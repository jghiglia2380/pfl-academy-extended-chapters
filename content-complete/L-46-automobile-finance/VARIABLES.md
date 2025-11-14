# L-46 State-Specific Variables

This document lists all template variables used in L-46 that require state-specific data.

## Automotive Variables

| Variable | Description | Typical Range | Example (Texas) |
|----------|-------------|---------------|-----------------|
| `{{STATE_SALES_TAX}}` | Sales tax rate on vehicles (%) | 0-10% | 6.25 |
| `{{STATE_REGISTRATION_INITIAL}}` | Initial title & registration fee ($) | $200-$500 | $350 |
| `{{STATE_REGISTRATION_ANNUAL}}` | Annual registration renewal fee ($) | $50-$150 | $75 |
| `{{STATE_INSURANCE_AVG_TEEN}}` | Average monthly insurance for teens/young drivers ($) | $200-$600 | $425 |
| `{{STATE_LEASE_ACQUISITION_FEE}}` | Typical lease acquisition fee ($) | $400-$900 | $695 |
| `{{STATE_INSPECTION_REQUIRED}}` | Emissions/safety inspection required (yes/no) | yes or no | yes |
| `{{STATE_INSPECTION_COST}}` | Cost of inspection if required ($) | $15-$75 | $25 |
| `{{STATE_INSURANCE_COMPARISON_URL}}` | State insurance comparison website | URL | https://www.tdi.texas.gov |

## Financial Variables

| Variable | Description | Typical Range | Example (Texas) |
|----------|-------------|---------------|-----------------|
| `{{STATE_AVG_AUTO_LOAN_RATE_NEW}}` | Average auto loan rate for new cars (%) | 3-8% | 5.8 |
| `{{STATE_AVG_AUTO_LOAN_RATE_USED}}` | Average auto loan rate for used cars (%) | 4-10% | 7.2 |
| `{{STATE_GAS_PRICE_CURRENT}}` | Current average gas price ($/gallon) | $2.50-$5.00 | $2.89 |

## State Information

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_NAME}}` | Full state name | Texas |
| `{{STATE_CODE}}` | Two-letter state code | TX |
| `{{STATE_DMV_URL}}` | State DMV website | https://www.txdmv.gov |
| `{{STATE_CONSUMER_PROTECTION_URL}}` | Consumer protection resources | https://www.texasattorneygeneral.gov |

## Usage Notes

- All percentage variables should be stored as numbers (6.25, not "6.25%")
- All dollar amount variables should be stored as numbers without $ symbol
- URLs should include full https:// protocol
- Boolean values (inspection_required) should be stored as true/false for programmatic use

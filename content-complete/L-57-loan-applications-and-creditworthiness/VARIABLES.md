# L-57 State-Specific Variables

This document lists all template variables used in L-57 that require state-specific data.

## Lending and Finance Variables

| Variable | Description | Typical Range | Example (Texas) |
|----------|-------------|---------------|-----------------|
| `{{STATE_AVG_AUTO_LOAN_RATE_NEW}}` | Average auto loan rate for new cars (%) | 3-8% | 5.8 |
| `{{STATE_AVG_AUTO_LOAN_RATE_USED}}` | Average auto loan rate for used cars (%) | 4-10% | 7.2 |
| `{{STATE_AVG_MORTGAGE_RATE_30YR}}` | Average 30-year fixed mortgage rate (%) | 5-8% | 6.75 |
| `{{STATE_MEDIAN_HOME_PRICE}}` | Median home sale price ($) | $150,000-$500,000+ | $295,000 |
| `{{STATE_MEDIAN_HOUSEHOLD_INCOME}}` | Median household income ($) | $45,000-$85,000 | $67,000 |

## Consumer Protection Resources

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_NAME}}` | Full state name | Texas |
| `{{STATE_CODE}}` | Two-letter state code | TX |
| `{{STATE_CONSUMER_PROTECTION_URL}}` | State consumer protection office website | https://www.texasattorneygeneral.gov |
| `{{STATE_CREDIT_UNION_ASSOCIATION_URL}}` | State credit union association website | https://www.tcul.coop |

## First-Time Borrower Programs

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_FIRST_TIME_HOMEBUYER_PROGRAM}}` | State first-time homebuyer assistance program name | Texas State Affordable Housing Corporation |
| `{{STATE_FIRST_TIME_HOMEBUYER_URL}}` | Program website URL | https://www.tsahc.org |
| `{{STATE_DOWN_PAYMENT_ASSISTANCE_AVAILABLE}}` | Whether state offers down payment assistance (yes/no) | yes |

## Local Nonprofit Resources

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{LOCAL_CREDIT_UNION_NAME}}` | Local credit union known for first-time borrower programs | University Federal Credit Union |
| `{{LOCAL_NONPROFIT_CREDIT_COUNSELING}}` | HUD-approved credit counseling agency | Texas Credit Union Counseling Services |
| `{{LOCAL_NONPROFIT_CREDIT_COUNSELING_URL}}` | Agency website | https://www.tcucs.org |

## Lending Regulations (Optional - for states with unique rules)

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_PAYDAY_LENDING_STATUS}}` | Regulation status of payday lenders | Allowed with restrictions |
| `{{STATE_MAX_INTEREST_RATE_CAP}}` | Usury cap on interest rates, if any | No specific cap (varies by loan type) |
| `{{STATE_COOLING_OFF_PERIOD}}` | Required waiting period for certain loans (if any) | N/A for most loans |

## Usage Notes

- All percentage variables should be stored as numbers (5.8, not "5.8%")
- All dollar amount variables should be stored as numbers without $ symbol or commas
- URLs should include full https:// protocol
- Boolean values should be stored as true/false or yes/no consistently
- For states without specific programs, use "Contact state housing authority" or similar generic guidance

## Context-Specific Usage

### In Student Content (Day 1 & Day 2):
The loan application process is largely universal, but examples become more relatable with local data:
- Mortgage examples: "In {{STATE_NAME}}, the median home price is ${{STATE_MEDIAN_HOME_PRICE}}, which means first-time buyers typically need a down payment of ${{CALCULATED: MEDIAN_HOME_PRICE * 0.10}} for 10% down."
- Interest rate examples: "Current average auto loan rates in {{STATE_NAME}} are approximately {{STATE_AVG_AUTO_LOAN_RATE_NEW}}% for new cars and {{STATE_AVG_AUTO_LOAN_RATE_USED}}% for used cars."

### In Teacher Guides:
- Reference local resources: "In {{STATE_NAME}}, students can find consumer protection resources at {{STATE_CONSUMER_PROTECTION_URL}} if they encounter predatory lending."
- First-time borrower programs: "{{STATE_NAME}} offers the {{STATE_FIRST_TIME_HOMEBUYER_PROGRAM}} which provides down payment assistance and competitive rates for qualifying first-time homebuyers."

### In Interactive Tools:
- Loan Application Simulator: Pre-populate interest rate ranges with state averages
- Creditworthiness Improvement Planner: Link to {{STATE_CREDIT_UNION_ASSOCIATION_URL}} for local first-time borrower resources
- Documentation Checklist: Reference state-specific requirements if any (most are universal)

## Data Sources for Annual Updates

To update these variables annually:

1. **Interest Rates**:
   - Federal Reserve Economic Data (FRED): https://fred.stlouisfed.org
   - Bankrate.com state-by-state rate surveys
   - State banking associations

2. **Home Prices**:
   - National Association of Realtors (NAR) state median price reports
   - Zillow Home Value Index by state
   - State real estate associations

3. **Consumer Protection Resources**:
   - State attorney general offices
   - State department of financial institutions
   - Consumer Financial Protection Bureau (CFPB) state resource lists

4. **First-Time Buyer Programs**:
   - State housing finance agencies
   - HUD state-by-state program directory
   - National Council of State Housing Agencies (NCSHA)

5. **Credit Counseling Agencies**:
   - HUD-approved counseling agency list (searchable by state)
   - National Foundation for Credit Counseling (NFCC) member agencies

## New Variables Needed for L-57 (Not in L-46)

The following variables are specific to L-57 and not present in the L-46 automobile finance chapter:

- `{{STATE_AVG_MORTGAGE_RATE_30YR}}` - Mortgage rates relevant for mortgage application examples
- `{{STATE_MEDIAN_HOME_PRICE}}` - Contextualizes mortgage examples for local market
- `{{STATE_MEDIAN_HOUSEHOLD_INCOME}}` - Helps assess whether borrower income is typical for state
- `{{STATE_FIRST_TIME_HOMEBUYER_PROGRAM}}` - Specific program name for local reference
- `{{STATE_FIRST_TIME_HOMEBUYER_URL}}` - Resource for students planning to buy homes
- `{{STATE_DOWN_PAYMENT_ASSISTANCE_AVAILABLE}}` - Helps students understand local opportunities
- `{{LOCAL_CREDIT_UNION_NAME}}` - Specific institution students can actually visit
- `{{LOCAL_NONPROFIT_CREDIT_COUNSELING}}` - Real resource for students needing help
- `{{LOCAL_NONPROFIT_CREDIT_COUNSELING_URL}}` - Direct access to assistance

## Implementation Priority

**Tier 1 (Essential):** Must have for chapter to function properly with local relevance
- `{{STATE_NAME}}`
- `{{STATE_CONSUMER_PROTECTION_URL}}`
- `{{STATE_AVG_AUTO_LOAN_RATE_NEW}}`
- `{{STATE_AVG_AUTO_LOAN_RATE_USED}}`
- `{{STATE_AVG_MORTGAGE_RATE_30YR}}`

**Tier 2 (Highly Recommended):** Significantly enhances local relevance
- `{{STATE_MEDIAN_HOME_PRICE}}`
- `{{STATE_CREDIT_UNION_ASSOCIATION_URL}}`
- `{{STATE_FIRST_TIME_HOMEBUYER_PROGRAM}}`
- `{{LOCAL_NONPROFIT_CREDIT_COUNSELING}}`

**Tier 3 (Nice to Have):** Adds additional context where available
- `{{STATE_MEDIAN_HOUSEHOLD_INCOME}}`
- `{{STATE_PAYDAY_LENDING_STATUS}}`
- `{{LOCAL_CREDIT_UNION_NAME}}`

For MVP implementation, Tier 1 variables are sufficient. Tier 2 and 3 can be added as state data layers are built out.

## Fallback Content for Missing Variables

If state-specific data is not available, use these fallback approaches:

**For Interest Rates:**
"Current national average auto loan rates are approximately 5-7% for new cars and 6-9% for used cars. Check with local lenders for current rates in your area."

**For Home Prices:**
"Median home prices vary widely by location, from under $200,000 in some markets to over $500,000 in others. Research your local market using resources like Realtor.com or Zillow."

**For Consumer Protection:**
"Contact your state attorney general's office or visit consumerfinance.gov for consumer protection resources."

**For First-Time Buyer Programs:**
"Many states offer first-time homebuyer programs with down payment assistance and competitive rates. Visit your state housing finance agency website or search '[Your State] first-time homebuyer program.'"

**For Credit Counseling:**
"Find HUD-approved credit counseling agencies at https://www.hud.gov/offices/hsg/sfh/hcc/hcs.cfm or call the National Foundation for Credit Counseling at 1-800-388-2227."

## Version History

**Version 1.0** - November 13, 2025
- Initial variable documentation for L-57
- Identified 15 state-specific variables
- 9 new variables not present in L-46
- Established tiered implementation priority

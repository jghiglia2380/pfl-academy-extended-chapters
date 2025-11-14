# L-65 State-Specific Variables

This document lists all template variables used in L-65 that require state-specific data.

## State Classification

**Tier Classification:** Tier 3 - Fully Agnostic

L-65 (Investment Portfolio Diversification) teaches universal investment principles that apply equally in all states. Portfolio diversification, asset allocation, correlation, and rebalancing are federal/national concepts not governed by state laws. Therefore, this chapter requires minimal state-specific customization.

## Optional Enhancement Variables

While the core content is universal, these optional variables can add local relevance:

### Investment Education Resources

| Variable | Description | Example (Florida) |
|----------|-------------|-------------------|
| `{{STATE_NAME}}` | Full state name | Florida |
| `{{STATE_CODE}}` | Two-letter state code | FL |
| `{{STATE_529_PLAN_NAME}}` | State 529 college savings plan name | Florida 529 Savings Plan |
| `{{STATE_529_PLAN_URL}}` | State 529 plan website | https://www.myfloridaprepaid.com |
| `{{STATE_INVESTMENT_EDUCATION_URL}}` | State securities regulator investor education page | https://www.flofr.com/education |

### Optional Financial Education Resources

| Variable | Description | Example (Florida) |
|----------|-------------|-------------------|
| `{{STATE_FINANCIAL_LITERACY_PROGRAM}}` | State financial literacy initiative (if any) | Florida Financial Lit

eracy Council |
| `{{STATE_INVESTMENT_FRAUD_HOTLINE}}` | State securities fraud reporting number | 1-800-ASK-FREC |
| `{{STATE_RETIREMENT_SYSTEM_URL}}` | Public employee retirement system (for teacher reference) | https://www.myfrs.com |

## Usage Context

### In Student Content (Day 1 & Day 2):
The chapter is designed to work without any state variables. If using them, light touches only:
- "Many states offer 529 college savings plans that provide investment options. In {{STATE_NAME}}, the {{STATE_529_PLAN_NAME}} offers target-date funds and age-based portfolios similar to what we're discussing."
- "For questions about investments or concerns about fraud, {{STATE_NAME}} residents can contact {{STATE_INVESTMENT_EDUCATION_URL}}."

### In Teacher Guides:
- Reference local 529 plans when discussing target-date funds: "Your state's 529 plan ({{STATE_529_PLAN_NAME}}) is a real-world example of age-based allocation—check {{STATE_529_PLAN_URL}} to see their investment options."
- Direct to state resources: "If students have questions about investment accounts or encounter suspicious investment offers, refer them to {{STATE_INVESTMENT_EDUCATION_URL}}."

### In Interactive Tools:
- Portfolio Diversification Builder could include link: "Learn more about 529 plans: {{STATE_529_PLAN_URL}}"
- Asset Allocation Optimizer could reference: "Many state 529 plans offer pre-built allocations. See {{STATE_NAME}}'s options."

## Implementation Notes

**Minimal Variables Needed:**
Given L-65's universal nature, only 2-3 variables add meaningful value:
1. `{{STATE_NAME}}` - For personalizing examples
2. `{{STATE_529_PLAN_NAME}}` and `{{STATE_529_PLAN_URL}}` - Real-world connection to target-date/age-based investing

**All Others Optional:** Investment principles (diversification, correlation, allocation, rebalancing) are identical across all states.

## Fallback Content (If Variables Not Available)

If state-specific data is unavailable, use national resources:

**For 529 Plans:**
"Most states offer 529 college savings plans with investment options ranging from age-based portfolios (that automatically rebalance) to individual fund selections. Visit savingforcollege.com to explore options."

**For Investment Education:**
"The SEC's Investor.gov (https://investor.gov) provides free investment education resources. FINRA's Investor Education Foundation (https://finra.org/investors) offers tools and calculators."

**For Fraud Prevention:**
"Report investment fraud to the SEC (sec.gov/complaint) or FINRA (finra.org/investors/file-complaint). Never invest based on unsolicited offers or pressure tactics."

## Why So Few Variables?

Unlike chapters on taxes (L-6), insurance (L-33-35), or housing (L-30-32) that have significant state-level variation, investment concepts are governed by federal securities laws and operate nationally. Key concepts in L-65:

- **Correlation** between asset classes: Same nationwide
- **Asset allocation strategies**: Universal principles based on age and risk tolerance
- **Rebalancing mechanics**: Independent of location
- **Modern Portfolio Theory**: Mathematical framework, not jurisdiction-specific
- **Target-date funds**: Operate the same in all states
- **Investment account types** (401(k), IRA, taxable): Federal tax code, not state-specific

The only meaningful state variation relates to:
1. **529 Plans:** Each state sponsors its own, but residents can use any state's plan
2. **State Retirement Systems:** Relevant for public employees (teachers, government workers)
3. **State Securities Regulators:** Investor protection and education resources

## New Variables for L-65 (Not in Previous Chapters)

- `{{STATE_529_PLAN_NAME}}` - Specific to college savings, relevant for age-based allocation discussion
- `{{STATE_529_PLAN_URL}}` - Direct resource link
- `{{STATE_INVESTMENT_EDUCATION_URL}}` - State securities regulator education page
- `{{STATE_FINANCIAL_LITERACY_PROGRAM}}` - Some states have formal initiatives
- `{{STATE_INVESTMENT_FRAUD_HOTLINE}}` - Investor protection resource
- `{{STATE_RETIREMENT_SYSTEM_URL}}` - For teacher/public employee relevance

Total new variables: 6 (all optional)

## Data Sources for Annual Updates

**529 Plan Information:**
- Savingforcollege.com (comprehensive 529 plan database)
- Individual state treasury or education department websites
- CSPN (College Savings Plan Network): https://www.collegesavings.org

**State Securities Regulators:**
- NASAA (North American Securities Administrators Association): https://www.nasaa.org
- State-by-state securities regulator directory
- Most states: Secretary of State office or Department of Financial Institutions

**Financial Literacy Programs:**
- Jump$tart Coalition state partner directory
- National Financial Educators Council state programs
- State education department financial literacy initiatives

## Version History

**Version 1.0** - November 13, 2025
- Initial variable documentation for L-65
- Identified as Tier 3 (Fully Agnostic) chapter
- 6 optional enhancement variables documented
- Minimal state customization needed due to universal investment concepts

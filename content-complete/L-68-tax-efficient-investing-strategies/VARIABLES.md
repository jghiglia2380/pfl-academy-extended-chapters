# L-68: Tax-Efficient Investing Strategies - State-Specific Variables

## Classification: Tier 2 - Moderate State Variation

**Rationale:** This chapter focuses primarily on federal tax treatment of investments, which applies universally across all states. However, state income tax rates and state-specific treatment of retirement accounts and investment income create meaningful variations that enhance the lesson's relevance when customized for specific states.

The core content and strategies (Roth vs. traditional choice, asset location, tax-loss harvesting, holding period optimization) remain highly valuable regardless of state tax variations. State-specific customization amplifies the benefits in high-tax states and acknowledges the simpler landscape in no-tax states, but does not fundamentally change the teaching approach or learning objectives.

## Federal Foundation (Universal - No State Variation)

The following content applies identically in all states and requires no customization:

### Federal Tax Treatment (Universal)
- **Federal income tax brackets:** 10%, 12%, 22%, 24%, 32%, 35%, 37%
- **Long-term capital gains rates:** 0%, 15%, 20% (based on taxable income thresholds)
- **Qualified dividend tax rates:** Same as long-term capital gains (0%, 15%, 20%)
- **Short-term capital gains:** Taxed as ordinary income (10-37%)
- **Non-qualified dividends:** Taxed as ordinary income
- **Interest income:** Taxed as ordinary income
- **Wash sale rule:** 30 days before and after sale (61-day window)
- **Capital loss limitations:** $3,000 annual offset against ordinary income; unlimited offset against capital gains
- **Retirement account rules:**
  - Traditional IRA/401(k): Tax-deductible contributions, tax-deferred growth, taxed at ordinary income rates upon withdrawal
  - Roth IRA/401(k): After-tax contributions, tax-free growth, tax-free qualified withdrawals
  - Required Minimum Distributions (RMDs): Begin at age 73 for traditional accounts
  - Early withdrawal penalties: 10% penalty before age 59½ (with exceptions)

### Core Strategies (Universal)
- **Roth vs. Traditional decision framework:** Based on current vs. expected future tax rates
- **Asset location principles:** Tax-inefficient assets in tax-advantaged accounts; tax-efficient assets in taxable accounts
- **Tax-loss harvesting mechanics:** Sell losses to offset gains and income
- **Holding period optimization:** Hold ≥1 year for long-term capital gains treatment
- **Strategic gain recognition:** Use 0% capital gains bracket during low-income years

**Teaching Approach:** Teach all federal content as presented in the curriculum. This forms the foundation and applies to all students.

## State-Specific Variables

### Variable 1: State Income Tax Rates

**States with No Income Tax (9 states):**
- Alaska, Florida, Nevada, New Hampshire*, South Dakota, Tennessee*, Texas, Washington, Wyoming
- *NH taxes dividends and interest only (not employment income); TN repealed its Hall Tax on investment income as of 2021

**Teaching Adjustment for No-Tax States:**
- Acknowledge that tax-efficient investing remains highly valuable (federal taxes alone are substantial)
- Emphasize: "Even without state income tax, federal tax on investments can be 15-20% on gains and up to 37% on ordinary income. These strategies still add $200,000-$500,000 to lifetime wealth."
- Simplified messaging: Focus on federal optimization without state tax complications
- Example: "In Texas, you don't pay state income tax, but you'll still pay federal taxes on all investment income. A 15% federal capital gains rate on $100,000 in gains is $15,000 in taxes—tax-efficient strategies can reduce or defer this."

**High State Income Tax States (Top marginal rate >8%):**
- California (13.3%), Hawaii (11%), New York (10.9%), New Jersey (10.75%), Oregon (9.9%), Minnesota (9.85%), District of Columbia (10.75%), Vermont (8.75%), Iowa (8.53%), Wisconsin (7.65%)

**Teaching Adjustment for High-Tax States:**
- Emphasize that tax efficiency is even more critical
- Provide combined federal + state rate examples to show the cumulative impact
- Example: "In California, the top combined rate on ordinary income is 50.3% (37% federal + 13.3% state). The combined long-term capital gains rate is 33.3% (20% federal + 13.3% state). That's a 17 percentage point difference—holding investments for at least one year saves 17% in taxes on every dollar of gain."
- Highlight: "Asset location is especially valuable in high-tax states. Bond interest taxed as ordinary income at 50%+ (combined) vs. qualified dividends taxed at 28-33% (combined) makes sheltering bonds in retirement accounts worth thousands more annually."

**Moderate State Income Tax States (Top marginal rate 3-8%):**
- Most other states fall in this range
- Standard teaching approach applies; can mention combined rates if helpful for context

**Variable to Use:**
```
STATE_INCOME_TAX_RATE = [State's top marginal rate]
COMBINED_ORDINARY_INCOME_RATE_HIGH_EARNER = 37% (federal) + STATE_INCOME_TAX_RATE
COMBINED_LONG_TERM_GAINS_RATE_HIGH_EARNER = 20% (federal) + STATE_CAPITAL_GAINS_RATE
```

**Example Calculations (California):**
- Ordinary income: 37% + 13.3% = 50.3%
- Long-term capital gains: 20% + 13.3% = 33.3%
- Tax advantage of long-term holding: 17 percentage points
- Bond interest (ordinary) vs. qualified dividends: 50.3% vs. 33.3% = 17 percentage point difference

### Variable 2: State Treatment of Retirement Accounts

**Most States (Standard Treatment):**
- Follow federal rules: Traditional IRA/401(k) contributions may be deductible; Roth contributions are not deductible
- Traditional withdrawals are taxable at state rates; Roth withdrawals are tax-free

**Teaching Adjustment:** Standard curriculum applies as written.

**States with Favorable Retirement Income Treatment:**

**Pennsylvania:**
- Does NOT tax any retirement account distributions (traditional or Roth)
- Traditional IRA/401(k) withdrawals are state-tax-free
- Teaching Adjustment: "In Pennsylvania, traditional retirement account withdrawals aren't taxed at the state level. This makes traditional accounts relatively more attractive compared to other states. The federal Roth vs. traditional analysis still applies, but Pennsylvania residents get an extra benefit from traditional accounts."
- Example: "If you withdraw $50,000/year from a traditional IRA in retirement, you'd pay federal taxes but $0 in Pennsylvania state taxes. In a state with 5% tax, you'd pay $2,500 in state taxes. This tilts the decision slightly toward traditional for PA residents."

**Alabama, Illinois, Mississippi:**
- Exclude some or all retirement income from state taxation
- Teaching Adjustment: "Your state provides tax breaks for retirement income, making traditional accounts more valuable relative to states that fully tax retirement distributions."

**States that Tax Roth Conversions as Income:**
- Most states follow federal treatment (Roth conversions are taxable income in the year of conversion)
- Teaching Adjustment (if relevant): "When you convert from traditional to Roth, you'll pay both federal and state taxes on the converted amount. In low-income years, this can still be valuable, but factor in both tax levels."

**Variable to Use:**
```
STATE_TAXES_RETIREMENT_DISTRIBUTIONS = Yes / No / Partial
STATE_RETIREMENT_INCOME_EXCLUSION = $[amount] (if applicable)
```

**Example (Pennsylvania):**
```
STATE_TAXES_RETIREMENT_DISTRIBUTIONS = No
STATE_RETIREMENT_INCOME_EXCLUSION = Unlimited (all retirement income excluded)
```

**Example (Illinois):**
```
STATE_TAXES_RETIREMENT_DISTRIBUTIONS = No (for qualified retirement plans)
STATE_RETIREMENT_INCOME_EXCLUSION = Unlimited (for qualified plans)
```

### Variable 3: State Capital Gains Treatment

**Most States:**
- Tax capital gains as ordinary income (use the same tax brackets as employment income)

**Teaching Adjustment:** Standard curriculum applies.

**States with Preferential Capital Gains Treatment:**
- Some states provide lower rates or exemptions for long-term capital gains
- Example: Wisconsin has a 30% exclusion for long-term capital gains (effectively reducing the rate)

**Teaching Adjustment (if applicable):** "Your state provides preferential treatment for long-term capital gains, making the 1-year holding period even more valuable."

**Variable to Use:**
```
STATE_CAPITAL_GAINS_RATE = Same as ordinary income / Preferential rate / [Specify if different]
```

### Variable 4: Municipal Bond Considerations

**All States:**
- Municipal bond interest is federally tax-free
- Municipal bond interest from bonds issued by your own state is typically state-tax-free as well
- Municipal bond interest from other states is typically subject to state tax

**Teaching Adjustment for High-Tax States:**
- Municipal bonds become more attractive for high-income investors in taxable accounts
- Example: "In California, a high-income investor in the 13.3% state bracket and 37% federal bracket faces a 50.3% combined rate on ordinary income. A California municipal bond yielding 3% tax-free is equivalent to a taxable bond yielding 6% (3% / (1 - 0.503) = 6.04%)."

**Variable to Use:**
```
STATE_TAX_ON_IN_STATE_MUNIS = 0% (tax-free)
STATE_TAX_ON_OUT_OF_STATE_MUNIS = STATE_INCOME_TAX_RATE
```

**Teaching Note:** Municipal bonds are an advanced topic; mention briefly for high-income students in high-tax states but don't emphasize for the general audience.

## State-Specific Teaching Approach

### For Teachers in No-Tax States (AK, FL, NV, SD, TX, WA, WY, etc.)

**Approach:**
1. Teach all federal content as written (fully applicable)
2. Acknowledge the state tax advantage: "You're fortunate to live in a state with no income tax, which means you only need to optimize for federal taxes."
3. Emphasize that federal tax efficiency alone adds $200,000-$500,000 to lifetime wealth
4. Simplified examples: Use only federal tax rates in calculations
5. Asset location still highly valuable: "Even with no state tax, bond interest at 37% federal vs. qualified dividends at 15-20% federal is a significant difference worth optimizing."

**Student Examples (Texas resident):**
- Roth vs. Traditional: Based on federal brackets only (12% now vs. 22% in retirement)
- Asset location: Federal rates only (bond interest 24% federal vs. qualified dividends 15% federal)
- Tax-loss harvesting: Federal tax savings only ($1,500 loss × 15% federal = $225 savings)

### For Teachers in High-Tax States (CA, NY, NJ, HI, OR, MN, etc.)

**Approach:**
1. Teach all federal content as foundation
2. Emphasize increased urgency: "Tax efficiency is even more critical in [State] due to high state income taxes."
3. Provide combined federal + state examples to show cumulative impact
4. Highlight asset location as especially valuable (show dollar impact with state rates included)
5. Mention municipal bonds for high-income students

**Student Examples (California resident):**
- Roth vs. Traditional: Combined rates (12% federal + 9.3% state = 21.3% now vs. 22% federal + 9.3% state = 31.3% in retirement if income is higher)
- Asset location: Combined rates (bond interest 24% federal + 9.3% state = 33.3% vs. qualified dividends 15% federal + 9.3% state = 24.3%)
- Tax-loss harvesting: Combined savings ($1,500 loss × 24.3% combined = $365 savings)
- Note: "Asset location saving you $200/year in federal taxes saves you an additional $78/year in California state taxes—$278 total annual savings."

### For Teachers in States with Retirement Income Exclusions (PA, IL, MS, AL, etc.)

**Approach:**
1. Teach standard federal content
2. Explain state-specific retirement income treatment
3. Adjust Roth vs. Traditional guidance: "Traditional accounts are relatively more attractive in [State] because withdrawals aren't subject to state tax."
4. Quantify the benefit: "If you withdraw $50,000/year in retirement, you save $[state tax amount] annually compared to states that tax retirement income."
5. Emphasize that federal analysis still dominates the decision

**Student Examples (Pennsylvania resident):**
- Roth vs. Traditional: "Traditional gives you a deduction at 12% federal + 3.07% state = 15.07% now. In retirement, you pay 22% federal but 0% state = 22% total. Without Pennsylvania's retirement income exclusion, you'd pay 22% federal + 3.07% state = 25.07%. Pennsylvania saves you 3.07 percentage points on all retirement withdrawals."

### For Teachers in Moderate-Tax States

**Approach:**
1. Standard curriculum as written
2. Optionally mention combined federal + state rates for context
3. Keep focus on federal optimization (provides most of the benefit)

## Example State Customizations

### California Customization:

**Roth vs. Traditional Example (Day 1):**
"A 25-year-old California resident earning $50,000 is in the 12% federal bracket and 9.3% California bracket (combined 21.3%). If they contribute $6,000 to a traditional IRA, they save $1,278 in combined taxes now (12% × $6,000 federal + 9.3% × $6,000 state). However, if they're in the 22% federal and 9.3% state bracket in retirement (combined 31.3%), they'll pay $375,000+ in combined taxes on $1.2 million in retirement wealth. A Roth contribution costs $1,278 in taxes now but saves $375,000 later—massive Roth advantage, even more pronounced in California than in no-tax states."

**Asset Location Example (Day 2):**
"Bonds in a taxable account generate $1,200 in interest taxed at 24% federal + 9.3% California = 33.3% combined = $400/year in taxes. Stocks generating $600 in qualified dividends are taxed at 15% federal + 9.3% California = 24.3% combined = $146/year. By placing bonds in your traditional IRA and stocks in taxable, you save $254/year in taxes. Over 30 years with compounding, that's $25,000+ in additional wealth just from optimal placement."

### Texas Customization:

**Roth vs. Traditional Example (Day 1):**
"A 25-year-old Texas resident earning $50,000 is in the 12% federal bracket with no state income tax. Contributing $6,000 to a traditional IRA saves $720 in federal taxes now. In retirement at 22% federal bracket, you'd pay $264,000 in federal taxes on $1.2 million. A Roth costs $720 now but saves $264,000 later. Since Texas has no state tax, the analysis is simpler and focuses purely on federal rates."

**Asset Location Example (Day 2):**
"Bonds generating $1,200 in interest are taxed at 24% federal = $288/year (no state tax to add). Stocks generating $600 in qualified dividends are taxed at 15% federal = $90/year. Optimal asset location saves $198/year in federal taxes—still highly valuable even without state tax complications."

### Pennsylvania Customization:

**Roth vs. Traditional Example (Day 1):**
"A 25-year-old Pennsylvania resident earning $50,000 is in the 12% federal and 3.07% state bracket (combined 15.07%). Contributing $6,000 to a traditional IRA saves $904 in combined taxes now. In retirement, Pennsylvania doesn't tax retirement distributions, so you'd pay only 22% federal (not 22% + 3.07% state) on withdrawals. This makes traditional accounts more attractive in Pennsylvania than in states that tax retirement income. However, for young investors in low brackets, Roth often still wins due to tax-free compounding over 40 years."

## Implementation Recommendations

### Minimal Customization Approach (Recommended for Most Teachers):
1. Teach federal content as written (universal and most impactful)
2. Add one verbal acknowledgment: "Your state [has no income tax / has high income tax / doesn't tax retirement distributions], which [simplifies the analysis / makes tax efficiency even more valuable / makes traditional accounts slightly more attractive]."
3. For calculations, use federal rates only (keeps complexity manageable)
4. Provide one state-specific example if it significantly changes the analysis

### Moderate Customization Approach (for teachers comfortable with state tax details):
1. Create a one-page state supplement showing:
   - State income tax brackets
   - State treatment of retirement distributions
   - State capital gains treatment
   - Combined federal + state rates for common brackets
2. Use combined rates in examples during Day 2 Learning Lab
3. Adjust Roth vs. traditional guidance based on state retirement income treatment

### Full Customization Approach (for advanced financial education programs):
1. Integrate state tax rates throughout curriculum
2. All calculations show both federal and state taxes
3. State-specific Tax Efficiency Optimizer module
4. State-specific examples and case studies
5. Municipal bond discussion for high-tax states

## State-Specific Variable Template

For teachers creating state-specific materials, use this template:

```
STATE: [State Name]

STATE INCOME TAX:
- Top marginal rate: [____%]
- Brackets: [List if providing detailed state content]
- No income tax: [Yes/No]

RETIREMENT ACCOUNT TREATMENT:
- Traditional contributions: [Deductible/Not deductible/Partially deductible]
- Traditional withdrawals: [Taxable/Tax-free/Partially taxable]
- Roth contributions: [Deductible/Not deductible] (almost always not deductible)
- Roth withdrawals: [Taxable/Tax-free] (almost always tax-free)

CAPITAL GAINS TREATMENT:
- Long-term capital gains: [Taxed as ordinary income / Preferential rate of ____%]
- Short-term capital gains: [Taxed as ordinary income]

MUNICIPAL BONDS:
- In-state muni interest: [Tax-free/Taxable]
- Out-of-state muni interest: [Tax-free/Taxable]

COMBINED TAX RATES (High Earners):
- Ordinary income: 37% federal + ____% state = ____%
- Long-term capital gains: 20% federal + ____% state = ____%
- Difference: ____ percentage points

TEACHING ADJUSTMENTS:
1. [Primary adjustment based on state tax structure]
2. [Secondary consideration]
3. [Example modifications for student calculations]
```

## Annual Updates Required

**State Tax Rates:**
- State income tax brackets may change annually (inflation adjustments, legislative changes)
- Review state tax authority websites each fall
- Update state-specific materials by January of each year

**Retirement Account Treatment:**
- Occasionally states change how they tax retirement income
- Monitor state legislation affecting retirement taxation
- Update materials if changes occur

**Update Timeline:**
- November: Review IRS and state tax authority announcements
- December: Update all rate tables and examples
- January: Distribute updated materials before spring semester

## Summary

L-68 Tax-Efficient Investing Strategies is classified as **Tier 2** because the core federal content is universally applicable and highly valuable regardless of state tax variations. State customization enhances relevance and precision but is not essential for students to gain the critical knowledge and skills.

**Core Message (Universal):**
- Tax-efficient investing can add $200,000-$500,000 to lifetime wealth through smart account selection, asset location, tax-loss harvesting, and holding period optimization
- Roth vs. traditional depends on current vs. future tax rates
- Asset location places tax-inefficient investments in tax-advantaged accounts
- Holding investments ≥1 year saves 9-17 percentage points in federal taxes

**State Variations:**
- No-tax states: Simpler analysis, federal optimization only, still highly valuable
- High-tax states: Even more critical, combined rates amplify benefits, municipal bonds relevant for high earners
- States with retirement income exclusions: Traditional accounts relatively more attractive

**Teaching Recommendation:**
Teach federal content to all students (provides 80%+ of the value), then add brief state-specific context relevant to your students' location. This approach maximizes learning efficiency while maintaining accuracy and relevance.

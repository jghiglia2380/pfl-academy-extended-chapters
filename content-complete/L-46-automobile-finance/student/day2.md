# L-46: Automobile Finance - Buying vs. Leasing - Learning Lab

> **Implementation Note:**
> Use the standardized header template (templates/student-header-template.html) for consistent styling.

## Learning Lab Overview
- **L-Chapter:** L-46: Automobile Finance - Buying vs. Leasing
- **Duration:** 55 minutes
- **Focus:** Hands-on analysis of real vehicle financing scenarios with decision-making tools
- **Learning Format:** 90% activities, 10% facilitation and reflection

## Materials Needed
- Auto Finance Decision Calculator (accessible via learning platform)
- Vehicle research data (internet access)
- Loan amortization calculator
- Vehicle Financing Decision Matrix worksheet
- Budget integration worksheet

## Pre-Class Setup
1. Complete Day 1 content review
2. Research one vehicle of interest (new price, used price, lease offer)
3. Bring personal budget information (if comfortable sharing)

## Learning Lab Activities

### Activity 1: Real-World Vehicle Cost Breakdown (15 minutes)
**Objective:** Calculate the TRUE total cost of ownership beyond the sticker price

**Instructions:**
1. Select one of three provided vehicle profiles:
   - **Profile A**: 2024 Honda Civic (Compact sedan, $28,000 new)
   - **Profile B**: 2021 Toyota RAV4 (Used mid-size SUV, $24,000)
   - **Profile C**: 2024 Hyundai Elantra (Lease offer: $299/month, 36 months)

2. Using the Total Cost Calculator, input these state-specific factors:
   - **Sales tax**: {{STATE_SALES_TAX}}% (your state rate)
   - **Registration/title fees**: Initial ${{STATE_REGISTRATION_INITIAL}}, Annual ${{STATE_REGISTRATION_ANNUAL}}
   - **Insurance**: Research typical rates for your age/location at {{STATE_INSURANCE_COMPARISON_URL}} (average for teens: ${{STATE_INSURANCE_AVG_TEEN}}/month)
   - **Fuel costs**: Calculate based on EPA mpg × annual miles ÷ mpg × ${{STATE_GAS_PRICE_CURRENT}}/gallon
   - **Maintenance**: Use manufacturer schedule (typically $500-1000/year)

3. Calculate 6-year totals including:
   - Purchase/lease payments
   - Sales tax and fees (one-time)
   - Registration renewals (annual)
   - Insurance (annual, increases ~3% yearly)
   - Fuel (annual, adjust for inflation)
   - Scheduled maintenance
   - Estimated repairs (increase as vehicle ages)
   - Residual value at year 6

4. Create a cost-per-mile calculation: Total 6-year cost ÷ total miles driven

5. Share findings: Which profile has the lowest cost per mile? What surprised you about the total cost breakdown?

### Activity 2: Buy vs. Lease Decision Simulator (20 minutes)
**Objective:** Experience the complete financial comparison using real market data

**Instructions:**
1. Choose ONE vehicle you're genuinely interested in (research current pricing)

2. Build three complete scenarios in the Auto Finance Decision Calculator:

   **SCENARIO 1: Buy New**
   - Purchase price: [Your researched price]
   - Sales tax: {{STATE_SALES_TAX}}%
   - Registration: Initial ${{STATE_REGISTRATION_INITIAL}}, Annual ${{STATE_REGISTRATION_ANNUAL}}
   - Down payment: 20% of purchase price
   - Loan: 60 months at {{STATE_AVG_AUTO_LOAN_RATE_NEW}}%
   - Insurance: Approximately ${{STATE_INSURANCE_AVG_TEEN}}/month (get quotes from {{STATE_INSURANCE_COMPARISON_URL}})

   **SCENARIO 2: Buy Used (3 years old)**
   - Purchase price: [Research same model, 3 years old]
   - Sales tax: {{STATE_SALES_TAX}}%
   - Registration: Initial ${{STATE_REGISTRATION_INITIAL}}, Annual ${{STATE_REGISTRATION_ANNUAL}}
   - Down payment: 15% of purchase price
   - Loan: 48 months at {{STATE_AVG_AUTO_LOAN_RATE_USED}}%
   - Insurance: Typically 10-15% lower than new vehicle (estimate 85% of ${{STATE_INSURANCE_AVG_TEEN}})

   **SCENARIO 3: Lease New**
   - MSRP: [Same as Scenario 1]
   - Acquisition fee: ${{STATE_LEASE_ACQUISITION_FEE}}
   - Cap cost reduction: $2,000
   - Lease: 36 months, [research current money factor]
   - Annual miles: 12,000
   - Excess mileage charge: $0.25/mile
   - Disposition fee: $400 at end of lease

3. The calculator shows:
   - Monthly payment for each
   - Year-by-year cost breakdown
   - Equity position over time (loan balance vs. value)
   - Total 6-year net cost
   - Decision point: When does buying beat leasing?

4. Add "what-if" scenarios:
   - Scenario 3B: What if you drive 18,000 miles/year? (Add mileage overage costs)
   - Scenario 1B: What if you keep the purchased car for 10 years instead of 6?
   - Scenario 2B: What if used car needs $2,500 in unexpected repairs at year 4?

5. Document your findings:
   - Which scenario has lowest monthly payment? Lowest total cost?
   - At what point does the purchased vehicle become "free" (paid off) while leasing continues?
   - How do mileage needs affect the decision?

### Activity 3: Loan Terms Impact Analysis (15 minutes)
**Objective:** Understand how loan length affects both flexibility and total cost

**Setup:** You're buying a $26,000 vehicle (after trade-in/down payment) at {{STATE_AVG_AUTO_LOAN_RATE_NEW}}% (current average rate in {{STATE_NAME}})

**Instructions:**
1. Compare these loan structures using the Loan Terms Analyzer:
   - **Option A**: 36 months at 5.5% APR
   - **Option B**: 60 months at 6.0% APR
   - **Option C**: 72 months at 7.5% APR

2. For each option, track:
   - Monthly payment amount
   - Total interest paid over life of loan
   - Loan balance vs. vehicle value at years 1, 2, 3, 4
   - "Underwater period" (months owing more than it's worth)

3. Calculate the break-even point:
   - If you needed to sell at year 3, which option leaves you with positive equity?
   - How much extra do you pay in total interest for the longest-term loan?
   - What is the monthly savings of the longer loan vs. shortest loan?

4. Budget integration exercise:
   - If your target monthly payment is $400, which loan terms can you afford?
   - If you could afford Option A payments ($784/month) but chose Option C ($390/month), what could you do with the $394 difference?
     - Pay down credit card debt?
     - Build emergency fund?
     - Invest for retirement?
   - Use the Opportunity Cost Calculator: $394/month invested for 6 years at 7% return = $34,785

5. Reflection: When is a longer loan justified despite higher total cost? When should you avoid it?

### Activity 4: Personal Vehicle Financing Strategy (5 minutes)
**Objective:** Create your personalized decision framework

**Instructions:**
1. Complete the Vehicle Financing Decision Matrix:

   **Your Priorities** (rank 1-5):
   - [ ] Lowest monthly payment
   - [ ] Lowest total cost
   - [ ] Always having a newer vehicle
   - [ ] No car payments eventually
   - [ ] Flexibility to change vehicles frequently

   **Your Circumstances:**
   - Annual income: $________
   - Current savings: $________
   - Expected annual mileage: ________
   - Career stability: Stable / Uncertain / Changing
   - Credit score range: Excellent / Good / Fair / Building

   **State-Specific Factors:**
   - Insurance costs in {{STATE_NAME}}: Average ${{STATE_INSURANCE_AVG_TEEN}}/month for young drivers
   - Emissions/safety inspection: {{#if STATE_INSPECTION_REQUIRED}}Required (${STATE_INSPECTION_COST}} annually){{else}}Not required{{/if}}
   - Sales tax rate: {{STATE_SALES_TAX}}% (compare with neighboring states when vehicle shopping)

2. Based on your analysis from Activities 1-3, identify:
   - Recommended approach: Buy new / Buy used / Lease
   - Maximum affordable monthly payment: $________
   - Target vehicle price range: $________ to $________
   - Plan for after loan payoff: Drive 5+ more years / Trade-in / Other

3. Set your personal rules:
   - "I will not finance a vehicle for more than ___ months"
   - "I will not buy a vehicle that costs more than ___% of my annual income"
   - "I will prioritize [low payment / low total cost / reliability / features]"

## Reflection & Wrap-up (5 minutes)
1. One key insight from today: What surprised you most about the total cost analysis?
2. One action you'll take: What will you do differently when acquiring your next vehicle?
3. Share with class: Which financing approach aligns with YOUR current life stage and financial goals?

## Key Takeaways
- Monthly payment is only ONE piece of total cost of ownership
- State-specific factors (taxes, registration, insurance) add thousands to vehicle costs
- Loan term dramatically affects total interest paid and equity position
- The years of payment-free driving after loan payoff are where real savings happen
- Your personal circumstances (income, mileage, stability) should drive your financing decision
- Understanding opportunity cost helps contextualize vehicle spending within broader financial goals

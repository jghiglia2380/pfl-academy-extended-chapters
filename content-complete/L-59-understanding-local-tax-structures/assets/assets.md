# L-59 Assets: Understanding Local Tax Structures

## Overview

This chapter requires six interactive tools and multiple printable resources to support both Day 1 conceptual learning and Day 2 hands-on application. All tools integrate {{STATE_NAME}} data dynamically and allow users to edit pre-populated values. Each interactive tool has a corresponding printable PDF alternative for accessibility and technology equity.

---

## Day 1 Assets

### 1. Local Tax Impact Calculator (Primary Skill Builder)

**Purpose:**
Enable students to calculate and compare total local tax burdens across multiple jurisdictions within {{STATE_NAME}}, understanding how location decisions impact their financial obligations.

**Format:**
Interactive web-based calculator with multi-tab interface and comparison mode.

**Inputs:**
1. **Jurisdiction Selection:**
   - Dropdown menu with 20+ {{STATE_NAME}} jurisdictions pre-loaded
   - Auto-populates tax rates when selected (user can manually edit)
   - Includes major cities, suburbs, and rural areas

2. **Property Information:**
   - Property market value (numeric input: $50,000 - $2,000,000)
   - Auto-calculates assessed value using {{STATE_ASSESSMENT_PERCENTAGE}}%
   - Applies homestead exemption (${{STATE_HOMESTEAD_EXEMPTION}}) if user indicates primary residence
   - Displays millage breakdown by authority (county, city, school, special districts)

3. **Annual Spending:**
   - Estimated annual taxable purchases (numeric input: $0 - $100,000)
   - Combined sales tax rate auto-populates based on jurisdiction
   - Calculates annual sales tax paid

4. **{{#if STATE_ALLOWS_LOCAL_INCOME_TAX}}Income Information (if applicable):**
   - Annual income (numeric input: $0 - $500,000)
   - Local income tax rate auto-populates based on jurisdiction
   - Calculates annual local income tax{{/if}}

5. **Household Profile (optional):**
   - Number of adults and children
   - Adjusts estimates for typical household spending patterns

**Expected Outputs:**
1. **Annual Tax Summary:**
   - Property tax: $[amount] ($[monthly])
   - Sales tax: $[amount] ($[monthly])
   - {{#if STATE_ALLOWS_LOCAL_INCOME_TAX}}Local income tax: $[amount] ($[monthly]){{/if}}
   - **Total local tax burden:** $[amount] ($[monthly])

2. **Visual Displays:**
   - Pie chart showing tax breakdown by type
   - Bar chart comparing selected jurisdiction to {{STATE_NAME}} average
   - Monthly cost visualization with icons

3. **Service Level Information:**
   - School district rating (1-10 scale)
   - Crime rate index
   - Infrastructure quality rating
   - Parks & recreation score
   - Public transportation availability

4. **Comparison Mode:**
   - Side-by-side comparison of up to 4 jurisdictions
   - Highlight differences in red/green
   - "Best Value" recommendation based on user-defined priorities

**Interaction Model:**
1. User selects jurisdiction from dropdown → rates auto-populate
2. User enters financial information → calculator updates in real-time
3. User clicks "Add Comparison" → new column appears for second jurisdiction
4. User adjusts priority sliders (cost vs. services) → recommendation updates
5. User clicks "Save Results" → generates shareable summary
6. User clicks "Print Report" → creates PDF with all comparisons

**Design Notes:**
- **Responsive Design:** Must work on mobile, tablet, and desktop
- **Real-Time Calculation:** Update outputs instantly as inputs change
- **State Data Integration:** Pull from {{STATE_NAME}} data layer automatically
- **Edit Capability:** All auto-populated fields should be editable with "Reset to Default" button
- **Visual Hierarchy:**
  - Large, clear output numbers with $ formatting
  - Color coding: Property tax = blue, Sales tax = green, Income tax = purple
  - Icons for different tax types
- **Accessibility:**
  - Screen reader compatible
  - Keyboard navigation support
  - High contrast mode option
  - Font size adjustable
- **Error Handling:**
  - Validate numeric inputs (no negative numbers, reasonable ranges)
  - Warn if inputs seem unrealistic ("$5M property value seems high. Verify?")
  - Graceful degradation if jurisdiction data unavailable

**State Variable Integration:**
```javascript
// Auto-populate from state data layer
jurisdiction_data = {
  name: "{{STATE_MAJOR_CITY_1}}",
  property_tax_rate: {{STATE_MAJOR_CITY_1_MILLAGE}}, // mills
  sales_tax_local: {{STATE_LOCAL_SALES_TAX_1}}, // %
  income_tax_rate: {{STATE_LOCAL_INCOME_TAX_RATE_1}}, // % (if applicable)
  assessment_ratio: {{STATE_ASSESSMENT_PERCENTAGE}} / 100,
  homestead_exemption: {{STATE_HOMESTEAD_EXEMPTION}},
  school_rating: 8.5,
  crime_index: 42, // lower is better
  services_score: 85
}
```

---

## Day 2 Assets

### 2. Property Tax Bill Analyzer

**Purpose:**
Help students decode an authentic property tax bill, understanding each component and verifying calculations.

**Format:**
Interactive annotated tax bill with clickable sections and built-in verification calculator.

**Inputs:**
- Primarily viewing tool; minimal user input
- Optional: User can upload their own tax bill for analysis (advanced feature)

**Expected Outputs:**
1. **Annotated Bill Display:**
   - Authentic {{STATE_NAME}} property tax bill specimen
   - Clickable hotspots on each section revealing explanations
   - Color-coded sections: Assessed value (blue), Exemptions (green), Millage rates (orange), Total tax (red)

2. **Breakdown Panel:**
   - Assessed value explanation
   - List of all taxing authorities with their millage rates
   - Calculation verification: (Assessed Value - Exemptions) × Millage Rate = Tax
   - Allocation pie chart showing where money goes

3. **Challenge Questions:**
   - "What would your tax be if assessed value increased by $25,000?"
   - "If you qualified for an additional $10,000 exemption, how much would you save?"
   - Built-in calculator for students to answer

**Interaction Model:**
1. Bill displays with highlighted sections
2. Student clicks on "Assessed Value" → popup explains what it means
3. Student clicks on "County Tax" → popup shows millage rate and calculation
4. Student uses built-in calculator to answer verification questions
5. Feedback provided: "Correct! The tax would increase by $[amount]"

**Design Notes:**
- Use actual {{STATE_NAME}} tax bill format (generic template with real structure)
- Make bill full-size and zoomable for readability
- Provide glossary sidebar with all terms defined
- Include print-to-PDF function
- Mobile-friendly: Bill should be readable on phone screens

**State Variable Integration:**
```javascript
tax_bill_specimen = {
  property_address: "123 Main Street, {{STATE_MAJOR_CITY_1}}",
  market_value: 280000,
  assessed_value: {{280000 * STATE_ASSESSMENT_PERCENTAGE / 100}},
  homestead_exemption: {{STATE_HOMESTEAD_EXEMPTION}},
  taxable_value: {{(280000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION}},

  taxing_authorities: [
    {name: "{{STATE_COUNTY_NAME}} County", mills: {{STATE_PROPERTY_TAX_COUNTY_RATE}}},
    {name: "City of {{STATE_MAJOR_CITY_1}}", mills: 12},
    {name: "School District", mills: {{STATE_PROPERTY_TAX_SCHOOL_RATE}}},
    {name: "Community College", mills: 2},
    {name: "Library District", mills: 1.5}
  ]
}
```

---

### 3. Tax Jurisdiction Comparison Matrix

**Purpose:**
Allow students to systematically compare multiple {{STATE_NAME}} jurisdictions across tax rates, costs, and services for informed location decisions.

**Format:**
Interactive comparison table with filtering, sorting, and customization features.

**Inputs:**
1. **Location Selection:** Choose 3-6 jurisdictions from dropdown
2. **Financial Profile:**
   - Annual income
   - Estimated rent or property value
   - Monthly spending on taxable goods
3. **Priority Weights:** Sliders for importance of:
   - Low cost (0-10)
   - School quality (0-10)
   - Safety (0-10)
   - Amenities (0-10)
   - Job market (0-10)

**Expected Outputs:**
1. **Comparison Table:**
   | Criterion | Location A | Location B | Location C |
   |-----------|-----------|-----------|-----------|
   | Property Tax Rate | 35 mills | 28 mills | 22 mills |
   | Sales Tax Rate | 8.5% | 7.75% | 7.0% |
   | Monthly Tax Burden | $856 | $642 | $518 |
   | School Rating | 9/10 | 7/10 | 6/10 |
   | Crime Index | 35 | 48 | 52 |
   | Median Income | $68k | $59k | $51k |
   | **Recommended Rank** | 1st | 2nd | 3rd |

2. **Visual Comparisons:**
   - Bar charts for each numeric criterion
   - Spider/radar chart showing overall profiles
   - Heat map: green (best), yellow (middle), red (worst)

3. **Written Recommendation:**
   "Based on your priorities (Schools: 8, Cost: 6), Location A offers the best value despite higher costs. Excellent schools and low crime justify the premium."

4. **Export Options:**
   - Print comparison table
   - Download CSV
   - Email to self
   - Save to student portfolio

**Interaction Model:**
1. Student selects 3 jurisdictions from map or dropdown
2. Enters their financial profile
3. Adjusts priority sliders based on what matters most
4. Table auto-populates with data and calculations
5. Visual charts update in real-time
6. Recommendation engine suggests best match
7. Student can override recommendation and save their own choice with reasoning

**Design Notes:**
- **Data Visualization:** Use color coding and icons extensively
- **Mobile Optimization:** Table should be scrollable/swipeable on mobile
- **Customization:** Allow users to add custom criteria
- **Sorting:** Click column headers to sort by that criterion
- **Filtering:** Option to filter out locations above/below certain thresholds
- **Save State:** Remember selections if student navigates away and returns

**State Variable Integration:**
```javascript
jurisdiction_profiles = [
  {
    id: "{{STATE_MAJOR_CITY_1}}",
    property_tax_mills: {{STATE_MAJOR_CITY_1_MILLAGE}},
    sales_tax_combined: {{STATE_SALES_TAX + STATE_LOCAL_SALES_TAX_1}},
    school_rating: 8.5,
    crime_index: 35,
    median_income: 68000,
    job_growth_rate: 3.2,
    unemployment_rate: 3.8
  },
  // ... repeat for 20+ jurisdictions
]
```

---

### 4. Home Affordability Calculator with Tax Integration

**Purpose:**
Show students how property taxes impact what home they can actually afford, demonstrating the gap between "mortgage you can afford" and "total housing cost you can afford."

**Format:**
Advanced calculator with multiple scenarios and 10-year projection feature.

**Inputs:**
1. **Financial Profile:**
   - Annual household income
   - Down payment saved
   - Other monthly debts (car, student loans, credit cards)
   - Desired total monthly housing payment (all-in budget)

2. **Loan Parameters:**
   - Mortgage rate (pre-populated with current average, editable)
   - Loan term (15, 20, 30 years)
   - Property insurance estimate (auto-calculated, editable)
   - PMI if down payment < 20%

3. **Home Scenarios:** Tool presents 3 homes in different {{STATE_NAME}} jurisdictions with different tax rates

**Expected Outputs:**
1. **Monthly Cost Breakdown for Each Home:**
   ```
   Home A: {{STATE_HIGH_TAX_CITY}}
   Purchase Price: $310,000
   Down Payment: $30,000
   Loan Amount: $280,000

   Monthly Costs:
   - Principal & Interest: $1,498
   - Property Tax: $728 ({{STATE_HIGH_TAX_MILLAGE}} mills)
   - Homeowner's Insurance: $145
   - PMI: $117
   --------------------------
   Total Monthly: $2,488

   Your Budget: $2,000
   OVER BUDGET by $488/month
   ```

2. **Affordability Analysis:**
   - Green checkmark if affordable
   - Red X if over budget
   - Yellow caution if within 5% of budget
   - Debt-to-income ratio calculated

3. **10-Year Projection:**
   ```
   Year 1: $8,736 in property taxes
   Year 3: $9,275 (after reassessment at +3% appreciation)
   Year 6: $9,850 (after reassessment at +3% appreciation)
   Year 10: $10,459 (after reassessment at +3% appreciation)

   Total Property Taxes Paid (10 years): $95,320
   Total Mortgage Interest Paid (10 years): $168,245
   Equity Built (appreciation + principal): $143,560
   ```

4. **Recommendation:**
   - "Based on your $2,000/month budget, you can afford Home C comfortably."
   - "Home A requires $488 more per month. To afford it, you'd need to earn $7,300 more annually or reduce other expenses."
   - "Consider: Home A has excellent schools (9/10). If you plan to have children, the investment might be worth it."

**Interaction Model:**
1. Student enters financial profile
2. Calculator shows 3 pre-set homes in different tax jurisdictions
3. Student reviews monthly costs and affordability for each
4. Student clicks "10-Year Projection" for detailed long-term analysis
5. Student can adjust inputs (higher down payment, lower other debts) to see impacts
6. Student makes selection and writes reasoning: "I chose Home __ because __"
7. Tool saves decision to portfolio

**Design Notes:**
- **Visual Affordability:** Use color coding (green/yellow/red) to show budget fit immediately
- **Comparison View:** Side-by-side monthly cost comparison
- **Interactive Sliders:** Allow adjusting down payment, mortgage rate to see impacts
- **Assumptions Visible:** Show all assumptions clearly (appreciation rate, tax increase rate, insurance estimate)
- **What-If Scenarios:** "What if I saved an extra $10k for down payment?" button
- **Mobile-Friendly:** Must work well on phone for students using mobile devices

**State Variable Integration:**
```javascript
home_scenarios = [
  {
    location: "{{STATE_HIGH_TAX_CITY}}",
    price: 310000,
    property_tax_mills: {{STATE_HIGH_TAX_MILLAGE}},
    assessment_ratio: {{STATE_ASSESSMENT_PERCENTAGE}} / 100,
    homestead_exemption: {{STATE_HOMESTEAD_EXEMPTION}},
    school_rating: 9,
    appreciation_rate: 0.03, // 3% annual
    reassessment_frequency: "{{STATE_PROPERTY_ASSESSMENT_FREQUENCY}}"
  },
  // ... 2 more scenarios
]
```

---

### 5. Assessment Challenge Tool

**Purpose:**
Teach students how to evaluate whether a property tax assessment is fair and when/how to file an appeal.

**Format:**
Interactive case study with comparable property database and appeal decision wizard.

**Inputs:**
1. **Your Property:**
   - Address (pre-populated with scenario)
   - Current assessment (pre-populated: $285,000)
   - Property specs (3BR/2BA, 1,800 sq ft)
   - Your purchase price 2 years ago ($245,000)

2. **Comparable Properties:** Tool provides 5-6 recent sales of similar homes

3. **User Analysis:** Student answers questions about fairness of assessment

**Expected Outputs:**
1. **Comparable Sales Analysis:**
   ```
   Your Assessment: $285,000 (16.3% increase in 2 years)

   Recent Comparable Sales:
   1. 123 Oak St - 3BR/2BA, 1,800 sf - Sold $255,000 (3 mo ago)
   2. 456 Elm St - 3BR/2BA, 1,750 sf - Sold $262,000 (6 mo ago)
   3. 789 Pine St - 4BR/2BA, 2,000 sf - Sold $278,000 (2 mo ago)
   4. 321 Maple Dr - 3BR/2BA, 1,850 sf - Sold $268,000 (4 mo ago)

   Your home is most similar to #1 (same size)
   Comparable avg: $265,750
   Your assessment: $285,000
   Difference: +$19,250 (7.2% higher than comparables)
   ```

2. **Appeal Decision Wizard:**
   - "Is your assessment significantly higher than comparables?" → YES
   - "Do you have documentation?" → Need to gather
   - "What's the deadline?" → {{STATE_ASSESSMENT_APPEAL_DEADLINE}}
   - "What are your chances of success?" → MODERATE (strong comparables, but within range)

3. **Financial Impact:**
   ```
   Current Assessment: $285,000
   Current Annual Tax: $7,980 ({{STATE_MEDIUM_TAX_MILLAGE}} mills)

   If appeal succeeds and assessment reduced to $265,000:
   New Annual Tax: $7,420
   Annual Savings: $560
   Savings over 10 years: $5,600

   Cost to file appeal: $0-$50
   Worth pursuing: YES
   ```

4. **Appeal Process Guide:**
   - Step 1: Gather comparable sales data
   - Step 2: Take photos of property condition issues
   - Step 3: Complete appeal form (link provided)
   - Step 4: Submit by {{STATE_ASSESSMENT_APPEAL_DEADLINE}}
   - Step 5: Attend informal hearing
   - Step 6: Formal hearing if needed

5. **Documentation Checklist:**
   - [ ] Completed appeal form
   - [ ] Comparable sales data (printed)
   - [ ] Photos of property
   - [ ] Copy of assessment notice
   - [ ] Your purchase records (if recent)

**Interaction Model:**
1. Student reviews their property assessment and purchase history
2. Tool presents comparable sales data
3. Student analyzes: "Is my assessment fair?"
4. Student uses decision wizard to determine whether to appeal
5. If yes, student follows step-by-step appeal guide
6. Student calculates potential savings from successful appeal
7. Student completes documentation checklist

**Design Notes:**
- **Educational Focus:** Teach the process, not just the calculation
- **Real Links:** Provide actual {{STATE_NAME}} appeal form and county assessor contact info
- **Visual Comparisons:** Map showing where comparable properties are located
- **Photos:** Include property photos for visual comparison
- **Success Stories:** Optional sidebar with real appeal success stories
- **Legal Disclaimer:** "This tool is educational. Consult a tax professional for specific advice."

**State Variable Integration:**
```javascript
assessment_scenario = {
  state: "{{STATE_NAME}}",
  county: "{{STATE_COUNTY_NAME}}",
  your_assessment: 285000,
  your_purchase_price: 245000,
  years_since_purchase: 2,
  property_specs: {bedrooms: 3, bathrooms: 2, sqft: 1800},

  comparables: [
    {address: "123 Oak St", price: 255000, sqft: 1800, months_ago: 3},
    // ... more comparables
  ],

  millage_rate: {{STATE_MEDIUM_TAX_MILLAGE}},
  assessment_ratio: {{STATE_ASSESSMENT_PERCENTAGE}} / 100,
  appeal_deadline: "{{STATE_ASSESSMENT_APPEAL_DEADLINE}}",
  appeal_form_url: "{{STATE_ASSESSMENT_APPEAL_FORM_URL}}",
  assessor_contact: "{{STATE_COUNTY_ASSESSOR_CONTACT}}"
}
```

---

### 6. Life Stage Tax Planning Tool

**Purpose:**
Help students understand how local tax priorities change throughout different life stages and plan accordingly.

**Format:**
Interactive scenario-based decision tool with four life stage simulations.

**Inputs:**
1. **Life Stage Selection:** Student chooses or is assigned a scenario:
   - Scenario A: Age 22, Single, Career Start
   - Scenario B: Age 30, Married, Planning for Children
   - Scenario C: Age 45, Married, Children in School
   - Scenario D: Age 65, Retired, Fixed Income

2. **For Each Scenario:**
   - Income level (pre-set but viewable)
   - Family composition
   - Key priorities (pre-set but can be adjusted)

**Expected Outputs:**
1. **Scenario Profile:**
   ```
   Scenario A: Age 22, Single, Career Start
   Income: $42,000
   Priorities:
   - Low cost of living (High)
   - Social activities/nightlife (High)
   - Job opportunities (High)
   - Schools (Low - not relevant yet)
   - Safety (Medium)
   ```

2. **Recommended Location Type:**
   - Urban apartment in downtown area
   - Accept higher sales tax for convenience and social opportunities
   - Property taxes not relevant (renting)
   - Focus on job market and career growth

3. **{{STATE_NAME}} Recommendations:**
   - Best fit: {{STATE_MAJOR_CITY_1}} downtown (vibrant, jobs, accepts higher costs)
   - Alternative: {{STATE_MAJOR_CITY_2}} urban neighborhood
   - Avoid: Rural areas (limited social life and job opportunities)

4. **Financial Snapshot:**
   ```
   Expected Monthly Costs in Recommended Location:
   - Rent: $950
   - Sales Tax (estimated): $85/month
   - Local income tax: ${{42000 * STATE_LOCAL_INCOME_TAX_RATE / 100 / 12}}/month
   - Total: ${{950 + 85 + (42000 * STATE_LOCAL_INCOME_TAX_RATE / 100 / 12)}}
   ```

5. **10-Year Outlook:**
   "By age 32, you'll likely be in Scenario B—married, planning for children. Your priorities will shift toward school quality and safety, making suburban areas more attractive even with higher property taxes."

**Interaction Model:**
1. Student selects or is assigned a life stage scenario
2. Tool presents the profile with priorities
3. Student adjusts priority sliders if desired
4. Tool recommends location types and specific {{STATE_NAME}} jurisdictions
5. Student views financial snapshot
6. Student can compare: "What if I chose a different priority ranking?"
7. Student reflects: "Which scenario am I closest to? What matters most to me now vs. in 10 years?"

**Design Notes:**
- **Storytelling:** Use narrative format—make each scenario feel like a real person
- **Persona Photos:** Include diverse character illustrations
- **Visual Timeline:** Show how priorities change over life stages
- **Compare Feature:** View multiple scenarios side-by-side
- **Reflection Questions:** Prompt students to think about their own future
- **Flexibility:** Allow students to create custom scenarios

**State Variable Integration:**
```javascript
life_stage_scenarios = [
  {
    stage: "A",
    age: 22,
    income: 42000,
    family: "single",
    priorities: {cost: 8, social: 9, jobs: 9, schools: 2, safety: 6},
    recommended_locations: [
      {name: "{{STATE_MAJOR_CITY_1}} Downtown", match_score: 9.2},
      {name: "{{STATE_MAJOR_CITY_2}} Urban Core", match_score: 8.8}
    ],
    monthly_costs: {
      rent: 950,
      sales_tax: 85,
      income_tax: ({{42000 * STATE_LOCAL_INCOME_TAX_RATE / 100}} / 12)
    }
  },
  // ... 3 more scenarios
]
```

---

## Skill Builder Assets (Primary Interactive Tool)

The **Local Tax Impact Calculator** (Asset #1) serves as the primary skill builder for this chapter and is featured in both Day 1 and Day 2. See full specifications in Day 1 Assets section above.

---

## Downloadable Resources (Printable PDFs)

All interactive tools must have printable PDF alternatives for accessibility and technology equity.

### PDF 1: Local Tax Calculation Worksheet

**Purpose:** Paper-based alternative to Local Tax Impact Calculator

**Format:** 8.5" x 11" fillable PDF worksheet

**Content:**
1. **Section 1: Property Tax Calculation**
   ```
   Property Market Value:           $___________
   Assessment Ratio ({{STATE_ASSESSMENT_PERCENTAGE}}%):         × 0.{{STATE_ASSESSMENT_PERCENTAGE}}
   Assessed Value:                  $___________
   Homestead Exemption:            - ${{STATE_HOMESTEAD_EXEMPTION}}
   Taxable Value:                   $___________

   Millage Rates:
   County:     _____ mills  = $___________
   City:       _____ mills  = $___________
   School:     _____ mills  = $___________
   Other:      _____ mills  = $___________
                Total Annual Property Tax:  $___________
                Monthly (÷ 12):             $___________
   ```

2. **Section 2: Sales Tax Calculation**
   ```
   Annual Taxable Purchases:        $___________
   State Sales Tax ({{STATE_SALES_TAX}}%):       × 0.0{{STATE_SALES_TAX}}
   Local Sales Tax (_____%):        × 0.0___
   Combined Rate:                   × 0.0___
   Annual Sales Tax Paid:           $___________
   Monthly (÷ 12):                  $___________
   ```

3. **{{#if STATE_ALLOWS_LOCAL_INCOME_TAX}}Section 3: Local Income Tax**
   ```
   Annual Income:                   $___________
   Local Income Tax Rate (_____%):  × 0.0___
   Annual Local Income Tax:         $___________
   Monthly (÷ 12):                  $___________
   ```{{/if}}

4. **Section 4: Total Local Tax Burden**
   ```
   Property Tax (monthly):          $___________
   Sales Tax (monthly):            + $___________
   Income Tax (monthly):           + $___________
   TOTAL Monthly Local Taxes:       $___________
   TOTAL Annual Local Taxes:        $___________
   ```

5. **Section 5: Location Comparison Table**
   | Category | Location A | Location B | Location C |
   |----------|-----------|-----------|-----------|
   | Property Tax Rate | _____ mills | _____ mills | _____ mills |
   | Sales Tax Rate | _____% | _____% | _____% |
   | Monthly Total Tax | $______ | $______ | $______ |
   | School Rating | ___/10 | ___/10 | ___/10 |
   | My Choice: _______________________ |
   | Reason: _________________________________________________ |

**State-Specific:** Auto-populate {{STATE_NAME}} rates and examples, but leave fillable for any jurisdiction.

---

### PDF 2: Property Tax Bill Decoder

**Purpose:** Annotated sample tax bill with explanations

**Format:** 8.5" x 14" (legal size) to accommodate full bill

**Content:**
- Full-size replica of {{STATE_NAME}} property tax bill
- Callout boxes explaining each section
- Glossary of terms on reverse side
- Practice calculations for students to verify totals

---

### PDF 3: Home Affordability Worksheet

**Purpose:** Paper-based home affordability calculator with tax integration

**Format:** 8.5" x 11" two-sided worksheet

**Content:**
1. **Your Financial Profile:**
   - Annual income, down payment, other debts, desired monthly payment

2. **Home Scenarios (A, B, C):**
   - For each: Purchase price, assessed value, millage rate, insurance
   - Monthly cost breakdown with spaces for calculations
   - Over/under budget analysis

3. **10-Year Projection Table:**
   - Years 1, 3, 6, 10 property tax estimates
   - Cumulative taxes paid
   - Equity built

4. **Decision Matrix:**
   - Which home fits budget?
   - Which home best aligns with priorities?
   - Final choice and reasoning

---

### PDF 4: Assessment Appeal Guide

**Purpose:** Step-by-step guide for challenging property assessment

**Format:** 8.5" x 11" tri-fold brochure

**Content:**
1. **Front Panel:** "Is Your Property Assessment Fair?"
2. **Panel 2:** How to gather comparable sales data
3. **Panel 3:** When to appeal (decision flowchart)
4. **Panel 4:** {{STATE_NAME}} appeal process steps
5. **Panel 5:** Documentation checklist
6. **Panel 6:** Sample appeal letter template

---

### PDF 5: Life Stage Tax Planning Matrix

**Purpose:** Visual guide to how tax priorities change over time

**Format:** 8.5" x 11" color chart

**Content:**
- 4 scenarios with priorities ranked
- Recommended location types for each
- Questions for self-reflection
- Space for personal planning notes

---

## State-Specific Data Requirements

All tools require the following data from the {{STATE_NAME}} data layer:

### Property Tax Data
```json
{
  "state_assessment_percentage": {{STATE_ASSESSMENT_PERCENTAGE}},
  "homestead_exemption": {{STATE_HOMESTEAD_EXEMPTION}},
  "assessment_frequency": "{{STATE_PROPERTY_ASSESSMENT_FREQUENCY}}",
  "appeal_deadline": "{{STATE_ASSESSMENT_APPEAL_DEADLINE}}",
  "appeal_form_url": "{{STATE_ASSESSMENT_APPEAL_FORM_URL}}",

  "jurisdictions": [
    {
      "name": "{{STATE_MAJOR_CITY_1}}",
      "county": "{{STATE_COUNTY_NAME}}",
      "property_tax_mills": {{STATE_MAJOR_CITY_1_MILLAGE}},
      "breakdown": {
        "county": {{STATE_PROPERTY_TAX_COUNTY_RATE}},
        "city": 12,
        "school": {{STATE_PROPERTY_TAX_SCHOOL_RATE}},
        "special": 3
      },
      "sales_tax_local": {{STATE_LOCAL_SALES_TAX_1}},
      "income_tax_rate": {{STATE_LOCAL_INCOME_TAX_RATE_1}},
      "school_rating": 8.5,
      "crime_index": 35,
      "median_income": 68000,
      "unemployment_rate": 3.8,
      "median_home_value": 285000
    }
    // ... 20+ jurisdictions
  ]
}
```

### Sales Tax Data
```json
{
  "state_sales_tax": {{STATE_SALES_TAX}},
  "local_sales_tax_range": {
    "min": {{STATE_LOCAL_SALES_TAX_MIN}},
    "max": {{STATE_LOCAL_SALES_TAX_MAX}}
  },
  "combined_range": {
    "min": {{STATE_COMBINED_SALES_TAX_MIN}},
    "max": {{STATE_COMBINED_SALES_TAX_MAX}}
  }
}
```

### {{#if STATE_ALLOWS_LOCAL_INCOME_TAX}}Income Tax Data
```json
{
  "local_income_tax_allowed": true,
  "rate_range": "{{STATE_LOCAL_INCOME_TAX_RANGE}}",
  "example": "{{STATE_LOCAL_INCOME_TAX_EXAMPLE}}"
}
```{{else}}Income Tax Data
```json
{
  "local_income_tax_allowed": false
}
```{{/if}}

---

## Technical Implementation Notes for Developers

### Data Architecture
- All {{STATE_NAME}} data should be pulled from centralized state data layer
- Cache jurisdiction data locally to reduce API calls
- Update rates annually (or when {{STATE_NAME}} updates occur)
- Allow manual override of auto-populated rates for "what-if" scenarios

### User Experience
- **Load Time:** Tools should load within 2 seconds on broadband
- **Responsive:** Must work on mobile (320px width minimum)
- **Save State:** Store user inputs in browser localStorage
- **Share Results:** Generate unique URLs for sharing comparisons
- **Print Friendly:** CSS print stylesheets for clean printouts

### Accessibility (WCAG 2.1 AA Compliance)
- Keyboard navigation throughout
- Screen reader compatible (proper ARIA labels)
- Color contrast ratios minimum 4.5:1
- Font size adjustable without breaking layout
- Alternative text for all images and charts
- Captions for any video content

### Analytics (Optional)
- Track which jurisdictions students compare most
- Monitor drop-off points in multi-step tools
- Measure time spent on each activity
- Identify common errors or confusion points

### Error Handling
- Validate all numeric inputs
- Provide helpful error messages ("Please enter a value between $50,000 and $2,000,000")
- Graceful degradation if state data unavailable
- Fallback to manual entry if auto-population fails

---

## Asset Priority for Development

If resources are limited, build in this order:

1. **Local Tax Impact Calculator** (Primary skill builder - required)
2. **Tax Jurisdiction Comparison Matrix** (Core Day 2 activity)
3. **Home Affordability Calculator** (High-value for real-world application)
4. **Property Tax Bill Analyzer** (Educational value, simpler to build)
5. **Assessment Challenge Tool** (Nice-to-have, specific use case)
6. **Life Stage Planning Tool** (Lowest priority, more reflective than calculational)

All printable PDFs should be created regardless of interactive tool priority.

---

## Maintenance & Updates

**Annual Review Required:**
- Update all {{STATE_NAME}} tax rates (December/January)
- Verify jurisdiction data accuracy
- Update mortgage rates to current averages
- Refresh school ratings if available
- Check that all state URLs are still valid

**As Needed:**
- Add new jurisdictions if requested by teachers
- Update comparable property sales data in Assessment Challenge
- Revise life stage scenarios to reflect current economic conditions
- Incorporate teacher feedback on usability issues

---

## End of Assets Documentation

**Questions for Development Team:**
Contact curriculum team with questions about specifications, desired functionality, or state data integration.

**Testing Requirements:**
All tools must be tested with actual {{STATE_NAME}} data before deployment to ensure accuracy and usability.

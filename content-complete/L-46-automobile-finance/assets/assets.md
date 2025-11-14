# Asset Specifications for L-46: Automobile Finance - Buying vs. Leasing

## Day 1 Assets

### 1. Buy vs. Lease Comparison Infographic
- **Purpose:** Visual side-by-side comparison of buying versus leasing
- **Format/Inputs:** Static infographic (SVG or high-res PNG), responsive design
- **Expected Outputs:** Clear visual reference students can bookmark/screenshot
- **Interaction Model:** Static display
- **Design Notes:**
  - Split-screen layout: BUYING (left) vs. LEASING (right)
  - Use icons: House (ownership) for buying, Calendar/Clock (temporary) for leasing
  - Key comparisons with visual indicators:
    - Monthly payment (show relative size with $ symbols)
    - Ownership status (checkmark vs. X)
    - Mileage limits (unlimited symbol vs. speedometer with limit)
    - End result (car icon you keep vs. return arrow)
    - Long-term cost (bar graph showing 6-year comparison)
  - Color scheme: Blue for buying, Orange for leasing
  - Include callout boxes for key insights: "After 6 years: OWN A $12K ASSET" vs. "After 6 years: PAID $30K, OWN NOTHING"

### 2. Vehicle Depreciation Curve Visualization
- **Purpose:** Show how vehicles lose value over time
- **Format/Inputs:** Interactive graph (HTML5/JavaScript) with hover states
- **Expected Outputs:** Visual understanding of depreciation rates
- **Interaction Model:**
  - Hover over years to see exact value
  - Toggle between new vs. used vehicle depreciation curves
  - Input purchase price to see personalized depreciation
- **Design Notes:**
  - X-axis: Years 0-10
  - Y-axis: Vehicle value ($0 to $50,000)
  - Show two curves: New car (steeper initial drop) vs. 3-year-old used car (gentler curve)
  - Annotate key milestones: "Year 1: -20-30% value", "Year 5: -60% value"
  - Shaded area under curve represents "lost value"
  - Allow students to input their vehicle's purchase price to generate custom curve

### 3. Total Cost of Ownership Calculator Preview
- **Purpose:** Teaser showing complete cost breakdown to hook students
- **Format/Inputs:** Static infographic showing example breakdown
- **Expected Outputs:** "Aha" moment that monthly payment is small part of total cost
- **Interaction Model:** Static (full calculator available in Day 2)
- **Design Notes:**
  - Center: Large "$399/month" in bold
  - Radiating out: Additional costs with icons
    - Insurance: +$200/mo
    - Fuel: +$150/mo
    - Maintenance: +$50/mo
    - Registration: +${{STATE_REGISTRATION_ANNUAL}}/mo (state-specific)
  - Bottom total: "ACTUAL COST: $839/month"
  - Percentage circle: "Vehicle payment is only 48% of total cost"
  - Callout: "What else are you forgetting?"

### 4. Loan Term Comparison Chart
- **Purpose:** Show how loan length affects total interest paid
- **Format/Inputs:** Animated bar chart (can be static with strong visual design)
- **Expected Outputs:** Clear visual of interest cost differences
- **Interaction Model:** Static or simple animation
- **Design Notes:**
  - Three bars showing 36-month, 60-month, 72-month loans for same $25,000 vehicle
  - Each bar split into two colors:
    - Principal (darker blue): Same for all
    - Interest (red): Grows significantly longer the term
  - Numbers displayed on bars: Monthly payment, Total paid, Total interest
  - Visual insight: "72-month loan costs $4,500 MORE in interest!"

### 5. Real-World Example Cards
- **Purpose:** Illustrate Mia, James, and Taylor scenarios from Day 1 content
- **Format/Inputs:** Digital cards or scrollable panels (mobile-friendly)
- **Expected Outputs:** Engaging case study presentation
- **Interaction Model:** Click/tap to expand each person's full story
- **Design Notes:**
  - Three cards, each with:
    - Character illustration (diverse representation)
    - Name and approach: "Mia's Buy-and-Keep Strategy"
    - Timeline graphic showing their 6-7 year journey
    - Key numbers highlighted: Total paid, Final value, Net cost
    - Outcome emoji: 😊 (Mia), 😰 (James), 🎯 (Taylor)
  - Use color coding: Green (good outcome), Red (expensive), Yellow (balanced)

## Day 2 Assets

### 1. Auto Finance Decision Calculator (PRIMARY SKILL BUILDER)
- **Purpose:** Interactive tool for comprehensive buy vs. lease comparison
- **Format/Inputs:** Web application with multi-section form
- **Expected Outputs:** Side-by-side scenario comparison with visualizations
- **Interaction Model:** Multi-step wizard with progressive disclosure
- **Design Notes:**

  **Step 1: Vehicle Selection**
  - Input: Vehicle make/model (dropdown or free text)
  - Input: New price ($)
  - Input: Used price (3-year-old) ($)
  - Input: Lease offer monthly payment ($)
  - Auto-lookup integration with KBB/Edmunds API (if available)

  **Step 2: Financing Details - BUY NEW**
  - Down payment ($ or %)
  - Loan term (dropdown: 36, 48, 60, 72 months)
  - Interest rate (% - default: {{STATE_AVG_AUTO_LOAN_RATE_NEW}}%)
  - STATE-SPECIFIC INPUTS (auto-populated for {{STATE_NAME}}):
    - Sales tax rate: {{STATE_SALES_TAX}}% (editable)
    - Registration fee: Initial ${{STATE_REGISTRATION_INITIAL}}, Annual ${{STATE_REGISTRATION_ANNUAL}} (editable)

  **Step 3: Financing Details - BUY USED**
  - Down payment ($ or %)
  - Loan term (dropdown: 24, 36, 48, 60 months)
  - Interest rate (typically higher than new, show as % above new rate)
  - Same state-specific inputs

  **Step 4: Leasing Details**
  - Lease term (dropdown: 24, 36, 39 months)
  - Cap cost reduction/down payment ($)
  - Annual mileage limit (dropdown: 10k, 12k, 15k)
  - Money factor (or APR equivalent)
  - Acquisition fee: ${{STATE_LEASE_ACQUISITION_FEE}} (editable, state-specific)
  - Disposition fee ($)

  **Step 5: Ownership Costs** (same for all scenarios)
  - Monthly insurance: ${{STATE_INSURANCE_AVG_TEEN}} default (editable, state-specific)
  - Annual mileage driven
  - Fuel efficiency (MPG)
  - Gas price: ${{STATE_GAS_PRICE_CURRENT}}/gallon default (editable, state-specific)
  - Estimated annual maintenance ($)

  **Step 6: Results & Comparison**
  - Display three columns: BUY NEW | BUY USED | LEASE
  - For each show:
    - Monthly payment
    - Total paid over 6 years
    - Vehicle value at 6 years
    - Net cost (paid - value)
    - Cost per mile
    - Equity position chart (line graph over time)
  - Visual winner indicator (lowest net cost highlighted in green)
  - "What if" sliders:
    - Adjust interest rate ±2%
    - Change annual mileage ±5000
    - Extend analysis to 10 years
  - Download/print button for results
  - Save scenario button (localStorage or account-based)

  **Technical Specifications:**
  - Responsive design (mobile, tablet, desktop)
  - Real-time calculation (no page refresh)
  - Input validation (prevent unrealistic values)
  - Tooltips on all fields explaining terms
  - State: {{STATE_NAME}} (automatically set, fields pre-populated)

### 2. Loan Terms Analyzer
- **Purpose:** Isolate the impact of loan term length on total cost
- **Format/Inputs:** Side-by-side comparison tool
- **Expected Outputs:** Clear visualization of term impact
- **Interaction Model:** Input loan amount and see three term scenarios
- **Design Notes:**
  - Single input: Loan amount ($)
  - Automatic calculation of three scenarios (36/60/72 months)
  - Output table showing:
    - Monthly payment
    - Total interest paid (HIGHLIGHTED)
    - Total amount paid
    - Years underwater (owing > value)
  - Amortization schedule view (expandable)
  - Visual: Line graph showing loan balance vs. vehicle value over time
    - Shaded "underwater" region
  - Opportunity cost calculator integration: "Invest the payment difference"

### 3. Total Cost of Ownership Worksheet (Interactive + Printable)
- **Purpose:** Step-by-step guide to calculate complete vehicle costs
- **Format/Inputs:** Interactive web form + PDF worksheet version
- **Expected Outputs:** Complete 6-year cost breakdown
- **Interaction Model:** Guided form with calculations
- **Printable Version Specifications:**
  - 2-page PDF worksheet
  - Page 1: Purchase & Financing Costs
    - Vehicle price: $_______
    - Down payment: $_______
    - Loan amount: $_______
    - Interest rate: _____%
    - Loan term: ____ months
    - Monthly payment: $_______
    - Total paid over loan: $_______
    - Total interest paid: $_______
  - Page 1 continued: State & Initial Costs
    - Sales tax ({{STATE_NAME}}): {{STATE_SALES_TAX}}% = $_______
    - Registration/title: ${{STATE_REGISTRATION_INITIAL}}
    - Initial inspection (if applicable): {{#if STATE_INSPECTION_REQUIRED}}${{STATE_INSPECTION_COST}}{{else}}N/A{{/if}}
  - Page 2: Ongoing Annual Costs (Years 1-6)
    - Registration renewal: $_____ × 6 = $_______
    - Insurance: $_____ × 6 = $_______
    - Fuel: $_____ × 6 = $_______
    - Maintenance: $_____ × 6 = $_______
    - Repairs estimate: $_______
  - Page 2 continued: Final Calculation
    - Total costs (sum all above): $_______
    - Estimated vehicle value at year 6: $_______
    - NET COST: $_______
    - Cost per mile (÷ total miles): $_______

### 4. Vehicle Financing Decision Matrix (Printable)
- **Purpose:** Personalized framework for making financing decisions
- **Format:** 1-page PDF worksheet
- **Content Structure:**
  - Section 1: Your Priorities (rank 1-5)
    - [ ] Lowest monthly payment
    - [ ] Lowest total cost
    - [ ] Always having a newer vehicle
    - [ ] No car payments eventually
    - [ ] Flexibility to change vehicles
  - Section 2: Your Current Circumstances
    - Annual income: $_______
    - Monthly take-home: $_______
    - Current savings: $_______
    - Expected annual mileage: _______
    - Credit score range: Excellent / Good / Fair / Building
    - Job stability: Very Stable / Stable / Uncertain / Changing Soon
  - Section 3: State-Specific Factors
    - State: {{STATE_NAME}}
    - Sales tax rate: {{STATE_SALES_TAX}}%
    - Registration fees: Initial ${{STATE_REGISTRATION_INITIAL}}, Annual ${{STATE_REGISTRATION_ANNUAL}}
    - Average insurance cost: ${{STATE_INSURANCE_AVG_TEEN}}/month
    - {{#if STATE_INSPECTION_REQUIRED}}Inspection required: ${{STATE_INSPECTION_COST}} annually{{else}}No inspection required{{/if}}
  - Section 4: Analysis Summary (from Day 2 activities)
    - Scenario 1 (Buy New) net cost: $_______
    - Scenario 2 (Buy Used) net cost: $_______
    - Scenario 3 (Lease) net cost: $_______
  - Section 5: My Decision Framework
    - Recommended approach: Buy New / Buy Used / Lease
    - Maximum monthly payment: $_______
    - Maximum loan term: ____ months
    - Target price range: $_______ to $_______
    - Plan after loan payoff: _________________
  - Section 6: My Personal Rules
    - I will not: _____________________________
    - I will prioritize: _____________________________
    - My timeline: _____________________________

### 5. Scenario Cards (Activity 1)
- **Purpose:** Standardized vehicle profiles for group analysis
- **Format:** Digital cards + printable handouts
- **Printable Version:**
  - Three 1-page handouts (one per profile)
  - Each includes:
    - Vehicle photo/illustration
    - Specifications (year, make, model, price)
    - Given financial parameters (down payment, loan terms, etc.)
    - STATE-SPECIFIC COST TABLE (auto-populated for {{STATE_NAME}}):
      - Sales tax: {{STATE_SALES_TAX}}%
      - Registration: Initial ${{STATE_REGISTRATION_INITIAL}}, Annual ${{STATE_REGISTRATION_ANNUAL}}
      - Insurance avg: ${{STATE_INSURANCE_AVG_TEEN}}/month
    - Calculation workspace:
      - Purchase/lease payments: $_______
      - State fees: $_______
      - Insurance (6 years): $_______
      - Fuel (6 years): $_______
      - Maintenance (6 years): $_______
      - Residual value: $_______
      - TOTAL NET COST: $_______
      - Cost per mile: $_______/mile

### 6. Opportunity Cost Calculator Supplement
- **Purpose:** Show what invested car payments could become
- **Format:** Simple calculator + visual chart
- **Inputs:**
  - Monthly payment difference between scenarios ($)
  - Investment period (years)
  - Expected return rate (default 7%)
- **Outputs:**
  - Future value of invested payments
  - Total contributions vs. total growth
  - Visual: Growth chart over time
- **Printable Version:**
  - Reference table showing common scenarios:
    - $200/month for 6 years at 7% = $17,392
    - $400/month for 6 years at 7% = $34,785
    - $500/month for 10 years at 7% = $87,052
  - Formula explanation for manual calculation
  - Reflection prompts: "What could this money mean for your future?"

## Downloadable Resources (Printable PDFs)

### 1. State-Specific Cost Reference Sheet (CRITICAL)
- **Purpose:** Quick reference for all state-specific costs
- **Format:** 1-page auto-populated reference (state-specific)
- **Content for {{STATE_NAME}}:**
  - State name: {{STATE_NAME}} ({{STATE_CODE}})
  - Sales tax rate on vehicles: {{STATE_SALES_TAX}}%
  - Registration fees:
    - Initial title & registration: ${{STATE_REGISTRATION_INITIAL}}
    - Annual renewal: ${{STATE_REGISTRATION_ANNUAL}}
  - Average insurance costs by age group:
    - 16-19: ${{STATE_INSURANCE_AVG_TEEN}}/month
    - 20-25: [calculated from state data]
    - 26-35: [calculated from state data]
  - Average gas price (current): ${{STATE_GAS_PRICE_CURRENT}}/gallon
  - Average auto loan rates:
    - New cars: {{STATE_AVG_AUTO_LOAN_RATE_NEW}}%
    - Used cars: {{STATE_AVG_AUTO_LOAN_RATE_USED}}%
  - Emissions/inspection requirements: {{#if STATE_INSPECTION_REQUIRED}}Yes - ${{STATE_INSPECTION_COST}} annually{{else}}No{{/if}}
  - State-specific programs: [To be researched per state]
  - Links:
    - State DMV: {{STATE_DMV_URL}}
    - Insurance comparison tool: {{STATE_INSURANCE_COMPARISON_URL}}
    - Consumer protection: {{STATE_CONSUMER_PROTECTION_URL}}

### 2. Auto Loan Comparison Worksheet
- **Purpose:** Side-by-side comparison of different loan options
- **Format:** 2-page PDF
- **Content:**
  - Header: Vehicle and loan details
  - Three-column comparison table (3 different loan terms)
  - Rows for: Monthly payment, Total interest, Total paid, Equity timeline
  - Visual breakeven chart (when do you have positive equity?)
  - Decision criteria checklist

### 3. Buy vs. Lease Decision Flowchart
- **Purpose:** Visual decision tool for determining best approach
- **Format:** 1-page infographic
- **Content:**
  - Start: "Choosing Vehicle Financing"
  - Decision nodes:
    - "Do you drive >15k miles/year?" → Yes: BUY
    - "Can you keep vehicle 8+ years?" → Yes: BUY
    - "Need to minimize monthly payment?" → Maybe lease
    - "Want to build equity?" → BUY
    - "Value always having new car?" → Maybe lease
  - End nodes with recommendations and warnings
  - QR codes to online calculators

### 4. Vehicle Financing Glossary
- **Purpose:** Quick reference for key terms
- **Format:** 2-page PDF booklet
- **Content:**
  - A-Z list of terms with definitions
  - Icons for visual reference
  - Examples for each term
  - Formula explanations (APR, depreciation rate, cost per mile)

### 5. Negotiation Tips & Consumer Rights Guide
- **Purpose:** Practical guide for dealership interactions
- **Format:** 2-page PDF
- **Content (Page 1):**
  - Research before you go (pricing tools)
  - Know your credit score
  - Get pre-approved financing
  - Negotiate price, then payments
  - Don't rush—dealers want the sale
  - Read ALL documents before signing
- **Content (Page 2):**
  - Your rights under {{STATE_NAME}} law
  - Lemon law protections ({{STATE_NAME}}-specific)
  - Contract cancellation periods
  - What to do if you're pressured
  - Resources: {{STATE_NAME}} Attorney General ({{STATE_CONSUMER_PROTECTION_URL}}), Consumer Financial Protection Bureau

## Asset Development Priority

**Phase 1 (Essential for Launch):**
1. Auto Finance Decision Calculator (primary skill builder)
2. State-Specific Cost Reference Sheet (critical for accuracy)
3. Vehicle Financing Decision Matrix (for personal strategy)
4. Total Cost of Ownership Worksheet (printable)

**Phase 2 (Enhances Experience):**
5. Buy vs. Lease Comparison Infographic
6. Loan Terms Analyzer
7. Scenario Cards for Activity 1

**Phase 3 (Nice to Have):**
8. Vehicle Depreciation Curve Visualization
9. Opportunity Cost Calculator
10. Downloadable guides and resources

## Technical Implementation Notes

**State-Specific System Requirements:**
- State determined at district/admin level during LMS setup
- All content automatically displays {{STATE_NAME}} data
- State data layer (JSON files) updated annually
- All calculators pre-populated with state-specific defaults (editable by user)
- Printable PDFs auto-populate with {{STATE_NAME}} data

**Accessibility:**
- All interactive tools must meet WCAG 2.1 AA standards
- Keyboard navigation required
- Screen reader compatible
- Color-blind friendly palettes
- Text alternatives for all graphics

**Data Sources:**
- Bankrate.com for interest rates
- AAA for fuel costs and maintenance estimates
- Kelly Blue Book / Edmunds for vehicle values
- State DMV websites for fees
- Insurance.com state averages

**Asset File Naming Convention:**
- `l46-{asset-name}-{version}.{ext}`
- Example: `l46-auto-calculator-v1.html`
- Example: `l46-state-costs-california-v1.pdf`

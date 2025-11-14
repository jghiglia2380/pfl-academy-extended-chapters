# L-57 Assets: Loan Application Process and Requirements

This document specifies all interactive tools, downloadable resources, and assets needed for L-57. Each asset includes detailed specifications for the development team.

---

## Day 1 Assets

### 1. Loan Application Simulator (PRIMARY SKILL BUILDER)

**Purpose:** Allow students to complete realistic loan applications for different scenarios and receive instant feedback on application quality, approval likelihood, and factors affecting their outcome.

**Format:** Interactive web-based application with form inputs, validation, and feedback system

**Inputs:**
- **Scenario Selection:** Dropdown to choose loan type (Auto Loan, Personal Loan, Mortgage)
- **Pre-loaded Borrower Profile:** System provides complete financial profile including:
  - Personal information (name, address, DOB, SSN - simulated)
  - Employment details (employer, position, length of employment, gross annual/monthly income)
  - Financial information (all current debts with balances and monthly payments, all assets with values)
  - Credit score and brief credit history summary
  - Loan request details (amount needed, purpose, term preferred)
- **Application Form Fields:**
  - Personal Information Section: Name, current address, previous addresses (if less than 2 years at current), phone, email, SSN, date of birth
  - Employment Section: Current employer name/address, position, supervisor, start date, gross monthly income, other income sources
  - Previous Employment (if current job less than 2 years): Previous employer, dates, position
  - Financial Section:
    - Current Debts: List each (credit cards, student loans, auto loans, mortgages) with creditor name, balance, monthly payment
    - Assets: Checking account balance, savings account balance, retirement accounts, other investments, real estate owned
  - Loan Request: Amount requested, loan purpose (dropdown options), desired term
  - Additional Questions: Yes/No questions about bankruptcies, foreclosures, lawsuits, co-signer availability
- **For Auto Loans:** Vehicle information (year, make, model, VIN, purchase price)
- **For Mortgages:** Property information (address, purchase price, down payment amount, property type)

**Expected Outputs:**
- **Real-time Validation Feedback:**
  - Red flags for missing required fields with specific error messages
  - Yellow warnings for incomplete sections (e.g., "Previous employment section incomplete")
  - Green checkmarks for properly completed sections
- **Automatic Calculations:**
  - Current Debt-to-Income Ratio (sum of all monthly debt payments ÷ gross monthly income)
  - Projected DTI with new loan payment
  - Loan-to-Value Ratio (for secured loans: loan amount ÷ asset value)
  - Available Reserves (savings remaining after down payment ÷ monthly payment amount)
- **Application Strength Score:** 0-100 scale based on:
  - Completeness (all required fields filled)
  - Accuracy (realistic information, consistent data)
  - Credit score
  - DTI ratio
  - Available capital/reserves
  - LTV (if applicable)
  - Employment stability
- **Approval Likelihood:** Categorical rating
  - "Strong Approval Likelihood" (Score 80-100): Multiple lenders would compete for this borrower
  - "Likely Approval" (Score 65-79): Would be approved at standard terms
  - "Conditional Approval" (Score 50-64): Approval possible with conditions (co-signer, larger down payment, higher rate)
  - "Unlikely Approval" (Score 35-49): Significant concerns, approval difficult
  - "Denial Likely" (Score 0-34): Multiple red flags, approval very unlikely
- **Estimated Interest Rate Range:** Based on credit score and loan type (e.g., "5.5% - 6.5%" for good credit auto loan)
- **Detailed Feedback Report:**
  - **Strengths:** List positive factors (e.g., "Strong credit score of 740", "Low DTI of 22%", "Stable employment for 4 years")
  - **Weaknesses:** List concerns (e.g., "Limited savings for reserves", "High credit utilization", "Recent job change")
  - **Recommendations:** Specific actions to improve application (e.g., "Increase down payment by $2,000 to reduce LTV from 90% to 82%", "Pay off $1,500 credit card balance to reduce DTI from 38% to 34%")
  - **Missing Documentation:** List any documents not mentioned that would be required (e.g., "2 months of bank statements", "Employment verification letter")

**Interaction Model:**
1. Student selects one of three preset scenarios (Auto Loan, Personal Loan, Mortgage)
2. System displays complete borrower profile for that scenario
3. Student completes the loan application form using information from the profile
4. As student fills fields, system provides real-time validation (red/yellow/green indicators)
5. System auto-calculates DTI and LTV as student enters debt and loan information
6. Student submits completed application
7. System generates Application Strength Score, approval likelihood, and detailed feedback report
8. Student can modify any borrower profile variables (increase down payment, change credit score, add/remove debts) and resubmit to see how changes affect outcome
9. System highlights which changes had the biggest impact on approval odds
10. Student can save comparisons showing "before" and "after" scenarios

**Design Notes:**
- Use progress indicator showing section completion (e.g., "Personal Info: Complete, Employment: Complete, Financial: 60%")
- Implement smart field validation (e.g., SSN must be 9 digits, dates must be logical, income must be positive number)
- Pre-populate some fields from borrower profile to reduce data entry, but require student to complete critical sections
- Use tooltips/help icons for complex terms (e.g., hover over "DTI" shows definition and formula)
- Make the feedback report downloadable/printable for student reference
- Use color coding consistently: Green = strong, Yellow = moderate concern, Red = significant concern
- Provide "Why does this matter?" explanations for each feedback item
- Include a comparison view showing multiple submissions side-by-side
- Mobile-responsive design for tablet use
- Estimated development time: 15-20 hours for full implementation with all three loan types

---

## Day 2 Assets

### 2. Documentation Checklist Builder

**Purpose:** Help students identify required documentation for different loan types and borrower situations

**Format:** Interactive checklist tool with drag-and-drop or selection interface

**Inputs:**
- **Borrower Profile Selection:** Student selects one of three provided profiles:
  - Profile A (Destiny): Auto loan seeker, W-2 employee, standard situation
  - Profile B (Andre): Personal loan seeker, self-employed, recent job change
  - Profile C (Keisha): Mortgage seeker, first-time homebuyer, receiving gift funds for down payment
- Each profile includes: Name, age, employment situation, income sources, loan type/amount sought, special circumstances
- **Available Documents List:** Student selects from ~25 possible documents:
  - Government-issued photo ID
  - Social Security card
  - Proof of current address (utility bill, lease agreement)
  - Recent pay stubs (quantity: 2 weeks, 1 month, 2 months, 3 months)
  - W-2 forms (1 year, 2 years)
  - Tax returns (1 year, 2 years)
  - Profit & Loss statement (for self-employed)
  - Business tax returns (for self-employed)
  - Bank statements (1 month, 2 months, 3 months)
  - Investment account statements
  - Retirement account statements
  - Current debt statements (credit cards, student loans, auto loans)
  - Employment verification letter
  - Letter explaining employment gap/job change
  - Gift letter (for down payment gifts)
  - Purchase agreement (for vehicle or property)
  - Vehicle information (VIN, title)
  - Property appraisal
  - Homeowners insurance quote
  - Divorce decree (if applicable)
  - Bankruptcy discharge papers (if applicable)
  - Reference letters
  - Business license (for self-employed)
  - Rental history/landlord references

**Expected Outputs:**
- **Document Classification:** For each selected document, system indicates:
  - **Critical** (application cannot proceed without this): Green border
  - **Supporting** (strengthens application but not mandatory): Blue border
  - **Not Needed** (not relevant for this loan type/borrower): Gray, crossed out
- **Completeness Score:** Percentage of critical documents selected
- **Feedback Report:**
  - "Missing Critical Documents": List of required items student didn't select
  - "Unnecessary Documents Included": List of items student selected that aren't needed
  - "Special Circumstances Addressed": Whether student identified documentation needed for unique situations (self-employment, gift funds, job change)
- **Explanation for Each Document:** Why it's needed and what it proves
  - Example: "2 months of bank statements - Verifies down payment source and ensures funds aren't borrowed; tracks deposits to confirm income"

**Interaction Model:**
1. Student selects one of three borrower profiles
2. System displays profile details including employment situation and special circumstances
3. Student reviews provided document list
4. Student selects all documents they believe are required
5. Student can mark each selected document as "Critical" or "Supporting"
6. Student submits checklist
7. System provides feedback on:
   - Correctly identified critical documents
   - Missed critical documents (explains why they're needed)
   - Incorrectly included documents (explains why they're not needed)
   - Special circumstance documentation (did student catch that Andre is self-employed and needs tax returns? Did student realize Keisha needs a gift letter?)
8. Student can revise selections based on feedback and resubmit
9. Partner comparison feature: Two students can compare their lists and see differences

**Design Notes:**
- Use icons for document types (📄 for forms, 💰 for financial statements, 🏠 for property docs)
- Group documents by category (Personal Identity, Income Verification, Asset Documentation, Debt Information, Property/Collateral)
- Implement search/filter to help students find specific documents in the list
- Show running count: "15 of 25 documents selected"
- Include a "Why is this needed?" button for each document
- Provide a "Typical Timeline" showing when to gather each document (e.g., "Get pre-approval letter: 1-2 months before purchase")
- Make checklist downloadable as PDF for student reference
- Estimated development time: 8-10 hours

### 3. Application Strength Analyzer (Five C's Evaluation Tool)

**Purpose:** Allow students to evaluate loan applications from a lender's perspective using the Five C's framework

**Format:** Interactive scoring rubric with calculation and recommendation engine

**Inputs:**
- **Borrower Scenario Selection:** Student chooses one of three borrowers:
  - **Borrower 1 (Jamal)**: 24, $42,000 income, 650 credit, $8,000 student loans, $3,000 credit card debt, $2,500 savings, seeking $18,000 auto loan with $1,500 down
  - **Borrower 2 (Sarah)**: 28, $55,000 income, 740 credit, $15,000 student loans, $500 credit card debt, $12,000 savings, seeking $180,000 mortgage with 10% down
  - **Borrower 3 (Marcus)**: 22, $35,000 income, 580 credit, $12,000 student loans, $4,500 credit card debt, $800 savings, seeking $8,000 personal loan for debt consolidation
- **Five C's Scoring Interface:** For each C, student provides:
  - **Numerical Score:** 1-10 scale (1 = very poor, 10 = excellent)
  - **Justification:** Text field explaining the score (required)
- **Character (Credit History):**
  - Scoring guide provided: 750+ = 9-10, 700-749 = 7-8, 650-699 = 5-6, 600-649 = 3-4, Below 600 = 1-2
- **Capacity (Ability to Repay):**
  - Student calculates DTI (tool provides calculator)
  - Scoring guide: DTI <20% = 9-10, 20-30% = 7-8, 30-40% = 5-6, 40-50% = 3-4, >50% = 1-2
- **Capital (Financial Resources):**
  - Student evaluates savings relative to loan amount and down payment
  - Scoring guide: Reserves >6 months payments = 9-10, 3-6 months = 7-8, 1-3 months = 5-6, <1 month = 3-4, None = 1-2
- **Collateral (Secured Loans):**
  - For auto/mortgage: Student calculates LTV
  - Scoring guide: LTV <70% = 9-10, 70-80% = 7-8, 80-90% = 5-6, 90-95% = 3-4, >95% = 1-2
  - For unsecured loans: Mark as N/A
- **Conditions (Loan Purpose & Economic Context):**
  - Student evaluates whether loan makes financial sense
  - Scoring guide: Excellent purpose/timing = 9-10, Good = 7-8, Neutral = 5-6, Questionable = 3-4, Poor = 1-2

**Expected Outputs:**
- **Overall Creditworthiness Score:** Weighted average of the Five C's
  - Character: 30% weight
  - Capacity: 30% weight
  - Capital: 20% weight
  - Collateral: 15% weight (or redistributed to other C's if N/A)
  - Conditions: 5% weight
- **Lending Recommendation:**
  - **Approve at Premium Terms** (Score 80-100): "This borrower shows exceptional creditworthiness across all factors. Offer best available rate."
  - **Approve at Standard Terms** (Score 65-79): "This borrower meets all standard criteria. Approve at market rate."
  - **Approve with Conditions** (Score 50-64): "Moderate concerns require mitigation. Approve with [specific conditions]: larger down payment, co-signer, or higher interest rate to offset risk."
  - **Conditional Decline** (Score 35-49): "Significant concerns make approval difficult. Decline unless borrower can [specific improvements]: substantially increase down payment, provide qualified co-signer, or reduce DTI."
  - **Decline** (Score 0-34): "Multiple serious red flags. Decline application. Borrower needs to [specific actions] before reapplying."
- **Detailed Analysis Report:**
  - Summary of each C's score and justification
  - Identification of strongest and weakest C's
  - Specific risk factors flagged
  - Recommended conditions for approval (if applicable)
  - Actions borrower could take to improve application
- **Comparison with "Expert" Evaluation:** System shows how a professional underwriter would score the same borrower, highlighting differences

**Interaction Model:**
1. Student selects one of three borrower scenarios
2. System displays complete financial profile
3. Student evaluates each of the Five C's, providing score (1-10) and written justification
4. For Capacity and Collateral, student uses built-in calculator to determine DTI or LTV
5. Student submits evaluation
6. System calculates weighted overall score
7. System generates lending recommendation based on score
8. System shows "Expert Evaluation" comparison, explaining differences
9. Student can adjust scores based on expert comparison and resubmit
10. In group phase: Students who evaluated different borrowers share and discuss
11. System provides "Lending Committee" discussion questions comparing all three borrowers

**Design Notes:**
- Provide scoring rubrics/guides prominently for each C
- Include calculator tools embedded in Capacity and Collateral sections
- Use slider interface for 1-10 scores with labels (Very Poor - Poor - Fair - Good - Excellent)
- Require justification text (minimum 20 characters) to prevent arbitrary scoring
- Color-code final recommendation (Green = Approve Premium, Blue = Approve Standard, Yellow = Conditional, Orange = Decline Conditional, Red = Decline)
- Show visual representation of Five C's scores (radar chart showing strengths/weaknesses)
- Include "What would make this borrower approvable?" suggestions for declined applications
- Estimated development time: 10-12 hours

### 4. Creditworthiness Improvement Planner

**Purpose:** Help students assess their current financial situation and create actionable plans to strengthen future loan applications

**Format:** Interactive planning tool with SWOT analysis and action tracking

**Inputs:**
- **Current Financial Assessment:**
  - Estimated credit score (or "No credit history yet" option)
  - Current monthly income (pre-tax)
  - List of current debts: Name, balance, monthly payment for each
  - Current total savings
  - Employment status: Not employed, Part-time, Full-time
  - Time at current job: Less than 6 months, 6-12 months, 1-2 years, 2+ years
- **Future Loan Goal:**
  - Type of loan anticipated in next 2-3 years: Auto, Personal, Student, Mortgage, Other
  - Approximate amount needed
  - Timeframe: Within 1 year, 1-2 years, 2-3 years
- **Improvement Action Selection:**
  - Student selects from list of possible actions:
    - **Credit Building:** Become authorized user, open secured credit card, apply for credit-builder loan, dispute credit report errors, pay all bills on time for 6 months
    - **Debt Reduction:** Pay off specific debts, reduce credit card balances below 30% utilization, avoid new debt
    - **Savings Building:** Save $X per month, build emergency fund, increase down payment fund
    - **Income Improvement:** Seek raise/promotion, take on additional hours, start side income
    - **Employment Stability:** Stay in current position, avoid job changes, gain relevant skills
    - **Documentation Preparation:** Gather tax returns, organize bank statements, obtain employment verification letter
- For each selected action:
  - Target completion date
  - Specific measurable goal (e.g., "Reduce credit card balance from $2,000 to $600" not just "Pay down debt")
  - How this addresses which of the Five C's

**Expected Outputs:**
- **Current Position SWOT Analysis:**
  - **Strengths:** Factors working in student's favor (e.g., "No debt", "Stable employment", "Good income for age")
  - **Weaknesses:** Factors that would limit approval or result in poor terms (e.g., "No credit history", "High DTI", "Limited savings")
  - **Opportunities:** Realistic improvements achievable in 6-12 months (e.g., "Can build credit with secured card", "Can save $100/month")
  - **Threats:** Potential obstacles (e.g., "Uncertain job stability", "Temptation to overspend", "Medical expenses")
- **Projected Improvement Impact:**
  - If actions are completed, estimated credit score improvement (e.g., "+30 to +50 points")
  - Projected DTI improvement (e.g., "Current: 35%, After plan: 28%")
  - Projected savings increase (e.g., "Current: $800, After 12 months: $2,000")
  - How these improvements affect approval likelihood for stated goal
- **Interest Rate Impact Estimate:**
  - Current likely rate for goal loan: X%
  - Projected rate after improvements: Y%
  - Dollar savings over life of loan: $Z
  - Example: "Improving credit score from 620 to 680 could reduce your auto loan rate from 8.5% to 6.5%, saving approximately $1,800 over a 5-year, $20,000 loan."
- **6-12 Month Action Plan:**
  - Month-by-month milestones
  - Specific tasks with deadlines
  - Progress tracking checkboxes
  - Recommended timeline for when to apply for actual loan
- **Priority Ranking:** Tool identifies which actions have highest impact and should be prioritized

**Interaction Model:**
1. Student inputs current financial situation (credit score estimate, income, debts, savings, employment)
2. Student selects anticipated loan need and timeframe
3. System performs SWOT analysis, identifying strengths/weaknesses/opportunities/threats
4. Student reviews available improvement actions and selects relevant ones
5. For each action, student sets specific measurable goal and target date
6. System calculates projected improvements (credit score, DTI, savings)
7. System estimates impact on approval likelihood and interest rates
8. System generates month-by-month action plan with milestones
9. System calculates dollar impact of improvements (interest savings)
10. Student can save plan and return to update progress
11. System provides motivational feedback when milestones are achieved
12. Optional: Share one action with class (anonymous or identified)

**Design Notes:**
- Use friendly, encouraging tone ("Great starting point!" not "Your credit is bad")
- For students with no credit: Emphasize this is normal, provide specific credit-building pathway
- For students with no income: Focus on actions they CAN control (learning about credit, avoiding debt)
- Include visual timeline showing current position → actions → goal
- Provide examples for each action type (e.g., "Example: Become authorized user on parent's card that has 5+ years of good payment history")
- Calculator showing interest rate impact in real dollars (very motivating)
- Make plan printable/downloadable/email-able
- Include motivational quotes or statistics ("Students who plan credit-building 6 months before applying save average of $1,500 on auto loans")
- Estimated development time: 12-15 hours

---

## Downloadable Resources (Printable PDFs)

All interactive tools must have printable PDF alternatives for accessibility and technology equity.

### PDF 1: Loan Application Worksheet (Auto/Personal/Mortgage)

**Purpose:** Printable version of the Loan Application Simulator for students without reliable technology access

**Format:** 4-6 page PDF fillable form

**Contents:**
- Three versions: One each for Auto Loan, Personal Loan, and Mortgage
- All form fields from the digital simulator
- Space for student to manually calculate DTI and LTV
- Rubric for self-assessment of application strength
- Checklist of common errors to avoid

**Design Notes:**
- Professional loan application format (mirrors real applications)
- Fill-in-the-blank style with clear instructions
- Include formulas for DTI and LTV calculations
- Provide answer key with example completed application
- Print in black and white for accessibility

### PDF 2: Documentation Checklist by Loan Type

**Purpose:** Reference guide showing required documentation for each loan type

**Format:** 2-page PDF chart

**Contents:**
- Three columns: Auto Loan, Personal Loan, Mortgage
- Rows for each document type with checkboxes
- Special sections for complicated scenarios (self-employed, co-signers, gift funds)
- Timeline showing when to gather each document

**Design Notes:**
- Simple checklist format for easy reference
- Include brief explanation of why each document is needed
- Laminated version could be reusable classroom poster
- Available in English and Spanish

### PDF 3: Five C's Evaluation Rubric

**Purpose:** Printable scoring guide for evaluating loan applications

**Format:** 2-page PDF rubric and worksheet

**Contents:**
- Definition of each C
- 1-10 scoring rubric for each C with descriptions
- Space to write justifications
- Formula for calculating weighted overall score
- Lending recommendation guidelines
- Three borrower scenarios to evaluate

**Design Notes:**
- Easy-to-follow table format
- Include sample evaluation as example
- Calculator-friendly layout
- Can be used for homework or assessment

### PDF 4: Personal Creditworthiness Improvement Plan Template

**Purpose:** Printable planning tool for students to create improvement strategies

**Format:** 4-page PDF worksheet

**Contents:**
- Current situation assessment (credit, income, debts, savings)
- SWOT analysis template
- Action selection worksheet with space for 6-8 actions
- Monthly timeline (12-month view)
- Progress tracking chart
- Interest rate impact calculator table

**Design Notes:**
- Professional planning template (students feel like they're creating a real financial plan)
- Space for goal-setting and milestone tracking
- Includes motivational prompts
- Can be hole-punched for binder

### PDF 5: Loan Application Quick Reference Guide

**Purpose:** One-page summary of key concepts for student reference

**Format:** 1-page front/back PDF

**Contents:**
- Front side:
  - Five C's definitions
  - DTI calculation formula and guidelines
  - LTV calculation formula and guidelines
  - Credit score ranges and what they mean
  - Required documentation list by loan type
- Back side:
  - Common loan application mistakes to avoid
  - Tips for strengthening applications
  - Red flags that delay or deny applications
  - Resources for credit building and financial assistance

**Design Notes:**
- Compact, reference-card style
- Could be printed on cardstock for durability
- Visually appealing with icons and color coding
- Students can keep in wallet or binder for future reference

---

## State-Specific Asset Customization

Several assets can be enhanced with state-specific data:

### Loan Application Simulator
- Pre-populate average interest rates with {{STATE_AVG_AUTO_LOAN_RATE_NEW}}, {{STATE_AVG_AUTO_LOAN_RATE_USED}}, {{STATE_AVG_MORTGAGE_RATE_30YR}}
- Include {{STATE_MEDIAN_HOME_PRICE}} in mortgage scenarios for local relevance
- Reference {{STATE_CONSUMER_PROTECTION_URL}} in feedback for predatory lending warnings

### Creditworthiness Improvement Planner
- Link to {{STATE_CREDIT_UNION_ASSOCIATION_URL}} for first-time borrower programs
- Reference {{STATE_FIRST_TIME_HOMEBUYER_PROGRAM}} if applicable
- Include {{STATE_CONSUMER_PROTECTION_URL}} for credit counseling resources

### Downloadable PDFs
- Include state-specific resources list in Quick Reference Guide
- Note any state-specific lending regulations or consumer protections
- Reference local nonprofit credit counseling agencies

**Note:** State-specific data auto-populates in platform. For printable PDFs, create template versions with {{VARIABLES}} that can be batch-generated for each state.

---

## Asset Development Priority

For phased implementation, prioritize in this order:

1. **Loan Application Simulator** (PRIMARY SKILL BUILDER) - Critical for Day 1 and Day 2
2. **Creditworthiness Improvement Planner** - Highest personal relevance, strong student engagement
3. **Documentation Checklist Builder** - Shorter development time, high educational value
4. **Application Strength Analyzer** - Valuable but more complex; could be simplified version initially
5. **Printable PDFs** - Create alongside digital tools for accessibility

Estimated total development time for all digital assets: 45-60 hours

---

## Accessibility Requirements

All digital tools must meet:
- **WCAG 2.1 AA** standards for web accessibility
- **Screen reader compatibility** for visually impaired students
- **Keyboard navigation** for students who cannot use a mouse
- **Color contrast** sufficient for colorblind users (don't rely solely on color to convey meaning)
- **Text resize** capability without breaking layout
- **Alternative text** for all images and icons
- **Printable PDF alternatives** for students without reliable technology access

---

## Technical Specifications

**Platform Compatibility:**
- Web-based (accessible via modern browsers: Chrome, Firefox, Safari, Edge)
- Mobile-responsive design (works on tablets and phones)
- No plugins required (HTML5, CSS3, JavaScript)

**Data Storage:**
- Student work should be saveable and retrievable
- Progress tracking across sessions
- Option to download/export results
- Data privacy compliant (FERPA, COPPA)

**Performance:**
- Load time under 3 seconds on standard school internet
- Real-time feedback without noticeable lag
- Handles 30+ simultaneous users without performance degradation

**Integration:**
- Can embed in Learning Management Systems (Canvas, Schoology, Google Classroom)
- Single sign-on compatible
- Gradebook integration for teacher dashboards

---

This comprehensive asset specification provides the development team with all information needed to build the interactive tools and resources for L-57.

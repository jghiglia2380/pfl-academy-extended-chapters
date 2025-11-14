# Asset Specifications for L-49: Scarcity, Opportunity Cost, and Incentives

## Day 1 Assets

### 1. Time Scarcity Visualization
- **Purpose:** Illustrate how limited time creates scarcity for everyone
- **Format/Inputs:** Static infographic (SVG or high-res PNG)
- **Expected Outputs:** Clear visual showing 168-hour weekly breakdown
- **Interaction Model:** Static display
- **Design Notes:**
  - Circle or pie chart showing 168 hours/week
  - Segments labeled and color-coded:
    - Sleep: 56 hours (8/night) - Blue
    - School: 40 hours - Yellow
    - Eating/hygiene: 21 hours - Green
    - Remaining: 51 hours for everything else - Red (highlight this)
  - Annotation: "Only 51 hours for work, homework, friends, exercise, hobbies, entertainment, family"
  - Visual emphasis on the small remaining slice
  - Responsive design for mobile/desktop viewing

### 2. Opportunity Cost Formula Visual
- **Purpose:** Provide clear visual reference for opportunity cost concept
- **Format/Inputs:** Static graphic with examples
- **Expected Outputs:** Quick reference students can return to
- **Interaction Model:** Static display (could be interactive hover for examples)
- **Design Notes:**
  - **Main Formula Box:**
    ```
    Opportunity Cost =
    Value of Next Best Alternative
    ```
  - **Example 1: Friday Night**
    - Visual: Three options shown as cards
    - Card 1: Movie ($30 spent + $60 forgone earnings = $90 total cost)
    - Card 2: Work ($60 earned, forgone fun)
    - Card 3: Study ($0 spent, potential better grade)
    - Arrows showing opportunity cost relationships
  - **Example 2: College**
    - Total Economic Cost = Explicit Costs + Opportunity Costs
    - Visual equation with numbers filled in
  - Color coding: Explicit costs (purple), Opportunity costs (orange), Total (green)

### 3. Explicit vs. Implicit Costs Comparison Table
- **Purpose:** Help students distinguish between two cost types
- **Format/Inputs:** Interactive comparison table
- **Expected Outputs:** Clear understanding of differences
- **Interaction Model:**
  - Static table with examples
  - Optional: Clickable scenarios that reveal cost breakdowns
- **Design Notes:**
  - Two-column comparison table
  - **Column 1: Explicit Costs (Purple header)**
    - Definition: Out-of-pocket payments
    - Characteristics: Easy to measure, shows in bank account
    - Examples: Tuition, rent, groceries, car payment
  - **Column 2: Implicit Costs / Opportunity Costs (Orange header)**
    - Definition: Value of alternatives you give up
    - Characteristics: Harder to measure, doesn't show in bank account, usually larger
    - Examples: Forgone earnings, forgone investment returns, time cost
  - **Practice Scenarios:** Clickable cards that reveal breakdown:
    - "Buy a car": Explicit ($15,000 purchase) vs. Implicit ($15,000 not invested = $X forgone growth)
    - "Go to college": Explicit (tuition + books) vs. Implicit (forgone earnings)
    - "Keep cash in checking": Explicit ($0) vs. Implicit (inflation loss + forgone interest)
  - Mobile-responsive design with collapsible sections

### 4. Incentives in Economic Systems Comparison
- **Purpose:** Connect opportunity cost/incentives back to L-48 economic systems
- **Format/Inputs:** Animated or interactive comparison
- **Expected Outputs:** Understanding of how different incentive structures produce different outcomes
- **Interaction Model:** Tab or accordion interface comparing systems
- **Design Notes:**
  - Three tabs/sections: Market Economy | Command Economy | Mixed Economy
  - For each system, show:
    - **Key Incentives:**
      - Market: Property rights, profit motive, competition, prices
      - Command: Quotas, state directives, egalitarianism
      - Mixed: Combination of both + social safety nets
    - **Behavioral Responses:**
      - Market: Innovation, hard work, risk-taking, customer service
      - Command: Meeting quotas (not quality), black markets, low motivation
      - Mixed: Balancing profit with social responsibility
    - **Personal Finance Impact:**
      - Market: High earning potential, high risk, personal responsibility
      - Command: Low earning potential, low risk, limited opportunities
      - Mixed: Moderate both
  - **Classic Example Highlighted:** Soviet Nail Factory
    - Incentive: Produce 10,000 nails
    - Response: Made 10,000 tiny, useless nails
    - Lesson: "Incentives matter; design determines outcomes"
  - Visual: Icons and color coding for quick scanning
  - Connection to {{STATE_NAME}}: Highlight which incentives exist locally

### 5. Real-World Incentive Examples Interactive
- **Purpose:** Show how incentives operate in students' daily lives
- **Format/Inputs:** Interactive exploration of incentive examples
- **Expected Outputs:** Recognition of incentives all around them
- **Interaction Model:** Clickable categories revealing examples
- **Design Notes:**
  - **Categories:**
    1. **Positive Incentives** (Green cards)
       - Tax deductions for retirement savings
       - Overtime pay (1.5× regular rate)
       - College scholarships for good grades
       - Cash-back credit card rewards
       - Employee bonuses for performance
    2. **Negative Incentives** (Red cards)
       - Late fees on credit cards
       - Speeding tickets
       - Higher insurance rates after accidents
       - Overdraft fees
       - Tax penalties for early retirement withdrawal
    3. **{{STATE_NAME}}-Specific Incentives** (Blue cards)
       - {{STATE_TAX_INCENTIVES}}
       - {{STATE_NAME}} first-time homebuyer programs
       - {{STATE_NAME}} minimum wage {{STATE_MIN_WAGE}}
       - State university tuition {{STATE_TUITION_PUBLIC}}
       - Local economic development incentives
  - Each card expands to show:
    - What behavior it encourages/discourages
    - Who benefits
    - Typical impact on personal finance
  - Search/filter functionality
  - "Add Your Own" feature where students can submit incentives they notice

### 6. Unintended Consequences Case Studies
- **Purpose:** Teach students to think critically about incentive design
- **Format/Inputs:** Short case study cards with discussion prompts
- **Expected Outputs:** Understanding that incentives can backfire
- **Interaction Model:** Scroll-through case studies with reflection questions
- **Design Notes:**
  - **Case Study 1: Cobra Bounties (Colonial India)**
    - Problem: Too many cobras in Delhi
    - Solution: Government pays bounty for dead cobras
    - Result: People bred cobras to collect bounties; more cobras when program ended
    - Lesson: "Consider how people will ACTUALLY respond"
  - **Case Study 2: College Degree Inflation**
    - Incentive: Employers require degrees for jobs that didn't need them
    - Result: Everyone goes to college, student debt crisis, degree devaluation
    - Lesson: "When everyone responds the same way, the incentive loses power"
  - **Case Study 3: Fuel Economy Standards**
    - Incentive: Higher MPG requirements for cars
    - Unintended result: People drive more because per-mile cost is lower
    - Lesson: "Cheaper per use → more use (rebound effect)"
  - Each case includes:
    - Visual illustration
    - Timeline of events
    - Discussion questions
    - Links to additional reading

---

## Day 2 Assets

### 1. Opportunity Cost Calculator (PRIMARY SKILL BUILDER)
- **Purpose:** Interactive tool for comparing financial decisions with full cost analysis
- **Format/Inputs:** Web-based calculator with scenario templates and custom input
- **Expected Outputs:** Side-by-side comparison showing explicit costs, opportunity costs, and total economic costs
- **Interaction Model:** Form-based input with real-time calculation and visual comparison

**Scenario Templates Available:**
1. **College vs. Trade School vs. Workforce**
   - Input fields:
     - College tuition (default: {{STATE_TUITION_PUBLIC}})
     - Books/supplies per year
     - Housing choice (at home vs. on campus)
     - Part-time earnings potential
     - Expected starting salary after graduation
   - Calculations:
     - 4-year explicit costs
     - 4-year opportunity costs (forgone earnings - part-time work)
     - 10-year net wealth projection
   - Visual: Line graph showing cumulative wealth over 10 years for each path

2. **Buying vs. Leasing a Car**
   - Input fields:
     - Purchase price
     - Lease monthly payment
     - Lease term
     - Estimated resale value
     - Alternative investment return rate
   - Calculations:
     - Total cost of ownership vs. leasing
     - Opportunity cost (money not invested)
     - 5-year comparison
   - Visual: Bar chart comparing total costs

3. **Living at Home vs. Renting an Apartment**
   - Input fields:
     - Monthly rent in {{STATE_NAME}} (default: {{STATE_MEDIAN_RENT}})
     - Utilities and expenses
     - Savings from living at home
     - Duration (months)
   - Calculations:
     - Total housing cost
     - Opportunity cost (savings not invested)
     - Intangible factors (independence vs. savings)
   - Visual: Pie chart showing cost breakdown

4. **Spending vs. Investing $1,000**
   - Input fields:
     - Amount to spend/invest
     - Time horizon (years)
     - Expected return rate
     - Inflation rate
   - Calculations:
     - Future value if invested
     - Opportunity cost of spending now
     - Real value considering inflation
   - Visual: Growth curve showing compound interest effect

5. **Higher-Paying Job Far Away vs. Lower-Paying Local Job**
   - Input fields:
     - Job A salary
     - Job A location costs (rent, commute, relocation)
     - Job B salary
     - Job B location costs
     - Other factors (family proximity, stress, career growth)
   - Calculations:
     - Net income after location costs
     - Time cost (commute hours)
     - Opportunity cost of time and relationships
   - Visual: Comparison table with intangible factors rated

**Technical Specifications:**
- Responsive design (mobile, tablet, desktop)
- Real-time calculations (no page refresh)
- Save scenario functionality
- Export to PDF option
- {{STATE_NAME}}-specific defaults (tuition, rent, minimum wage)
- Shareable results (unique URL for each calculation)
- Embed video tutorial explaining how to use calculator

**Data Sources:**
- {{STATE_NAME}} public university tuition: State higher education website
- {{STATE_NAME}} median rent: Zillow or Census data
- Investment return assumptions: Historical S&P 500 average (~10% nominal, ~7% real)
- Inflation rate: Federal Reserve target (2%)

### 2. Monthly Budget Allocation Tool
- **Purpose:** Help students practice opportunity cost thinking in everyday spending
- **Format/Inputs:** Interactive budget builder with visual feedback
- **Expected Outputs:** Completed budget showing trade-offs and opportunity costs
- **Interaction Model:** Drag-and-drop or slider-based allocation

**Features:**
- **Income Input:**
  - Monthly income field (default: $1,200 for part-time student)
  - Auto-calculate required expenses ($330)
  - Show discretionary income ($870)

- **Allocation Categories:**
  - Emergency Fund (slider: $0-$500)
  - Car Savings (slider: $0-$500)
  - College/Training Savings (slider: $0-$500)
  - Entertainment/Social (slider: $0-$400)
  - Clothing/Shopping (slider: $0-$300)
  - Other (custom field)

- **Visual Feedback:**
  - Pie chart showing allocation percentages
  - Progress bars for each category
  - Remaining budget indicator (red if over, green if balanced)
  - "Months to Goal" calculator for savings categories

- **Opportunity Cost Display:**
  - For each category, show: "If invested at 8% instead, would be worth $X in 5 years"
  - Highlight trade-offs: "Spending $200 on entertainment means $200 less for car savings"

- **50/30/20 Rule Comparison:**
  - Show recommended allocation per rule
  - Compare student's allocation to rule
  - Explain when deviating from rule makes sense

- **Save & Compare:**
  - Save multiple budget scenarios
  - Compare side-by-side
  - Track actual spending vs. planned budget (if used over time)

**Technical Specifications:**
- Mobile-first design
- Touch-friendly sliders
- Auto-save to localStorage
- Export to CSV/Excel
- Print-friendly format

### 3. Personal Incentive System Designer
- **Purpose:** Help students create actionable incentive systems for their goals
- **Format/Inputs:** Guided form with examples and best practices
- **Expected Outputs:** Customized incentive plan students can implement
- **Interaction Model:** Step-by-step wizard with validation

**Step 1: Goal Definition**
- Input: Specific financial goal (SMART framework)
- Examples provided:
  - "Save $2,000 for car down payment by June 30"
  - "Reduce discretionary spending by $100/month for 6 months"
  - "Increase income by $200/month through side hustle"
- Validation: Is goal specific, measurable, time-bound?

**Step 2: Positive Incentives (Rewards)**
- Input fields:
  - Small milestone (% of goal): Reward
  - Medium milestone (% of goal): Reward
  - Goal completion: Reward
- Examples:
  - "25% saved → Dinner at favorite restaurant ($30)"
  - "50% saved → New shoes ($75)"
  - "100% saved → Weekend trip ($200 from saved interest)"
- Validation: Are rewards proportional? Do they undermine goal?

**Step 3: Negative Incentives (Consequences)**
- Input fields:
  - If I miss weekly target: Consequence
  - If I spend outside budget: Consequence
  - Accountability partner: Name
- Examples:
  - "Miss target → Skip streaming service for one week"
  - "Overspend → Extra work shift to make up difference"
  - "Accountability partner: Mom checks my savings every Friday"
- Validation: Are consequences enforceable? Too harsh or too lenient?

**Step 4: Structural Incentives (Make It Easy)**
- Input fields:
  - Automate savings: Amount and frequency
  - Remove temptations: What to delete/avoid
  - Visual tracking method: How will you track?
- Examples:
  - "Auto-transfer $75/week to separate savings account"
  - "Delete food delivery apps, unsubscribe from marketing emails"
  - "Wall chart with stickers for each $100 saved"

**Step 5: Social Incentives (Peer Support)**
- Input fields:
  - Accountability buddy: Name and how they'll help
  - Public commitment: Who will you tell?
  - Friendly competition: Challenges with friends
- Examples:
  - "Best friend checks in every Sunday"
  - "Post progress on social media monthly"
  - "Challenge roommate to save together, compare results"

**Step 6: Review & Export**
- Display complete incentive plan
- Check alignment with goal
- Export as PDF
- Set phone reminders for check-ins
- Email plan to self and accountability partner

**Gamification Elements:**
- Progress bar
- Achievement badges for completing steps
- Example incentive systems from other students (anonymized)
- "Success rate" predictor based on incentive design quality

**Technical Specifications:**
- Progress saving (localStorage or user account)
- Mobile-responsive
- PDF export with professional formatting
- Optional integration with calendar apps for reminders
- Social sharing options (text, email, social media)

### 4. {{STATE_NAME}} Policy Incentives Explorer
- **Purpose:** Help students understand and leverage state-specific incentive policies
- **Format/Inputs:** Interactive database of {{STATE_NAME}} policies
- **Expected Outputs:** Personalized list of incentives student can use
- **Interaction Model:** Searchable/filterable database with personal relevance indicators

**Policy Categories:**

1. **Education Incentives**
   - {{STATE_NAME}} college savings plans (529 benefits)
   - State university tuition rates ({{STATE_TUITION_PUBLIC}})
   - Scholarship programs (merit, need-based, specific fields)
   - Apprenticeship and trade school incentives
   - Loan forgiveness programs for public service
   - Each listing includes:
     - Description
     - Who qualifies
     - How to apply
     - Personal finance impact
     - Opportunity cost (what you give up to qualify)

2. **Housing Incentives**
   - First-time homebuyer programs
   - Down payment assistance
   - Property tax exemptions
   - Energy efficiency rebates
   - {{STATE_NAME}} median rent for comparison: {{STATE_MEDIAN_RENT}}

3. **Employment Incentives**
   - Minimum wage: {{STATE_MIN_WAGE}}
   - Earned Income Tax Credit (state supplement)
   - Job training grants
   - Unemployment benefits and requirements
   - Worker protection laws

4. **Tax Incentives**
   - {{STATE_TAX_INCENTIVES}}
   - Retirement savings tax benefits
   - Dependent care credits
   - Education expense deductions
   - Charitable contribution deductions

5. **Small Business & Entrepreneurship**
   - Business startup resources
   - Small Business Administration (SBA) programs in {{STATE_NAME}}
   - Minority/women-owned business incentives
   - Economic development zones
   - Microloan programs

**Interaction Features:**
- **Personalization Quiz:**
  - "What are your goals?" (college, homeownership, business, etc.)
  - "What's your situation?" (student, working, family status)
  - Results: "5 {{STATE_NAME}} incentives relevant to you"

- **Opportunity Cost Calculator Integration:**
  - "If you use this incentive, you save $X"
  - "Opportunity cost of not using: $X over Y years"
  - Visual comparison

- **Action Plan Generator:**
  - "Here's how to take advantage of this incentive:"
  - Step-by-step instructions
  - Links to application forms
  - Deadline reminders

- **Comparison Tool:**
  - Compare {{STATE_NAME}} to neighboring states
  - "Is {{STATE_NAME}} more or less generous?"
  - Migration implications (should you consider moving for better incentives?)

**Data Sources:**
- {{STATE_NAME}} Department of Revenue
- {{STATE_NAME}} Department of Commerce/Economic Development
- {{STATE_NAME}} Higher Education Commission
- {{STATE_NAME}} Housing Finance Agency
- Tax Foundation state-by-state comparisons

**Technical Specifications:**
- Searchable database
- Filter by: category, eligibility, benefit amount
- Sort by: personal relevance, benefit size, ease of use
- Mobile-friendly cards with expand/collapse details
- Save favorites
- Email summary of relevant incentives
- Annual updates as policies change

### 5. College vs. Alternative Paths Detailed Calculator
- **Purpose:** Extended version of Activity 1 with more customization
- **Format/Inputs:** Multi-step calculator with scenario builder
- **Expected Outputs:** Comprehensive financial analysis of post-high school options
- **Interaction Model:** Wizard-style form with real-time calculations and visualizations

**Path Options:**
1. **4-Year Public University ({{STATE_NAME}})**
2. **4-Year Private University**
3. **Community College (2 years) → Transfer to 4-year**
4. **Trade School / Apprenticeship**
5. **Military Service with Education Benefits**
6. **Immediate Workforce Entry**
7. **Gap Year → Career Path**
8. **Custom Path (student defines)**

**Input Variables:**
- Tuition per year
- Books and supplies
- Housing (at home, on campus, off campus)
- Transportation costs
- Part-time work earnings
- Full-time starting salary (if not in school)
- Expected post-graduation salary
- Years to completion
- Loan interest rates (if borrowing)
- Scholarship/grant amounts

**Calculations:**
- **4-Year Costs:**
  - Total explicit costs
  - Total opportunity costs (forgone earnings)
  - Total economic cost
  - Net cost after financial aid
- **10-Year Net Wealth:**
  - Cumulative earnings
  - Minus costs
  - Plus projected salary growth
- **20-Year Net Wealth:**
  - Extended projection
  - Compound effect of higher earnings
- **Break-Even Analysis:**
  - Year when college graduate surpasses non-college paths in cumulative wealth
- **Loan Payoff Timeline:**
  - If borrowing, when will loans be paid off?
  - Total interest paid

**Visualizations:**
- **Line Graph:** Cumulative wealth over time for each path
- **Bar Chart:** Total costs comparison (explicit vs. opportunity)
- **Table:** Year-by-year breakdown
- **Break-Even Point:** Visual indicator of when paths cross

**Scenarios & Sensitivity Analysis:**
- "What if tuition increases by 5% per year?"
- "What if you earn a higher salary ($10K more)?"
- "What if you take 5 years instead of 4?"
- "What if you attend community college first (2+2)?"
- Slider-based sensitivity analysis showing how changes affect outcomes

**Decision Support:**
- **Non-Financial Factors Checklist:**
  - Career fit and passion
  - Job market demand
  - Geographic flexibility
  - Physical demands
  - Work-life balance
  - Advancement potential
  - Job security
- **Weight these factors** (1-10 scale)
- **Integrated scoring** (financial + non-financial)

**Comparison to {{STATE_NAME}} Averages:**
- Average student debt in {{STATE_NAME}}
- Average starting salary by field
- Employment rates by education level
- Show "You compared to average"

**Export Options:**
- PDF report
- Excel spreadsheet with formulas
- Shareable link
- Email to parents/counselors

---

## Downloadable Resources (Printable PDFs)

### 1. Opportunity Cost Analysis Worksheet
- **Purpose:** Structured guide for Day 1 learning
- **Format:** 2-page PDF worksheet
- **Content:**
  - **Page 1:** Definitions and examples
    - Scarcity definition with examples
    - Opportunity cost formula and practice problems
    - Explicit vs. implicit costs table (fill-in-the-blank)
  - **Page 2:** Application questions
    - Calculate opportunity cost for 3 scenarios
    - Identify explicit and implicit costs
    - Connect to {{STATE_NAME}} context
  - Answer key for teachers

### 2. Day 2 Learning Lab Activity Packet
- **Purpose:** All Day 2 activities in printable format
- **Format:** 8-page PDF packet
- **Content:**
  - **Page 1:** Activity 1 - College vs. Alternative Paths (calculation tables)
  - **Page 2:** Activity 1 - 10-Year Comparison and Analysis Questions
  - **Page 3:** Activity 2 - Monthly Budget Allocation (table and questions)
  - **Page 4:** Activity 2 - Analysis Questions and 50/30/20 Rule Comparison
  - **Page 5:** Activity 3 - Personal Incentive System Designer (template)
  - **Page 6:** Activity 4 - {{STATE_NAME}} Policy Incentives (table and analysis)
  - **Page 7:** Opportunity Cost Calculator (blank template for any decision)
  - **Page 8:** Reflection questions and self-assessment
  - State-specific version auto-populated with {{STATE_NAME}} data

### 3. {{STATE_NAME}} Financial Incentives Fact Sheet
- **Purpose:** Quick reference for state-specific policies
- **Format:** 1-page double-sided reference card
- **Content (Front):**
  - Key {{STATE_NAME}} tax incentives
  - Education incentives (tuition, scholarships, 529 plans)
  - Housing incentives (first-time buyer, down payment assistance)
  - Employment data (minimum wage, unemployment rate)
  - Cost of living index
- **Content (Back):**
  - How to take advantage of each incentive
  - Eligibility requirements
  - Application processes and deadlines
  - Links to {{STATE_NAME}} government resources
  - Comparison to neighboring states

### 4. Scarcity and Opportunity Cost Vocabulary Glossary
- **Purpose:** Reference for key terms and concepts
- **Format:** 2-page PDF with definitions and examples
- **Content:**
  - Scarcity
  - Opportunity cost
  - Explicit costs
  - Implicit costs
  - Incentive (positive and negative)
  - Trade-off
  - Marginal analysis
  - Sunk cost (and sunk cost fallacy)
  - Each term includes:
    - Clear definition
    - Example in context
    - Relevance to personal finance
    - {{STATE_NAME}}-specific application where relevant

### 5. Decision-Making Framework Guide
- **Purpose:** Systematic process for applying opportunity cost analysis to any decision
- **Format:** 1-page PDF decision flowchart
- **Content:**
  - **Step 1:** Define the decision clearly
  - **Step 2:** List all realistic alternatives
  - **Step 3:** Calculate explicit costs for each alternative
  - **Step 4:** Identify and estimate opportunity costs
  - **Step 5:** Consider non-financial factors (intangibles)
  - **Step 6:** Make informed choice
  - **Step 7:** Review decision after implementation (learn for next time)
  - Visual flowchart format
  - Example walkthrough using college decision
  - Blank template to fill in for personal decisions

### 6. Incentive Design Checklist
- **Purpose:** Help students create effective incentive systems
- **Format:** 1-page PDF checklist
- **Content:**
  - **Goal Definition:**
    - [ ] Specific
    - [ ] Measurable
    - [ ] Achievable
    - [ ] Relevant
    - [ ] Time-bound
  - **Positive Incentives:**
    - [ ] Clear triggers
    - [ ] Meaningful rewards
    - [ ] Proportional to effort
    - [ ] Don't undermine goal
  - **Negative Incentives:**
    - [ ] Enforceable
    - [ ] Not too harsh
    - [ ] Clear consequences
  - **Structural Incentives:**
    - [ ] Automated where possible
    - [ ] Removed temptations
    - [ ] Visual tracking
  - **Social Incentives:**
    - [ ] Accountability partner identified
    - [ ] Public commitment made
    - [ ] Check-in schedule set
  - Examples of well-designed incentive systems

---

## Asset Development Priority

**Phase 1 (Essential for Launch):**
1. Opportunity Cost Calculator (primary skill builder for Day 2)
2. Time Scarcity Visualization
3. Opportunity Cost Formula Visual
4. Day 2 Learning Lab Activity Packet (printable)
5. {{STATE_NAME}} Financial Incentives Fact Sheet

**Phase 2 (Enhances Experience):**
6. Monthly Budget Allocation Tool
7. Personal Incentive System Designer
8. Explicit vs. Implicit Costs Comparison Table
9. Opportunity Cost Analysis Worksheet (printable)
10. Vocabulary Glossary

**Phase 3 (Nice to Have):**
11. Incentives in Economic Systems Comparison
12. Real-World Incentive Examples Interactive
13. Unintended Consequences Case Studies
14. {{STATE_NAME}} Policy Incentives Explorer
15. College vs. Alternative Paths Detailed Calculator
16. Decision-Making Framework Guide
17. Incentive Design Checklist

---

## Technical Implementation Notes

**State-Specific System Requirements:**
- All calculators must pull {{STATE_NAME}}-specific data:
  - Public university tuition: {{STATE_TUITION_PUBLIC}}
  - Median rent: {{STATE_MEDIAN_RENT}}
  - Minimum wage: {{STATE_MIN_WAGE}}
  - Tax incentives: {{STATE_TAX_INCENTIVES}}
  - Cost of living index
- State determined at district/admin level during LMS setup
- All content automatically displays correct {{STATE_NAME}} data
- Annual data updates (tuition, rent, wages update each summer)

**Accessibility:**
- All interactive tools must meet WCAG 2.1 AA standards
- Keyboard navigation required for all interactive elements
- Screen reader compatible (ARIA labels on all inputs/outputs)
- Color-blind friendly palettes (don't rely on color alone)
- Text alternatives for all visuals
- Adjustable text size

**Data Sources:**
- {{STATE_NAME}} Higher Education Commission (tuition data)
- Bureau of Labor Statistics (wage data, employment statistics)
- Zillow / Census Bureau (rent and housing data)
- {{STATE_NAME}} Department of Revenue (tax policies)
- Tax Foundation (state comparisons)
- Historical stock market data: S&P 500 average returns
- Inflation data: Federal Reserve / Bureau of Labor Statistics

**Performance Requirements:**
- Calculators must update in real-time (<100ms latency)
- Mobile-optimized for 3G connections
- All PDFs under 2MB for easy download
- Responsive design: mobile, tablet, desktop
- Works on all major browsers (Chrome, Firefox, Safari, Edge)

**Asset File Naming Convention:**
- `l49-{asset-name}-{version}.{ext}`
- Example: `l49-opportunity-cost-calculator-v1.html`
- Example: `l49-activity-packet-{{STATE_CODE}}-v1.pdf`
- Example: `l49-time-scarcity-viz-v1.svg`

**Integration Points:**
- Opportunity Cost Calculator embeds in Day 2 student content
- Monthly Budget Allocation Tool optional embed or standalone
- Downloadable PDFs linked from teacher guides
- {{STATE_NAME}} data pulls from central database (updated annually)
- User data (saved scenarios) stored in LMS database

---

## Assessment Integration

**Formative Assessment Tools:**
- Embedded quiz questions after key concepts
- Self-check calculators with immediate feedback
- "Did I understand?" reflection prompts

**Summative Assessment:**
- Completed Opportunity Cost Calculator (graded on accuracy and reasoning)
- Budget allocation with written justification
- Incentive system design (graded on quality and feasibility)
- {{STATE_NAME}} policy analysis (graded on depth and application)

**Rubrics Provided:**
- For each major activity
- Clear criteria for different performance levels
- Aligned with learning objectives

# L-47: Introduction to Investment Types - Assets Specification

This document specifies all interactive tools, calculators, and downloadable resources needed for L-47.

---

## Day 1 Assets

### 1. Investment Characteristics Visual Comparison Chart

**Purpose:** Help students visualize and compare key characteristics of stocks, bonds, mutual funds, and ETFs side-by-side

**Format:** Interactive comparison table / Static printable chart

**Inputs:**
- No user inputs required (displays standard comparison data)

**Expected Outputs:**
- Side-by-side comparison showing:
  - Historical average returns (stocks: ~10%, bonds: ~5%, funds/ETFs: varies by holdings)
  - Risk level (volatility indicators)
  - Liquidity (how quickly converted to cash)
  - Typical fees (expense ratios)
  - Minimum investment amounts
  - Income generation (dividends/interest)

**Interaction Model:**
- Students review pre-populated comparison chart
- Can toggle between detailed view and simplified view
- Can sort by different characteristics (risk, return, fees, etc.)
- Printable version available for accessibility

**Design Notes:**
- Use consistent color coding: Stocks (blue), Bonds (green), Mutual Funds (orange), ETFs (purple)
- Include visual indicators for risk (low/medium/high with icon system)
- Include tooltips explaining each characteristic
- Mobile-responsive grid layout
- Print version should fit on single page with all key data

---

### 2. Real-Time Investment Examples Display

**Purpose:** Show students current prices and performance data for representative investments

**Format:** Data display widget with auto-updating market information

**Inputs:**
- Pre-selected investments (teacher can customize):
  - Example stock: Apple (AAPL), Microsoft (MSFT), or Tesla (TSLA)
  - Example bond fund: Vanguard Total Bond Market (BND or VBTLX)
  - Example stock ETF: Vanguard S&P 500 (VOO) or SPDR S&P 500 (SPY)

**Expected Outputs:**
- For each investment:
  - Current price
  - 1-day change ($ and %)
  - 1-year return (%)
  - Dividend yield or interest rate (%)
  - Expense ratio (for funds)
  - Volume/trading activity

**Interaction Model:**
- Display updates automatically (or has refresh button)
- Students can click each investment for expanded details
- Historical price chart (1 year) displays on click
- Comparison mode shows all three side-by-side

**Design Notes:**
- Use real market data API (Alpha Vantage, Yahoo Finance, or similar)
- Include timestamp showing when data was last updated
- Fallback to static data if API fails or market is closed
- Color-code gains (green) and losses (red) for clarity
- Include disclaimer: "Past performance does not guarantee future results"
- Printable static version captures data at specific time for offline analysis

---

### 3. Fee Impact Calculator (Simple Version)

**Purpose:** Demonstrate how seemingly small fee differences compound to large amounts over time

**Format:** Interactive calculator with visual output

**Inputs:**
- Initial investment amount ($1,000 - $100,000)
- Monthly contribution ($0 - $2,000)
- Annual return percentage (default 8%, adjustable 0-15%)
- Investment time period (1-50 years)
- Fee/expense ratio (0-3%)

**Expected Outputs:**
- Final portfolio value after fees
- Total amount paid in fees over time period
- Comparison: "Fees consumed X% of your potential gains"
- Visual graph showing portfolio growth with and without fees

**Interaction Model:**
- Sliders or input fields for all variables
- Real-time calculation and graph update as values change
- "Compare Two Scenarios" mode: shows low-fee vs. high-fee side-by-side
- Dramatic reveal: "Those fees cost you $X, equivalent to Y years of your contributions"

**Design Notes:**
- Use Formula: FV = P(1 + r)^n + PMT × [((1 + r)^n - 1) / r]
  Where r = (annual return - fee percentage)
- Graph should clearly show the gap between low-fee and high-fee scenarios
- Include tooltip explaining: "Expense ratio is an annual fee expressed as % of investment"
- Highlight the difference amount prominently
- Preset comparison buttons: "0.05% vs. 1.0%" and "0.10% vs. 1.5%" for quick analysis
- Mobile-friendly with touch-optimized sliders
- Printable summary of calculations

---

### 4. Investment Type Learning Module (Definitions and Examples)

**Purpose:** Provide interactive reference for key investment terms and concepts

**Format:** Interactive glossary with expandable definitions and examples

**Inputs:**
- Student selects term to explore

**Expected Outputs:**
- Clear definition
- Real-world example
- Visual representation where applicable
- Related terms/concepts

**Key Terms to Include:**
- Stock, Bond, Mutual Fund, ETF, Dividend, Capital Gains, Interest, Risk Tolerance, Diversification, Liquidity, Expense Ratio, Index Fund, Asset Allocation, Compound Interest

**Interaction Model:**
- Search functionality to find terms quickly
- Click term to expand full definition with example
- "Related Terms" links to navigate between connected concepts
- Quiz mode: Definition provided, student guesses term
- Bookmark favorite terms for quick reference

**Design Notes:**
- Definitions written at high school reading level
- Examples use realistic, relatable scenarios (not abstract)
- Include 1-2 sentence explanation PLUS concrete example for each term
- Visual icons for each investment type
- Audio pronunciation for financial terms
- Printable reference sheet with all terms

---

## Day 2 Assets

### 1. Investment Type Analyzer (Primary Skill Builder)

**Purpose:** Main interactive tool allowing students to explore investment types, compare scenarios, and build sample portfolios

**Format:** Comprehensive multi-section interactive tool

**Section A: Scenario Comparison**

**Inputs:**
- Select scenario type:
  - Conservative (70% bonds, 30% stocks)
  - Moderate (60% stocks, 40% bonds)
  - Growth (90% stocks, 10% bonds)
  - Custom (student defines allocation)
- Monthly investment amount ($50-$500 slider)
- Time horizon (10, 20, or 30 years)

**Expected Outputs:**
- Asset allocation pie chart
- Historical risk level (standard deviation of returns)
- Expected long-term return (based on historical averages)
- Best/worst one-year historical return for that allocation
- Growth projection showing potential future value at different time periods
- Table comparing all scenarios side-by-side

**Section B: Custom Portfolio Builder**

**Inputs:**
- Select 3-5 specific investments from curated list:
  **Stocks:**
  - Individual stocks (e.g., Apple, Microsoft, Amazon) - Higher risk/return
  - S&P 500 Index ETF (VOO, SPY) - Diversified large-cap stocks
  - Total Stock Market ETF (VTI) - Entire U.S. stock market
  - International Stock ETF (VXUS) - Non-U.S. stocks

  **Bonds:**
  - Total Bond Market ETF (BND, AGG) - Diversified bonds
  - Treasury Bond ETF (GOVT) - U.S. government bonds only
  - Corporate Bond ETF (VCIT) - Corporate bonds

  **Balanced:**
  - Target Date Fund (e.g., 2060 target date) - Auto-adjusting mix
  - Balanced Fund (60/40 stock/bond mix) - Fixed moderate allocation

- For each selected investment, choose allocation percentage (must total 100%)

**Expected Outputs:**
- Visual portfolio allocation chart
- Combined expected return and risk based on weighted averages
- Total expense ratio (weighted average of all fees)
- Diversification score (based on number and type of holdings)
- Performance projection over selected time horizon
- Recommendation: "This portfolio is most suitable for [investor type/goal]"

**Section C: Goal-Based Recommendations**

**Inputs:**
- Financial goal type:
  - Retirement (long-term, 20+ years)
  - Home down payment (medium-term, 5-10 years)
  - Major purchase (short-term, 2-5 years)
  - General wealth building (flexible timeline)

- Current age
- Goal timeline
- Risk tolerance (low/moderate/high)

**Expected Outputs:**
- Recommended asset allocation
- Suggested specific funds/ETFs
- Monthly contribution needed to reach goal (if goal amount specified)
- Alternative scenarios: "If you contribute $X more per month, you could reach goal Y years earlier"

**Interaction Model:**
- Tabbed interface for three main sections
- Drag-and-drop for custom portfolio building (alternative: percentage sliders)
- Real-time updates as allocations change
- Save portfolio feature (stores to student profile)
- Compare multiple portfolios side-by-side
- Print portfolio summary with all details

**Design Notes:**
- Use real historical return data for calculations (stocks: ~10%, bonds: ~5%, adjust weighted average for allocations)
- Risk displayed as standard deviation and/or min-max range
- Expense ratios based on actual fund fees (update annually)
- Disclaimer: "Projections based on historical averages; actual returns will vary"
- Mobile-responsive with touch-optimized controls
- Accessibility: keyboard navigation, screen reader support
- Loading states for calculations
- Clear visual feedback when allocations don't total 100%
- Tooltips explaining every metric

---

### 2. Stock vs. Bond Performance Simulator

**Purpose:** Help students understand how different investments perform under various economic conditions

**Format:** Interactive scenario-based simulation tool

**Inputs:**
- Select economic scenario:
  - Strong Economic Growth (GDP +4%, low unemployment)
  - Recession (GDP -2%, rising unemployment)
  - High Inflation (CPI +5% annually)
  - Rising Interest Rates (Fed raises rates 2%)

**Expected Outputs:**
For each scenario:
- Typical stock performance (% return range)
- Typical bond performance (% return range)
- Historical example with specific year and actual returns
- Explanation of why each investment type performed that way
- Visual comparison chart

**Historical Comparison Mode:**

**Inputs:**
- Starting amount (default $10,000)
- Time period selection:
  - Last 30 years (1993-2023)
  - Last 20 years (2003-2023)
  - Last 10 years (2013-2023)
- Portfolio allocation:
  - 100% stocks
  - 100% bonds
  - 60/40 balanced
  - 40/60 conservative

**Expected Outputs:**
- Ending value for each allocation
- Total return percentage
- Average annual return
- Best single year
- Worst single year
- Volatility measure (standard deviation)
- Year-by-year growth chart showing all portfolios

**Interaction Model:**
- Two-panel view: Economic scenarios on left, historical comparison on right
- Toggle between views or see both
- Animated chart showing year-by-year performance
- Hover over any year to see returns for that specific year
- Ability to highlight specific market events (2008 crisis, 2020 COVID crash, etc.)

**Design Notes:**
- Use real historical S&P 500 data for stocks
- Use Barclays Aggregate Bond Index or similar for bonds
- Include major market events as annotations on timeline
- Color-code scenarios: green (growth), red (recession), yellow (inflation), blue (rising rates)
- Provide narrative explanations, not just numbers
- Show that past performance doesn't guarantee future results
- Make worst year losses VERY visible to emphasize risk
- Printable scenario comparison summary

---

### 3. Mutual Fund vs. ETF Head-to-Head Comparator

**Purpose:** Help students understand practical differences between similar mutual funds and ETFs

**Format:** Side-by-side comparison tool

**Pre-Loaded Comparisons:**
1. S&P 500 Tracking:
   - Mutual Fund: Fidelity 500 Index (FXAIX)
   - ETF: SPDR S&P 500 (SPY) or Vanguard 500 (VOO)

2. Total Stock Market:
   - Mutual Fund: Vanguard Total Stock Market Index (VTSAX)
   - ETF: Vanguard Total Stock Market (VTI)

3. Total Bond Market:
   - Mutual Fund: Vanguard Total Bond Market Index (VBTLX)
   - ETF: Vanguard Total Bond Market (BND)

**Comparison Factors:**
For each fund:
- Expense ratio (annual fee %)
- Minimum investment amount
- Trading hours (mutual fund: end of day only; ETF: market hours)
- Dividend handling (mutual fund: automatic reinvest; ETF: manual or automatic)
- Tax efficiency rating (ETFs generally more efficient)
- Bid-ask spread (ETFs only)
- Historical returns (should be nearly identical for similar funds)

**Expected Outputs:**
- Side-by-side table showing all factors
- Visual highlighting of key differences
- Summary recommendation: "ETFs are typically better for beginners due to lower fees and no minimums"
- Exception notes: "Mutual funds may be preferable if automatic investing in employer 401k"

**Interaction Model:**
- Select which pair to compare from dropdown
- View side-by-side comparison
- Click factor for detailed explanation
- "Show me the math" button reveals fee impact calculator for that specific comparison

**Design Notes:**
- Update expense ratios and minimums annually (these change)
- Use actual current data from fund websites
- Explain bid-ask spread simply: "Small cost when buying/selling ETF shares, usually pennies"
- Highlight in green the "better" option for each factor (lower fee = green, etc.)
- Include note: "Both can be excellent choices; ETFs offer more flexibility and lower costs"
- Printable comparison chart

---

### 4. Fee Impact Calculator (Advanced Version)

**Purpose:** Calculate precise long-term cost of fees across multiple scenarios

**Format:** Multi-scenario calculator with comparative outputs

**Inputs:**
- Scenario 1 (Low-cost ETF):
  - Initial investment
  - Monthly contribution
  - Years investing
  - Annual return (default 8%)
  - Expense ratio (default 0.03%)

- Scenario 2 (Average mutual fund):
  - Same investment amounts and timeline
  - Expense ratio (default 0.75%)

- Scenario 3 (High-cost active fund):
  - Same investment amounts and timeline
  - Expense ratio (default 1.25%)

**Expected Outputs:**
- Final value for each scenario
- Total fees paid over time period
- Difference between scenarios
- Visual representation: "The fee difference cost you $X, which equals Y months of your contributions"
- Bar chart comparing final values
- Pie chart showing "Your Money vs. Fees" for high-cost scenario

**Advanced Features:**
- Ability to add up to 5 custom scenarios
- Export comparison as PDF
- "What if" analysis: "To match the low-cost fund's final value, you'd need to contribute $X more per month with the high-cost fund"

**Interaction Model:**
- Tabs or columns for each scenario
- Change any value and all outputs update
- Highlight the differences prominently
- "Shocking Facts" callouts: "You lost the equivalent of 8 years of contributions to fees!"

**Design Notes:**
- Formula: Account for compounding fees annually
- Make the fee impact VISCERAL and memorable
- Include real fund examples with actual expense ratios
- Emphasize this is why low-cost index funds recommended
- Auto-save calculations to student profile
- Printable detailed report
- Mobile-optimized with swipeable scenario comparison

---

### 5. Portfolio Scenario Simulator

**Purpose:** Allow students to design portfolios for specific life scenarios and goals

**Format:** Scenario-based portfolio design tool

**Pre-Built Scenarios:**

**Scenario 1: Recent Graduate (Age 24)**
- Goal: Retirement at 65
- Time horizon: 41 years
- Current income: $45,000
- Monthly investable: $200-500
- Risk capacity: High (long timeline)
- Suggested allocation: 85-90% stocks, 10-15% bonds

**Scenario 2: Young Professional (Age 28)**
- Goal: Home down payment ($40,000) in 5 years
- Current savings: $8,000
- Monthly investable: $500
- Risk capacity: Moderate (specific timeline)
- Suggested allocation: 50% stocks, 45% bonds, 5% cash

**Scenario 3: Mid-Career (Age 45)**
- Goal: Retirement at 65
- Time horizon: 20 years
- Monthly investable: $600
- Risk capacity: Moderate (less time for recovery)
- Suggested allocation: 65-70% stocks, 30-35% bonds

**For Each Scenario:**

**Student Tasks:**
1. Review scenario details
2. Propose asset allocation (stocks/bonds/cash %)
3. Select specific investments from provided list
4. Justify allocation based on goal, timeline, and risk factors

**Tool Provides:**
- Scenario details and constraints
- Guided questions: "What is the time horizon? Does this allow for stock volatility?"
- Investment selection menu (stocks, bonds, funds appropriate for scenario)
- Allocation validator (checks if allocation matches risk capacity)
- Projection: Final portfolio value based on allocation and contributions
- Feedback: "This allocation is [too aggressive/appropriate/too conservative] for this scenario because..."

**Expected Outputs:**
- Completed portfolio plan for each scenario
- Projected outcome (will goal be met?)
- Risk assessment
- Teacher feedback section (for assessment)
- Comparison across scenarios showing how allocations differ based on circumstances

**Interaction Model:**
- Wizard-style progression through each scenario
- Cannot proceed until allocation totals 100%
- Drag-and-drop or slider interface for allocation
- Real-time feedback as choices are made
- Save all three scenario portfolios
- Print comprehensive portfolio plan

**Design Notes:**
- Make scenarios RELATABLE (realistic ages, incomes, goals)
- Don't use luxury examples (no "$5 million retirement goal")
- Include diverse names and situations
- Validate allocations but allow some flexibility (70% vs 75% stocks both acceptable)
- Provide explanatory feedback, not just "right/wrong"
- Show consequences: "With this conservative allocation, you'll likely fall $8,000 short of goal"
- Suggest adjustments: "To reach goal with this allocation, increase monthly contribution by $75"
- Accessibility: keyboard navigation, screen reader compatible
- Mobile-responsive

---

### 6. Investment Decision Framework Tool

**Purpose:** Guide students through systematic framework to determine personal investment approach

**Format:** Interactive decision tree / questionnaire

**Section 1: Personal Financial Assessment**

**Questions:**
1. Emergency fund status:
   - [ ] I have 3-6 months expenses saved
   - [ ] I have 1-2 months expenses saved
   - [ ] I have less than 1 month saved
   - [ ] I have no emergency fund

2. Debt situation:
   - [ ] No debt or only low-interest mortgage
   - [ ] Manageable debt with payments under control
   - [ ] High-interest credit card debt
   - [ ] Overwhelming debt situation

3. Primary investment goal:
   - [ ] Long-term retirement (20+ years)
   - [ ] Medium-term goal like home/education (5-15 years)
   - [ ] Short-term goal (2-5 years)
   - [ ] Building general wealth (flexible timeline)

4. Risk tolerance assessment:
   - If your $5,000 investment dropped to $3,500, you would:
     - [ ] Stay invested and keep contributing (high tolerance)
     - [ ] Feel nervous but probably hold (moderate tolerance)
     - [ ] Likely sell to prevent further loss (low tolerance)

**Section 2: Recommended Strategy**

**Based on responses, provide:**
- Priority action: "Build emergency fund first" OR "Ready to invest"
- Recommended asset allocation
- Suggested investment types
- Specific fund recommendations
- Monthly contribution suggestion based on goals
- Timeline: When to reassess allocation

**Section 3: Action Plan**

**Tool generates personalized checklist:**
- [ ] Open investment account at [recommended brokerage]
- [ ] Set up automatic monthly contribution of $[amount]
- [ ] Invest in [specific fund/ETF recommendations]
- [ ] Review portfolio every [6/12] months
- [ ] Rebalance when allocation drifts more than [5/10]%
- [ ] Reassess strategy when [life change occurs]

**Expected Outputs:**
- Personalized investment recommendation
- Written justification based on student's inputs
- Printable action plan
- Resource links (how to open account, etc.)
- Reminder: "This is a starting point; adjust as you learn and circumstances change"

**Interaction Model:**
- Wizard-style progression through questions
- Can go back and change answers
- Results update in real-time as answers change
- Save assessment and recommendations to student profile
- Option to email action plan to self
- Comparison tool: "How would recommendation change if time horizon was 30 years instead of 10?"

**Design Notes:**
- Non-judgmental tone (no "good" or "bad" labels for answers)
- Emphasize that all starting points are valid
- If emergency fund lacking, don't shame—provide resources and encouragement
- Action plan should be SPECIFIC and ACTIONABLE, not vague
- Include actual brokerage names (Vanguard, Fidelity, Schwab) and account types (Roth IRA, taxable brokerage, etc.)
- Links to open accounts (affiliate-free, educational purpose)
- Privacy note: Answers not shared, stored locally or in student profile only
- Printable personal investment plan suitable for student portfolio

---

## Skill Builder Assets (Cross-Reference)

The **Investment Type Analyzer** (Asset 1 in Day 2 section) serves as the primary skill builder introduced in Day 1 and used extensively in Day 2. It integrates:
- Scenario comparison
- Custom portfolio building
- Goal-based recommendations

See detailed specifications in Day 2 Assets, Section 1 above.

---

## Downloadable Resources

All interactive tools must have printable alternatives for accessibility and technology equity.

### Printable PDFs

**1. Investment Characteristics Comparison Chart**
- Static table comparing stocks, bonds, mutual funds, ETFs across key factors
- 1-page reference suitable for printing and annotation
- Includes space for student notes

**2. Portfolio Planning Worksheet**
- Template for designing portfolios for different scenarios
- Includes sections for: Goal, Time Horizon, Risk Tolerance, Asset Allocation, Specific Investments, Rationale
- 2-page worksheet with 3 scenario templates

**3. Fee Impact Calculation Worksheet**
- Step-by-step guide to calculating fee impact manually
- Includes formulas and worked example
- Space for students to calculate 2-3 scenarios by hand
- 1-page reference

**4. Investment Decision Checklist**
- Printable version of decision framework
- Flowchart format: "Do you have emergency fund? → If yes, proceed. If no, build that first."
- Ends with personalized allocation recommendation based on decision path
- 2-page flowchart and action plan template

**5. Investment Type Reference Guide**
- Glossary of key terms with definitions and examples
- Includes icons and visual representations
- 4-page comprehensive reference suitable for student binders
- Organized by category: Investment Types, Key Concepts, Performance Metrics, Fees & Costs

**6. Real-World Investment Examples Sheet**
- Static data snapshot showing:
  - Sample stocks with prices, returns, dividends
  - Sample bond funds with yields and expense ratios
  - Sample ETFs with allocations and fees
- Updated quarterly with current data
- 2-page reference with analysis questions

**7. Scenario-Based Portfolio Solutions Guide** (Teacher Resource)
- Shows exemplar student responses for three scenarios
- Includes reasoning and justification
- Useful for teacher assessment and student self-check
- 3-page guide with rubric

**8. Investment Action Plan Template**
- Fillable PDF students can complete digitally or by hand
- Sections: Current situation, Goals, Recommended allocation, Specific investments, Timeline, Next steps
- 1-page professional-looking plan students can actually use

---

## Technical Requirements

### Data Requirements

**Real-Time Financial Data:**
- Stock prices and performance (Alpha Vantage, Yahoo Finance, IEX Cloud APIs)
- Fund/ETF expense ratios (updated quarterly from fund websites)
- Historical index returns (S&P 500, Bond Index data)
- Economic indicators for scenarios (Fed data for interest rates, BLS for inflation)

**Update Frequency:**
- Stock/ETF prices: Daily (or real-time during market hours)
- Expense ratios: Quarterly review
- Historical return data: Annual update
- Economic scenario data: Annual review

### Calculation Accuracy

**Required Formulas:**

**Future Value with Regular Contributions:**
```
FV = P(1 + r)^n + PMT × [((1 + r)^n - 1) / r]
Where:
P = initial principal
r = annual rate of return
n = number of years
PMT = monthly payment (multiply by 12 for annual)
```

**Fee Impact Calculation:**
```
FV_net = P(1 + (r - fee))^n + PMT × [((1 + (r - fee))^n - 1) / (r - fee)]
Where:
fee = expense ratio (as decimal, e.g., 0.01 for 1%)
Difference = FV_gross - FV_net
```

**Standard Deviation (Risk/Volatility):**
```
σ = √[Σ(x - μ)² / N]
Based on historical annual returns
```

**Weighted Average (Portfolio Returns/Fees):**
```
Portfolio Return = (Stock% × Stock Return) + (Bond% × Bond Return)
Portfolio Fee = (Fund1% × Fund1 Fee) + (Fund2% × Fund2 Fee)...
```

### User Experience Requirements

**Performance:**
- Calculations complete within 1 second
- Page/tool loads within 3 seconds
- Real-time updates as inputs change (debounced for performance)

**Accessibility:**
- WCAG 2.1 AA compliant
- Keyboard navigation for all tools
- Screen reader compatible with proper ARIA labels
- Color-blind friendly color schemes
- Text resizable without breaking layout
- High contrast mode option

**Mobile Responsiveness:**
- All tools functional on tablets and phones
- Touch-optimized controls (sliders, buttons)
- Readable text on small screens
- Stacked layouts for narrow screens
- No horizontal scrolling required

**Browser Compatibility:**
- Modern browsers: Chrome, Firefox, Safari, Edge (current and 1 version back)
- Graceful degradation for older browsers
- Fallback to static content if JavaScript fails

**Data Privacy:**
- No personal financial data collected
- Student inputs saved only to their account (not shared)
- Clear privacy notice on tools
- Option to work anonymously without saving

---

## Design Consistency

**Visual Theme:**
- Consistent color scheme:
  - Stocks: Blue (#2563EB)
  - Bonds: Green (#059669)
  - Mutual Funds: Orange (#EA580C)
  - ETFs: Purple (#9333EA)
  - Growth/Positive: Green (#10B981)
  - Loss/Negative: Red (#EF4444)
  - Neutral/Info: Gray (#6B7280)

**Typography:**
- Headings: Clear, bold, sans-serif
- Body: Readable, 16px minimum
- Numbers/Data: Monospace for clarity and alignment

**Icons:**
- Stocks: Line chart going up
- Bonds: Certificate or document icon
- Funds: Basket or collection icon
- Fees: Money with downward arrow
- Risk: Warning triangle or volatility graph
- Time: Clock or calendar

**Charts:**
- Line charts for performance over time
- Bar charts for comparisons between options
- Pie charts for portfolio allocations
- Area charts for growth projections

**Interaction Patterns:**
- Sliders for continuous values (amounts, years, percentages)
- Dropdown menus for categorical choices (scenarios, funds)
- Radio buttons for mutually exclusive options
- Checkboxes for multiple selections
- Drag-and-drop for portfolio building (with numeric input alternative)

---

## Development Priorities

**Phase 1 (Minimum Viable):**
1. Investment Type Analyzer (primary skill builder)
2. Fee Impact Calculator (both versions)
3. Portfolio Scenario Simulator
4. Printable resources

**Phase 2 (Enhanced Features):**
5. Stock vs. Bond Performance Simulator
6. Mutual Fund vs. ETF Comparator
7. Investment Decision Framework Tool
8. Real-time data integration

**Phase 3 (Advanced Features):**
9. Save/export functionality
10. Personalized recommendations
11. Progress tracking across multiple sessions
12. Integration with student portfolios

---

## Quality Assurance

**Testing Requirements:**

**Calculation Verification:**
- All formulas verified against financial calculators
- Edge cases tested (zero contributions, 50-year timelines, negative returns)
- Rounding handled consistently (to 2 decimal places for currency)

**User Testing:**
- Test with actual students before full deployment
- Gather feedback on clarity and usability
- Iterate based on confusion points

**Content Accuracy:**
- Financial data verified against authoritative sources
- Expense ratios confirmed from fund prospectuses
- Historical returns matched to verified index data
- Annual review and update of all static content

**Accessibility Testing:**
- Screen reader testing with JAWS/NVDA
- Keyboard-only navigation testing
- Color contrast verification
- Mobile device testing on iOS and Android

---

**End of Assets Specification**

*These tools are designed to make investment concepts tangible, accessible, and immediately applicable to students' financial futures. Development should prioritize educational clarity and user experience over feature complexity.*

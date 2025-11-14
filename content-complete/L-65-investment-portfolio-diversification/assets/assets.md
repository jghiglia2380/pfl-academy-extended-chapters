# L-65 Assets: Investment Portfolio Diversification

This document specifies all interactive tools, downloadable resources, and assets needed for L-65. Each asset includes detailed specifications for the development team.

---

## Day 1 Assets

### 1. Portfolio Diversification Builder (PRIMARY SKILL BUILDER)

**Purpose:** Allow students to construct diversified investment portfolios, visualize correlation effects, and see how different allocations perform through historical market conditions including crashes and bull markets.

**Format:** Interactive web-based portfolio construction tool with simulation engine

**Inputs:**
- **Investor Profile Selection:**
  - Age (dropdown: 20-30, 30-45, 45-60, 60-70, 70+)
  - Monthly contribution amount ($0-$2,000)
  - Investment time horizon (years until need money: 5-50 years)
  - Risk tolerance (slider: conservative - moderate - aggressive)
- **Asset Allocation Builder:**
  - US Large-Cap Stocks (percentage slider 0-100%)
  - US Small-Cap Stocks (percentage slider 0-50%)
  - International Developed Markets (percentage slider 0-40%)
  - Emerging Markets (percentage slider 0-30%)
  - US Government Bonds (percentage slider 0-80%)
  - Corporate Bonds (percentage slider 0-40%)
  - Real Estate (REITs) (percentage slider 0-30%)
  - Gold (percentage slider 0-15%)
  - Cash/Money Market (percentage slider 0-30%)
  - **Total must equal 100%** - tool shows running total and locks allocation when it reaches 100%
- **Simulation Settings:**
  - Time period: 10, 20, 30, or 40 years
  - Include market crashes: Yes/No toggle
  - Rebalancing frequency: None, Annual, Quarterly, or Threshold-based (5% drift)
  - Starting portfolio value (default $10,000 or customizable)
  - Monthly contributions (linked to profile or custom)

**Expected Outputs:**
- **Portfolio Visualization:**
  - Pie chart showing current allocation across all asset classes
  - Color-coded segments with percentages
  - Asset class labels with dollar amounts
- **Risk Metrics:**
  - **Expected Annual Return:** Based on historical data for selected allocation (e.g., "7.8% average")
  - **Volatility (Standard Deviation):** Annual return variability (e.g., "12.3%")
  - **Maximum Drawdown:** Largest peak-to-valley loss expected (e.g., "-28%")
  - **Recovery Time:** Estimated months to recover from max drawdown (e.g., "18 months")
- **Historical Simulation Results:**
  - Line graph showing portfolio value growth over selected time period
  - Multiple lines comparing: Your Portfolio, 100% Stocks, 60/40 Stock/Bond, Target-Date Fund equivalent
  - Shaded regions indicating recession/crisis periods
  - Annotations showing major market events (2008 crash, 2020 pandemic, bull markets)
- **Performance Summary Table:**
  - Final portfolio value
  - Total contributions made
  - Total growth (final value minus contributions)
  - Annualized return (CAGR - Compound Annual Growth Rate)
  - Best year return
  - Worst year return
  - Number of negative years
  - Sharpe Ratio (risk-adjusted return measure)
- **Comparison Metrics:**
  - How your portfolio compares to benchmark allocations
  - Efficiency score (return per unit of risk)
  - Diversification score (0-100 based on asset spread and correlation)
- **Rebalancing Impact:**
  - If rebalancing selected, shows trades executed and their impact
  - Comparison: portfolio with rebalancing vs. without
  - Dollar impact of rebalancing discipline
- **Scenario Analysis:**
  - "What if" buttons: "What if 2008 crash repeated?", "What if inflation surge?", "What if prolonged bull market?"
  - Shows how portfolio would perform under each scenario
- **Downloadable Report:**
  - PDF summary with charts, metrics, and recommendations
  - Includes allocation pie chart, performance graph, and key statistics

**Interaction Model:**
1. Student selects investor profile (age, contributions, time horizon, risk tolerance)
2. Tool suggests "Recommended Allocation" based on profile
3. Student can accept recommendation or customize allocation using sliders
4. As student adjusts sliders, pie chart updates in real-time
5. Tool shows risk metrics dynamically ("If you increase stocks to 85%, max drawdown increases to -32%")
6. Student runs simulation with selected time period and settings
7. Tool processes simulation (showing progress bar for longer periods)
8. Results display with interactive charts (hover over graph to see specific year values)
9. Student can modify allocation and re-run to compare outcomes
10. Tool allows saving multiple portfolios for side-by-side comparison
11. "Optimize" feature suggests allocation adjustments to improve risk-adjusted returns
12. Export/download feature creates PDF report

**Design Notes:**
- Use intuitive slider controls with immediate visual feedback
- Color-code asset classes consistently (stocks = shades of blue, bonds = green, real estate = orange, gold = yellow, cash = gray)
- Show "allocation remaining" counter prominently (e.g., "65% allocated, 35% remaining")
- Prevent allocations that exceed 100% (sliders lock or redistribute)
- Provide tooltips explaining each asset class and metric
- Include "Help" overlays with definitions and guidance
- Use responsive charts that work on desktop and tablet
- Implement "undo" functionality to revert allocation changes
- Provide preset allocations: "Conservative," "Moderate," "Aggressive," "Target-Date 2050"
- Simulation should complete within 5 seconds for good user experience
- Mobile-friendly design with touch-optimized sliders
- Accessibility: keyboard navigation, screen reader labels, high-contrast mode
- Estimated development time: 25-30 hours for full implementation

---

## Day 2 Assets

### 2. Correlation Matrix Analyzer

**Purpose:** Help students understand correlation relationships between asset classes and identify combinations that provide diversification benefits

**Format:** Interactive correlation matrix with portfolio testing functionality

**Inputs:**
- **Asset Class Selection:** Students can select/deselect asset classes to include in analysis:
  - US Large-Cap Stocks
  - US Small-Cap Stocks
  - International Developed Markets
  - Emerging Markets
  - US Government Bonds
  - Corporate Bonds
  - Real Estate (REITs)
  - Gold
  - Commodities (broad basket)
  - Cash
- **Time Period:** Choose historical period for correlation calculation:
  - Last 10 years
  - Last 20 years
  - Last 30 years
  - Since 1970 (longest available data)
  - Custom date range
- **Portfolio Testing:** Build up to 5 test portfolios with different allocations
- **Market Condition Filter:** Show correlations during specific periods:
  - All periods (default)
  - Bull markets only
  - Bear markets/recessions only
  - High inflation periods
  - Low interest rate periods

**Expected Outputs:**
- **Correlation Matrix Display:**
  - Grid showing correlation coefficient for every asset pair
  - Color-coded cells: Dark red (-1.0 to -0.5), Light red (-0.5 to -0.2), White (-0.2 to +0.2), Light blue (+0.2 to +0.5), Dark blue (+0.5 to +1.0)
  - Hover over any cell shows: Correlation value, interpretation ("Low positive correlation"), scatter plot of the two assets' returns
- **Interpretation Guide:**
  - Key explaining correlation ranges and what they mean
  - "Pairs with correlation below +0.3 provide good diversification"
  - "Pairs near zero or negative provide excellent diversification"
- **Highlighted Insights:**
  - Automatically identifies and highlights:
    - Best diversification pairs (lowest/most negative correlation)
    - Worst diversification pairs (highest positive correlation)
    - Surprising relationships (e.g., "Gold and stocks have near-zero correlation")
- **Portfolio Comparison Tool:**
  - Student builds Portfolio A (up to 10 asset classes with percentages)
  - Student builds Portfolio B (different allocation)
  - Tool calculates and compares:
    - Weighted average correlation of Portfolio A
    - Weighted average correlation of Portfolio B
    - Diversification score (0-100, higher = better diversified)
    - Historical volatility of each portfolio
    - Maximum drawdown of each portfolio
- **Historical Performance Visualization:**
  - Graph showing how selected asset classes performed over chosen time period
  - Toggle on/off different assets to see their individual paths
  - Shaded regions for recessions/crises
  - Annotations: "Notice: During 2008 crisis, stocks fell -37% while government bonds rose +5%"

**Interaction Model:**
1. Student views default correlation matrix for 9 major asset classes
2. Matrix displays with color coding making patterns immediately visible
3. Student hovers over cells to see details and scatter plots
4. Student can change time period to see how correlations shift
5. Student filters to "Bear markets only" to see crisis correlations
6. Student builds test Portfolio A (e.g., 100% US stocks)
7. Student builds test Portfolio B (e.g., 60% stocks, 40% bonds)
8. Tool calculates diversification scores and shows which is better diversified
9. Historical performance graph shows how each portfolio would have performed
10. Student iterates, testing different combinations to optimize diversification
11. Export feature creates correlation matrix image and portfolio comparison summary

**Design Notes:**
- Matrix should be easily scannable—clear visual hierarchy
- Use color blind-friendly palette (not just red/green)
- Provide scatter plots on hover for visual learners
- Include educational popups explaining correlation concepts
- Allow students to save/bookmark interesting asset pairs
- Provide "Challenge Mode": "Find an allocation with diversification score >80"
- Show real-time feedback: "Adding 20% bonds increased your diversification score from 45 to 72!"
- Estimated development time: 12-15 hours

### 3. Asset Allocation Optimizer

**Purpose:** Guide students in designing age-appropriate asset allocations and understanding risk-time horizon relationships

**Format:** Interactive allocation design tool with recommendation engine

**Inputs:**
- **Investor Profile Data:**
  - Current age (slider or input: 18-80)
  - Retirement target age (slider or input: 55-75)
  - Current savings/portfolio value ($0-$500,000)
  - Monthly contribution amount ($0-$2,000)
  - Other assets (home equity, inheritance expected, pension): Yes/No toggles
  - Risk tolerance quiz (5 questions):
    - "If your portfolio dropped 25% tomorrow, would you: A) Panic sell, B) Hold steady, C) Buy more?"
    - "I prefer investments that: A) Protect my money, even with low returns, B) Balance growth and safety, C) Maximize growth potential"
    - "I lose sleep if my portfolio drops: A) 10%, B) 20%, C) 30%+"
    - "My investing knowledge is: A) Beginner, B) Intermediate, C) Advanced"
    - "I have emergency savings to cover 6+ months expenses: A) No, B) Partially, C) Yes"
  - Financial goals: Retirement only, Home down payment, Other major purchase
- **Constraint Inputs (Optional):**
  - Maximum acceptable loss percentage
  - Minimum return needed to reach goal
  - Cannot invest in certain assets (religious/ethical restrictions)

**Expected Outputs:**
- **Risk Profile Assessment:**
  - Based on quiz and data, classifies investor as: Very Conservative, Conservative, Moderate, Moderately Aggressive, Aggressive
  - Explanation: "Based on your responses, you have moderate risk tolerance with 22 years to retirement"
- **Recommended Allocation:**
  - Personalized allocation with specific percentages:
    - "Recommended: 68% Stocks, 28% Bonds, 4% Real Estate"
    - Breakdown: "Stocks: 45% US Large-Cap, 15% US Small-Cap, 8% International"
    - Rationale for each recommendation
  - Visual pie chart of recommended allocation
  - Comparison to standard age-based allocation ("120 minus age" rule)
- **Allocation Comparison Tools:**
  - Shows 3-5 preset allocations for comparison:
    - "Target-Date 2050 Fund" allocation
    - "Age-appropriate" (using 120-age formula)
    - "Conservative" (for this age)
    - "Aggressive" (for this age)
    - "Your Custom" (if student modifies recommendation)
- **For Each Allocation, Tool Projects:**
  - Expected portfolio value at retirement age
  - Probability of reaching stated financial goal (if provided)
  - Maximum likely loss during worst market crash
  - Best year, worst year, average year returns
  - **Confidence bands:** "There's an 80% chance your portfolio will be between $1.2M and $2.4M at age 67"
- **Sensitivity Analysis:**
  - "What if" scenarios:
    - "What if you increased monthly contribution by $100?"
    - "What if you used more conservative allocation?"
    - "What if market returns are lower than historical average?"
  - Shows impact on retirement outcome
- **Goal Achievement Meter:**
  - Visual gauge showing likelihood of reaching financial goal with current plan
  - Red (0-40%): "Current plan unlikely to reach goal"
  - Yellow (40-70%): "Moderate chance of reaching goal"
  - Green (70-100%): "Strong likelihood of reaching goal"
  - Suggestions to improve: "Increase monthly contribution" or "Extend retirement age 2 years"

**Interaction Model:**
1. Student enters investor profile data (age, retirement target, savings, contributions)
2. Student completes risk tolerance quiz (5 questions, multiple choice)
3. Tool analyzes and provides risk profile classification
4. Tool generates recommended allocation with rationale
5. Student sees projected retirement outcomes (value, probability of goal)
6. Student can accept recommendation or customize allocation
7. If customizing, tool provides real-time feedback: "Increasing bonds to 40% reduces expected value by $120,000 but cuts max drawdown from -28% to -18%"
8. Student compares multiple allocation options side-by-side
9. Student tests "what if" scenarios (more contributions, different allocations, varying time horizons)
10. Student finalizes allocation and receives comprehensive report
11. Export feature creates detailed allocation plan with implementation steps

**Design Notes:**
- Risk quiz should feel engaging, not like a test
- Use clear, jargon-free language in questions
- Provide "Why we ask this" explanations for each quiz question
- Visual feedback for projections (line graphs with confidence bands, not just numbers)
- Goal achievement meter should be prominent and motivating
- Implement "smart defaults" that adjust based on inputs
- Include educational sidebars: "Why time horizon matters," "Understanding risk tolerance"
- Allow saving multiple scenarios to compare later
- Provide printable allocation plan
- Estimated development time: 15-18 hours

### 4. Rebalancing Simulator

**Purpose:** Provide hands-on practice making rebalancing decisions over a multi-year period, demonstrating discipline and "buy low/sell high" mechanics

**Format:** Interactive year-by-year decision simulator with parallel universe comparisons

**Inputs:**
- **Starting Portfolio Setup:**
  - Initial value (default $100,000 or custom $10,000-$500,000)
  - Target allocation (percentage sliders for stocks vs. bonds, or full multi-asset)
  - Rebalancing threshold (tolerance for drift before rebalancing): 3%, 5%, 10%, or "Always at year-end"
  - Monthly contribution amount ($0-$2,000)
- **Decision Preferences:**
  - **Manual Mode:** Student decides each year whether to rebalance
  - **Automatic Mode:** Student sets rules, tool executes automatically
  - **Learn Mode:** Tool provides guidance/hints for each decision
- **Market Scenario:**
  - **Historical:** Use actual historical returns from selected period (1990s, 2000s, 2010s, 2000-2020 including two crashes)
  - **Simulated:** Randomized returns within historical parameters
  - **Custom:** User defines specific bull/bear sequences

**Expected Outputs:**
- **Year-by-Year Dashboard:**
  - Current year displayed prominently
  - Starting values for year: Stock value, Bond value, Total value
  - Annual returns: "Stocks returned +18%, Bonds returned +4%"
  - Ending values before rebalancing
  - Current allocation percentage vs. target
  - Drift amount: "6% over target on stocks"
  - Visual allocation pie chart showing current vs. target (overlay comparison)
- **Rebalancing Decision Interface:**
  - Clear prompt: "Your allocation is now 76% stocks / 24% bonds (target: 70% / 30%). Rebalance?"
  - Options: [Rebalance Now] [Do Nothing] [Get Recommendation]
  - If "Get Recommendation": Tool explains pros/cons:
    - "Pro: Restore target allocation, lock in stock gains"
    - "Con: Transaction costs (minimal in this simulation), potential taxes in taxable account"
    - "Recommendation: Yes, drift exceeds your 5% threshold"
- **Trade Execution Screen** (if rebalancing):
  - Shows exact trades needed:
    - "Sell $6,450 of stock index fund"
    - "Buy $6,450 of bond index fund"
  - New allocation after trades: "70.0% stocks / 30.0% bonds"
  - Running transaction cost (for realism, though small)
- **Parallel Universe Tracker:**
  - Three columns showing three strategies simultaneously:
    - **Your Decisions:** Based on student's choices
    - **Always Rebalance:** Automatic annual rebalancing
    - **Never Rebalance:** Let portfolio drift without any rebalancing
  - Each shows: Current value, Current allocation, Cumulative returns
  - Color-coded performance: Green (best performing), Yellow (middle), Red (worst)
- **End-of-Simulation Summary (After 10 years):**
  - Final portfolio values for all three strategies
  - Total returns (dollar amount and percentage)
  - Annualized returns (CAGR)
  - Maximum drawdown experienced by each strategy
  - Allocation drift in "Never Rebalance" scenario
  - Risk metrics: Volatility, Sharpe Ratio for each
  - **Key Insight Box:**
    - "Rebalancing improved returns by X%" or "Rebalancing reduced max drawdown by Y%"
    - "Never rebalancing resulted in 89% stocks allocation (target was 70%)—much riskier than intended!"
- **Decision Replay:**
  - Timeline showing all rebalancing decisions made
  - Ability to "go back" and change a specific year's decision to see alternate outcome
  - "What if you had rebalanced in Year 5 instead of holding?" comparison

**Interaction Model:**
1. Student sets up starting portfolio ($100,000, 70/30 stocks/bonds target)
2. Simulation begins at Year 1
3. Tool shows market returns for the year and new allocation
4. Student decides: Rebalance or Hold
5. Tool executes decision and shows impact
6. Simulation advances to Year 2
7. Process repeats for 10 years
8. Student can see parallel universe outcomes updating each year
9. After Year 10, comprehensive comparison of three strategies
10. Student can replay simulation with different starting allocation or decision strategy
11. "Challenge Mode": "Can you beat the Always Rebalance strategy?"
12. Export feature creates timeline of decisions with outcomes

**Design Notes:**
- Year-by-year progression should feel like game levels (progress bar showing "Year 5 of 10")
- Parallel universe comparison should be visible throughout, not just at end
- Use clear visual indicators for allocation drift (red zone = needs rebalancing)
- Provide "Fast Forward" option for students who want to skip to final results
- Include "Rewind" feature to change past decisions and see alternate timeline
- Decision interface should clearly show WHY rebalancing is recommended
- Celebrate good decisions: "Great choice! Rebalancing after that surge locked in gains."
- Provide teachable moments: "Stocks just crashed 30%. This is when rebalancing feels hardest—buying what fell."
- Historical scenario mode should include annotations about real events: "2008 Financial Crisis," "2020 Pandemic"
- Estimated development time: 18-20 hours

---

## Downloadable Resources (Printable PDFs)

### PDF 1: Correlation Reference Matrix

**Purpose:** Printable correlation matrix for students without technology access

**Format:** 2-page PDF

**Contents:**
- Full correlation matrix for 9 major asset classes
- Color-coded cells (grayscale-friendly for printing)
- Explanation key for correlation values
- Highlighted asset pairs with best diversification potential
- Historical notes: "During 2008 crisis, stocks and bonds had -0.4 correlation"

### PDF 2: Age-Based Allocation Guide

**Purpose:** Reference guide showing recommended allocations by age

**Format:** 2-page PDF chart

**Contents:**
- Table showing allocations for ages 20, 30, 40, 50, 60, 70
- Each row: Age, Years to retirement, Stock %, Bond %, Other %, Example dollar allocation
- Visual pie charts for each age group
- "120 minus age" formula with examples
- Explanations for why allocations change with age

### PDF 3: Rebalancing Decision Worksheet

**Purpose:** Printable worksheet for practicing rebalancing calculations

**Format:** 3-page PDF worksheet

**Contents:**
- Three scenarios with starting portfolios
- Market return data for each asset class
- Blank spaces for calculating new values
- Spaces for determining if rebalancing is needed
- Trade calculation worksheets
- Answer key on final page

### PDF 4: Portfolio Diversification Planning Template

**Purpose:** Students can design and document their portfolio strategy

**Format:** 3-page PDF template

**Contents:**
- Personal profile section (age, risk tolerance, goals)
- Target allocation planner (percentage inputs for each asset class)
- Pie chart template to color in allocation visually
- Rebalancing commitment (frequency, threshold)
- Review schedule (when to reassess allocation)
- Notes section for strategy adjustments

### PDF 5: Diversification Quick Reference Card

**Purpose:** One-page summary of key concepts

**Format:** 1-page front/back PDF (card size)

**Contents:**
- Front:
  - Correlation scale (-1.0 to +1.0) with explanations
  - Key asset classes and typical correlations
  - "120 minus age" allocation rule
  - Rebalancing frequency recommendations
- Back:
  - Benefits of diversification (bullet points)
  - Common mistakes to avoid
  - Emergency checklist: "Before you panic sell..."
  - Resources for further learning

---

## Accessibility Requirements

All digital tools must meet:
- WCAG 2.1 AA standards
- Screen reader compatibility (all charts must have text descriptions)
- Keyboard navigation for all interactive elements
- Color blind-friendly palettes (don't rely solely on color)
- Text resize up to 200% without breaking layouts
- High-contrast mode option
- Alternative text for all images, charts, and icons
- Printable PDF alternatives for students without reliable technology

---

## Technical Specifications

**Platform Compatibility:**
- Web-based (HTML5, CSS3, JavaScript)
- Modern browsers: Chrome, Firefox, Safari, Edge
- Mobile-responsive (works on tablets, minimum)
- No plugins required

**Data & Performance:**
- Portfolio simulations complete within 5 seconds
- Support 30+ concurrent users without degradation
- Local storage for saving portfolios/progress
- Optional account sync for saving across devices
- FERPA/COPPA compliant data handling

**Integration:**
- LMS embeddable (Canvas, Schoology, Google Classroom)
- Single sign-on compatible
- Gradebook integration for completion tracking
- Export features (PDF, CSV for data)

---

## Development Priority

**Phase 1 (MVP):**
1. Portfolio Diversification Builder (primary skill builder)
2. Asset Allocation Optimizer (high educational value)
3. Printable PDFs (accessibility requirement)

**Phase 2:**
4. Correlation Matrix Analyzer (shorter dev time, good value)
5. Rebalancing Simulator (complex but high engagement)

**Estimated Total Development Time:** 70-85 hours for all digital assets

---

This comprehensive asset specification provides the development team with all information needed to build interactive tools and resources for L-65.

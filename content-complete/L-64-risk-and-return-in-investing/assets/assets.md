# Asset Specifications for L-64: Risk and Return in Investing

## Day 1 Assets

### 1. Risk-Return Scatterplot Visualization
- **Purpose:** Visual representation of the risk-return tradeoff across different asset classes
- **Format/Inputs:** Interactive SVG chart with hover functionality
- **Expected Outputs:** Clear visual understanding that higher returns correlate with higher risk
- **Interaction Model:**
  - Static display showing six investment types plotted on risk (x-axis) vs. return (y-axis) coordinates
  - Hover over each point to see detailed information (asset name, average return, standard deviation)
  - Color-coded by risk level: Green (low risk), Yellow (moderate), Orange (moderate-high), Red (high)
  - Diagonal "frontier" line showing efficient risk-return combinations
- **Design Notes:**
  - **X-Axis:** Risk (Standard Deviation) from 0% to 40%
  - **Y-Axis:** Expected Return from 0% to 16%
  - **Plotted Points:**
    - Savings Account: (0.5%, 2%) - Green
    - Treasury Bonds: (3%, 3.5%) - Green
    - Corporate Bonds: (5%, 4.5%) - Yellow
    - Balanced Fund: (10%, 7%) - Yellow
    - Large-Cap Stocks: (18%, 10%) - Orange
    - Small-Cap/Emerging Markets: (30%, 13%) - Red
  - Include gridlines for easy reading
  - Add annotation: "The Risk-Return Tradeoff: Higher returns require accepting higher risk"
  - Responsive design for mobile viewing
  - Accessibility: Screen reader describes each point's coordinates and meaning

### 2. Historical Market Returns Chart (1990-Present)
- **Purpose:** Show actual stock market volatility over 30+ years with context of major events
- **Format/Inputs:** Interactive line chart with annotations
- **Expected Outputs:** Understanding that markets are volatile short-term but positive long-term
- **Interaction Model:**
  - Line graph showing S&P 500 annual returns from 1990 to present
  - Hover over any year to see exact return percentage
  - Toggle between "Absolute Values" ($10,000 investment growth) and "Annual Returns" (yearly percentages)
  - Click on notable events to read context (dot-com crash, financial crisis, pandemic)
  - Zoom function to examine specific time periods in detail
- **Design Notes:**
  - **X-Axis:** Years (1990-2025)
  - **Y-Axis (Primary View):** Annual Return Percentage (-40% to +40%)
  - **Y-Axis (Alternative View):** Portfolio Value ($0 to $250,000 for initial $10,000)
  - Color coding: Green for positive years, Red for negative years
  - Annotated events:
    - 2000-2002: Dot-com bubble burst (-37% over 3 years)
    - 2008: Financial crisis (-37% in one year)
    - 2020: Pandemic crash (-34% in March) then rapid recovery
    - 2022: Inflation/rate shock (-18%)
  - Show average return line (~10%) across entire period
  - Include calculation: $10,000 invested in 1990 → $__ in 2025
  - Mobile-responsive with simplified annotations for small screens
  - Printable version available as static PDF

### 3. Diversification Visual Demonstration
- **Purpose:** Illustrate how diversification reduces unsystematic risk
- **Format/Inputs:** Animated visual showing risk reduction with more holdings
- **Expected Outputs:** Understanding that diversification eliminates company-specific risk but not market risk
- **Interaction Model:**
  - Interactive slider: Move from 1 stock to 50 stocks in portfolio
  - Chart shows total portfolio risk (standard deviation) decreasing as holdings increase
  - At 1 stock: High risk (both systematic + unsystematic)
  - At 20-30 stocks: Risk plateaus (only systematic risk remains)
  - Visual representation using circles or bars showing risk decomposition
- **Design Notes:**
  - **Display Elements:**
    - Portfolio Risk Meter: Visual gauge showing total risk level
    - Risk Breakdown Bars:
      - Blue bar: Systematic Risk (market-wide, unavoidable) - stays constant
      - Orange bar: Unsystematic Risk (company-specific) - shrinks with more holdings
    - Total Risk Line: Decreases from ~40% (1 stock) to ~18% (30+ stocks)
  - Interactive features:
    - Drag slider to change number of holdings
    - Click example scenarios: "1 tech stock", "10 diverse stocks", "S&P 500 index (500 stocks)"
    - Animate the transition showing risk reduction
  - Educational callouts:
    - "Adding stocks 1-10: Big risk reduction"
    - "Adding stocks 10-30: Moderate reduction"
    - "Adding stocks 30+: Minimal additional benefit"
  - Include real-world example: Compare Marcus's one-stock portfolio disaster vs. diversified portfolio
  - Accessibility: Text descriptions of risk levels at different diversification points

### 4. Beta Comparison Visualization
- **Purpose:** Show how different investments move relative to the market
- **Format/Inputs:** Comparative line chart showing market vs. different beta investments
- **Expected Outputs:** Understanding beta as measure of market sensitivity
- **Interaction Model:**
  - Base line: Market index (beta = 1.0) showing hypothetical year with 10% rise and 10% fall
  - Overlay lines for investments with different betas
  - User can toggle lines on/off to compare specific investments
  - Hover to see exact percentage moves
- **Design Notes:**
  - **Scenario Display:** Market rises 10%, then falls 10%
  - **Plotted Investments:**
    - Treasury Bonds (beta 0.0): Flat line, no correlation
    - Conservative Fund (beta 0.5): Rises 5%, falls 5%
    - Market Index (beta 1.0): Rises 10%, falls 10% (baseline)
    - Growth Stocks (beta 1.3): Rises 13%, falls 13%
    - Aggressive Fund (beta 1.6): Rises 16%, falls 16%
  - Color coding matching risk level (green to red)
  - Annotation: "Beta measures market sensitivity—higher beta amplifies both gains AND losses"
  - Interactive controls: Select market scenario (up 20%, down 30%, etc.)
  - Show calculations: "Market: +10% × Beta 1.3 = +13%"
  - Responsive design with tooltip explanations
  - Print version showing 2-3 key scenarios

### 5. Sharpe Ratio Comparison Bar Chart
- **Purpose:** Compare risk-adjusted returns across different investments
- **Format/Inputs:** Horizontal bar chart with calculation breakdown
- **Expected Outputs:** Understanding that highest return doesn't mean best risk-adjusted performance
- **Interaction Model:**
  - Bar chart showing Sharpe ratios for six investments
  - Bars sorted from highest to lowest Sharpe ratio
  - Click any bar to see calculation breakdown
  - Toggle to show raw returns vs. Sharpe ratios for comparison
- **Design Notes:**
  - **Investments Displayed (with sample Sharpe ratios):**
    - Treasury Bonds: 2.48 (highest—excellent risk-adjusted return)
    - Balanced Fund: 0.69
    - Large-Cap Index: 0.72
    - Small-Cap Growth: 0.44
    - Emerging Markets: 0.32 (lowest—high risk poorly compensated)
    - High-Yield Savings: -2.0 (below risk-free rate)
  - Color gradient: Dark green (high) to red (low)
  - On-click expansion shows:
    - Return: X%
    - Risk-Free Rate: 2.5%
    - Standard Deviation: Y%
    - Calculation: (X% - 2.5%) ÷ Y% = Sharpe Ratio
  - Side-by-side comparison option: Show returns vs. Sharpe ratios to illustrate difference
  - Annotation: "Higher Sharpe ratio = better return per unit of risk taken"
  - Interpretation guide: "Above 1.0 = excellent, 0.5-1.0 = good, below 0.5 = poor"
  - Accessibility: Table view alternative with all data

### 6. Age-Based Portfolio Allocation Chart
- **Purpose:** Demonstrate how appropriate risk levels change with age/time horizon
- **Format/Inputs:** Visual chart showing recommended allocations at different ages
- **Expected Outputs:** Understanding that age-appropriate investing is essential
- **Interaction Model:**
  - Three side-by-side pie charts for ages 25, 45, and 65
  - Interactive slider allowing users to see allocation at any age 20-70
  - Click each pie slice to see investment details
  - Show projected growth scenarios for each allocation
- **Design Notes:**
  - **Age 25 Allocation (Aggressive):**
    - Stocks: 85% (Large pie slice, blue)
    - Bonds: 10% (Small slice, green)
    - Cash: 5% (Tiny slice, gray)
    - Time horizon: 40 years to retirement
    - Risk level: High (can weather volatility)
  - **Age 45 Allocation (Moderate):**
    - Stocks: 60% (Medium-large slice, blue)
    - Bonds: 30% (Medium slice, green)
    - Cash: 10% (Small slice, gray)
    - Time horizon: 20 years to retirement
    - Risk level: Moderate (balance growth and stability)
  - **Age 65 Allocation (Conservative):**
    - Stocks: 35% (Smaller slice, blue)
    - Bonds: 50% (Large slice, green)
    - Cash: 15% (Medium slice, gray)
    - Time horizon: Approaching/in retirement
    - Risk level: Low (capital preservation priority)
  - Include projection box showing $500/month growth at each allocation
  - Rule of thumb display: "Simple guideline: Stock % = 110 - Your Age"
  - Customization: Users can input their age to see recommended allocation
  - Accessibility: Text descriptions of each allocation with rationale

## Day 2 Assets

### 1. Risk Tolerance Assessment Tool (PRIMARY SKILL BUILDER)
- **Purpose:** Comprehensive assessment to determine student's personal risk tolerance
- **Format/Inputs:** Multi-section digital questionnaire with scoring algorithm
- **Expected Outputs:** Risk tolerance score (0-100) with interpretation and recommended allocations
- **Interaction Model:** Progressive questionnaire with three sections, automatic scoring, personalized results
- **Design Notes:**

  **SECTION A: Time Horizon Questions (0-30 points)**
  - Question 1: "When do you expect to need this money?"
    - Within 3 years (0 pts)
    - 3-7 years (5 pts)
    - 7-15 years (15 pts)
    - 15-25 years (25 pts)
    - 25+ years (30 pts)
  - Question 2: "How stable is your income source?"
    - Very unstable/no income (0 pts)
    - Somewhat unstable (5 pts)
    - Moderately stable (15 pts)
    - Very stable (30 pts)
  - Question 3: "Do you have an adequate emergency fund (3-6 months expenses)?"
    - No emergency fund (0 pts)
    - Less than 1 month (5 pts)
    - 1-3 months (15 pts)
    - 3-6 months (25 pts)
    - More than 6 months (30 pts)
  - Question 4: "What percentage of your net worth is this investment?"
    - More than 75% (-10 pts penalty)
    - 50-75% (0 pts)
    - 25-50% (10 pts)
    - 10-25% (20 pts)
    - Less than 10% (30 pts)

  **SECTION B: Financial Situation Questions (0-35 points)**
  - Question 5: "Describe your current debt situation"
    - High-interest debt (credit cards) (0 pts)
    - Student loans but manageable (15 pts)
    - Low-interest mortgage only (25 pts)
    - No debt (35 pts)
  - Question 6: "Your current savings/investment level is:"
    - Just starting, little saved (5 pts)
    - Building gradually (15 pts)
    - On track for goals (25 pts)
    - Ahead of savings goals (35 pts)
  - Question 7: "If you lost your job, how long could you maintain your lifestyle?"
    - Less than 1 month (0 pts)
    - 1-3 months (10 pts)
    - 3-6 months (20 pts)
    - 6-12 months (30 pts)
    - More than 12 months (35 pts)

  **SECTION C: Emotional Temperament Questions (0-35 points)**
  - Question 8: "Your $10,000 investment drops to $7,000 in 6 months. You:"
    - Panic and sell immediately (0 pts)
    - Feel very uncomfortable but hold (10 pts)
    - Stay relatively calm and hold (25 pts)
    - See it as buying opportunity (35 pts)
  - Question 9: "How often would you check your portfolio value?"
    - Multiple times daily (0 pts)
    - Daily (5 pts)
    - Weekly (15 pts)
    - Monthly (25 pts)
    - Quarterly or less (35 pts)
  - Question 10: "Have you made financial decisions you regretted based on fear or excitement?"
    - Yes, frequently (0 pts)
    - Yes, occasionally (15 pts)
    - Rarely (25 pts)
    - No, I stay disciplined (35 pts)
  - Question 11: "How much portfolio volatility can you tolerate without losing sleep?"
    - Very little—stability critical (0 pts)
    - Moderate swings acceptable (15 pts)
    - Significant volatility okay (30 pts)
    - High volatility no problem (35 pts)

  **SCORING & INTERPRETATION:**
  - Total Score: 0-100 points (sum of all questions)

  - **Conservative (0-30 points):**
    - Profile: Low risk tolerance
    - Recommended Allocation: 20% stocks, 70% bonds, 10% cash
    - Appropriate Investments: Savings accounts, CDs, government bonds, stable value funds
    - Expected Return: 3-5% annually
    - Risk Level: Low volatility, minimal downside
    - Time Horizon: Short-term (0-5 years)
    - Message: "Your profile suggests you prioritize stability and capital preservation. This is appropriate if you have a short time horizon or cannot afford significant losses."

  - **Moderate (31-60 points):**
    - Profile: Balanced risk tolerance
    - Recommended Allocation: 50-60% stocks, 35-40% bonds, 5-10% cash
    - Appropriate Investments: Balanced funds, bond funds, large-cap stock indexes, REITs
    - Expected Return: 6-8% annually
    - Risk Level: Moderate volatility, some downside protection
    - Time Horizon: Medium-term (5-15 years)
    - Message: "Your profile suggests you want growth but with manageable risk. This balanced approach provides growth potential while limiting extreme volatility."

  - **Aggressive (61-100 points):**
    - Profile: High risk tolerance
    - Recommended Allocation: 80-90% stocks, 10-20% bonds, 0-5% cash
    - Appropriate Investments: Stock index funds, growth stocks, small-cap funds, emerging markets
    - Expected Return: 8-12% annually
    - Risk Level: High volatility, significant downside possible
    - Time Horizon: Long-term (15+ years)
    - Message: "Your profile suggests you can handle volatility in pursuit of long-term growth. This is appropriate with a long time horizon and stable financial situation."

  **RESULTS DISPLAY:**
  - Visual gauge showing where student falls on Conservative-Moderate-Aggressive spectrum
  - Pie chart showing recommended allocation
  - Key insights: "Your primary constraint is [time horizon / financial situation / emotional temperament]"
  - Comparison: "Your time horizon suggests [X] tolerance, but your temperament suggests [Y] tolerance. Use the lower of the two."
  - Action items: Specific next steps based on profile
  - Disclaimer: "This is an educational tool, not professional financial advice. Consider consulting a qualified advisor."

  **TECHNICAL SPECIFICATIONS:**
  - Progressive disclosure: Show one section at a time
  - Save progress: LocalStorage to prevent losing data if navigating away
  - Retake option: Allow students to adjust answers and see how score changes
  - Print results: PDF export of full assessment and recommendations
  - Accessibility: Keyboard navigation, screen reader compatible
  - Mobile-responsive: Works on all device sizes
  - Security: No personal data collected or stored on servers
  - Load time: <2 seconds for assessment tool

### 2. Risk Metrics Calculator
- **Purpose:** Calculate standard deviation, beta, and Sharpe ratio for six different investments
- **Format/Inputs:** Interactive calculator with historical return data pre-loaded
- **Expected Outputs:** Calculated risk metrics with interpretation for each investment
- **Interaction Model:**
  - Six investment panels, each showing 5 years of historical returns
  - Click "Calculate Metrics" button to compute standard deviation, beta, Sharpe ratio
  - Step-by-step calculation display showing formula and process
  - Comparison table showing all six investments side-by-side
- **Design Notes:**

  **INVESTMENT DATA (Pre-Loaded):**

  **Investment A: U.S. Treasury Bonds**
  - Historical Returns: Year 1: 3.2%, Year 2: 2.8%, Year 3: 3.5%, Year 4: 3.0%, Year 5: 3.1%
  - Average Return: 3.12%
  - Standard Deviation: 0.25%
  - Beta: 0.05
  - Sharpe Ratio: 2.48

  **Investment B: Large-Cap Stock Index**
  - Historical Returns: Year 1: 12%, Year 2: -8%, Year 3: 22%, Year 4: 15%, Year 5: 8%
  - Average Return: 9.8%
  - Standard Deviation: 10.2%
  - Beta: 1.0
  - Sharpe Ratio: 0.72

  **Investment C: Small-Cap Growth Stocks**
  - Historical Returns: Year 1: 18%, Year 2: -15%, Year 3: 35%, Year 4: 22%, Year 5: -5%
  - Average Return: 11%
  - Standard Deviation: 19.4%
  - Beta: 1.4
  - Sharpe Ratio: 0.44

  **Investment D: Emerging Markets**
  - Historical Returns: Year 1: 25%, Year 2: -22%, Year 3: 40%, Year 4: 18%, Year 5: -8%
  - Average Return: 10.6%
  - Standard Deviation: 25.1%
  - Beta: 1.6
  - Sharpe Ratio: 0.32

  **Investment E: Balanced Fund (60/40)**
  - Historical Returns: Year 1: 8%, Year 2: -3%, Year 3: 14%, Year 4: 10%, Year 5: 5%
  - Average Return: 6.8%
  - Standard Deviation: 6.2%
  - Beta: 0.6
  - Sharpe Ratio: 0.69

  **Investment F: High-Yield Savings**
  - Historical Returns: Year 1: 2.1%, Year 2: 2.3%, Year 3: 2.0%, Year 4: 2.2%, Year 5: 2.4%
  - Average Return: 2.2%
  - Standard Deviation: 0.15%
  - Beta: 0.0
  - Sharpe Ratio: -2.0

  **CALCULATION FEATURES:**
  - **Average Return Calculation:**
    - Shows: "(Return₁ + Return₂ + Return₃ + Return₄ + Return₅) ÷ 5"
    - Step-by-step display of addition and division
    - Result highlighted

  - **Standard Deviation Calculation:**
    - Option 1: Automatic calculation with result only
    - Option 2: Detailed steps shown (for advanced students)
    - Visual representation: Bar chart showing returns with average line, highlighting variance
    - Interpretation tooltip: "Standard deviation of 10% means roughly 2/3 of years fall within ±10% of average"

  - **Beta Calculation:**
    - Explanation: "Calculated using regression analysis comparing investment returns to market returns"
    - Simplified: Shows correlation without complex formula
    - Interpretation guide:
      - Beta = 0: No market correlation
      - Beta < 1: Less volatile than market
      - Beta = 1: Moves with market
      - Beta > 1: More volatile than market

  - **Sharpe Ratio Calculation:**
    - Formula displayed: (Average Return - Risk-Free Rate) ÷ Standard Deviation
    - Risk-free rate shown: 2.5% (user can adjust if desired)
    - Step-by-step: (9.8% - 2.5%) ÷ 10.2% = 0.72
    - Interpretation scale:
      - Above 1.0: Excellent risk-adjusted return
      - 0.5-1.0: Good
      - 0.0-0.5: Acceptable
      - Below 0.0: Poor (returns below risk-free rate)

  **COMPARISON TABLE:**
  - Side-by-side display of all six investments
  - Sortable columns: Click to sort by return, risk, beta, or Sharpe ratio
  - Color coding: Green (best) to red (worst) for each metric
  - Download as spreadsheet option

  **TECHNICAL SPECIFICATIONS:**
  - Responsive design for mobile and desktop
  - Print-friendly version available
  - Calculations update in real-time
  - Error handling for invalid inputs
  - Accessibility: All calculations have text descriptions
  - Help tooltips on every metric explaining meaning

### 3. Portfolio Construction Tool
- **Purpose:** Build and analyze diversified portfolios for three different investor profiles
- **Format/Inputs:** Interactive allocation builder with drag-and-drop or slider controls
- **Expected Outputs:** Portfolio metrics, projections, and comparison across three profiles
- **Interaction Model:**
  - Three tabs for three investor profiles (Maria age 25, David age 45, Sharon age 63)
  - Allocation controls for each of six investment options
  - Real-time calculation of portfolio metrics as allocations change
  - Visual representation of allocation with pie charts
  - Projection calculator showing growth over time horizon
- **Design Notes:**

  **INVESTOR PROFILES:**

  **Profile 1: Maria (Age 25, Aggressive)**
  - Situation: Recent graduate, $45,000 salary, contributing $300/month to 401(k)
  - Time Horizon: 40 years until retirement
  - Risk Tolerance: High (long timeline, stable job, can recover from volatility)
  - Goals: Maximum long-term wealth accumulation
  - Starting Suggested Allocation:
    - Treasury Bonds: 0%
    - Large-Cap Stocks: 50%
    - Small-Cap Growth: 25%
    - Emerging Markets: 15%
    - Balanced Fund: 10%
    - Savings: 0%

  **Profile 2: David (Age 45, Moderate)**
  - Situation: Established career, $78,000 salary, has $150,000 saved
  - Time Horizon: 20 years until retirement
  - Risk Tolerance: Moderate (needs growth but less time to recover from setbacks)
  - Goals: Steady growth with manageable volatility
  - Starting Suggested Allocation:
    - Treasury Bonds: 20%
    - Large-Cap Stocks: 40%
    - Small-Cap Growth: 10%
    - Emerging Markets: 5%
    - Balanced Fund: 20%
    - Savings: 5%

  **Profile 3: Sharon (Age 63, Conservative)**
  - Situation: Retiring in 2 years, $620,000 saved, needs income and stability
  - Time Horizon: 2 years until retirement, then 20+ years in retirement
  - Risk Tolerance: Low (cannot afford significant losses before retirement)
  - Goals: Capital preservation with modest growth
  - Starting Suggested Allocation:
    - Treasury Bonds: 40%
    - Large-Cap Stocks: 25%
    - Small-Cap Growth: 0%
    - Emerging Markets: 0%
    - Balanced Fund: 25%
    - Savings: 10%

  **ALLOCATION CONTROLS:**
  - Method 1: Slider controls (0-100%) for each investment
  - Method 2: Numeric input boxes
  - Method 3: Drag-and-drop allocation (mobile-friendly)
  - Real-time validation: Total must equal 100%
  - Visual indicator if total ≠ 100% with error message
  - "Reset to Suggested" button to restore defaults
  - "Equalize All" button for experimentation (equal weight across all six)

  **PORTFOLIO METRICS (Auto-Calculated):**
  - **Weighted Average Return:**
    - Formula: Σ(Allocation% × Investment Return)
    - Example: (0.50 × 9.8%) + (0.25 × 11%) + (0.15 × 10.6%) + (0.10 × 6.8%) = 9.98%
    - Display: "Expected Annual Return: 9.98%"

  - **Portfolio Standard Deviation:**
    - Calculated using correlation matrix (simplified for educational tool)
    - Accounts for diversification benefit
    - Display: "Portfolio Volatility: 12.4% (moderate-high)"

  - **Portfolio Beta:**
    - Weighted average of individual betas
    - Display: "Market Sensitivity: 1.12 (12% more volatile than market)"

  - **Portfolio Sharpe Ratio:**
    - Formula: (Portfolio Return - 2.5%) ÷ Portfolio SD
    - Display: "Risk-Adjusted Return: 0.60 (good)"

  **GROWTH PROJECTIONS:**
  - Input fields:
    - Initial investment amount
    - Monthly contribution
    - Time horizon (years)
  - Calculation:
    - Uses compound growth formula with monthly contributions
    - Accounts for portfolio's expected return
  - Visual display:
    - Line graph showing portfolio growth over time
    - Hover to see value at any year
    - Comparison overlay showing different allocation outcomes

  **Example for Maria:**
  - $300/month for 40 years at 9.98% = ~$1,623,000
  - Show breakdown: Contributions ($144,000) + Growth ($1,479,000)

  **Example for David:**
  - $500/month for 20 years at 7.31% = ~$262,000
  - Plus $150,000 existing savings growing at 7.31% = ~$597,000
  - Total projected: ~$859,000

  **Example for Sharon:**
  - $620,000 growing at 5.62% for 20 years = ~$1,844,000
  - Shows retirement income potential

  **COMPARISON VIEW:**
  - Side-by-side display of all three portfolios
  - Comparative metrics in table format
  - Highlighting of key differences (risk levels, projections, allocations)
  - "What-If" scenarios:
    - "What if Maria used Sharon's allocation?" (Shows lost growth)
    - "What if Sharon used Maria's allocation?" (Shows crash risk)

  **TECHNICAL SPECIFICATIONS:**
  - Real-time calculation (no page refresh needed)
  - Save portfolios: LocalStorage to preserve student work
  - Export functionality: PDF or spreadsheet download
  - Print-friendly layout
  - Mobile-responsive with touch-friendly controls
  - Accessibility: Keyboard controls, screen reader compatible
  - Help system: Contextual tooltips explaining each feature
  - Performance: Calculations complete in <100ms

### 4. Historical Volatility Simulator
- **Purpose:** Analyze historical market volatility and make investment decisions during crisis
- **Format/Inputs:** Interactive timeline showing real market data with decision points
- **Expected Outputs:** Understanding of market recovery patterns and importance of staying invested
- **Interaction Model:**
  - Timeline showing S&P 500 from 2007-2020 with notable events
  - "Crisis Decision Point" scenario where students choose action during 2008 crash
  - Outcome visualization showing results of each decision
  - Comparison of different investor responses
- **Design Notes:**

  **HISTORICAL DATA DISPLAY:**
  - **Timeline:** 2007-2020 (13-year period covering financial crisis and recovery)
  - **Key Events Annotated:**
    - 2007: Pre-crisis peak
    - 2008: Financial crisis (-37% for year)
    - 2009: Recovery begins (+26%)
    - 2010-2019: Bull market (+250% cumulative)
    - 2020: Pandemic crash (-34% in one month) then recovery

  - Interactive elements:
    - Scrub through timeline to see portfolio value at any point
    - Toggle between absolute value and percentage change views
    - Highlight specific crash/recovery periods
    - Compare to inflation-adjusted returns

  **CRISIS DECISION SCENARIO:**

  **Setup:**
  - Date: December 2008
  - Your situation: Invested $10,000 in January 2008
  - Current value: $6,300 (down 37%)
  - Time horizon: Need money in 5 years (2013) for house down payment

  **Your Options:**
  - **Option A:** Sell now, move to bonds (lock in $3,700 loss, safety for remaining)
  - **Option B:** Hold current portfolio (ride out volatility, hope for recovery)
  - **Option C:** Invest additional $2,000 (double down, buy at low prices)
  - **Option D:** Switch to balanced fund (reduce volatility, still some growth)

  **Student Selection:**
  - Choose one option
  - Provide reasoning (text box): "Why did you choose this?"
  - Submit decision to see outcomes

  **OUTCOME VISUALIZATION:**

  Shows what actually happened with each choice:

  **Option A Outcome (Sell to Bonds):**
  - 2008: $6,300
  - 2009: $6,520 (3.5% bond return)
  - 2010: $6,748
  - 2011: $6,984
  - 2012: $7,229
  - 2013: $7,482 (target year—still below initial $10,000)
  - Analysis: "You avoided further losses but never recovered. Final loss: $2,518 (25%)"

  **Option B Outcome (Hold Stocks):**
  - 2008: $6,300
  - 2009: $7,938 (+26%)
  - 2010: $9,135 (+15%)
  - 2011: $9,135 (flat year)
  - 2012: $11,781 (+29%)
  - 2013: $14,946 (+27%)—Available for house: $14,946
  - Analysis: "Patience rewarded. Final gain: $4,946 (49%) from initial investment"

  **Option C Outcome (Buy More at $2,000):**
  - Total now invested: $12,000 ($10,000 original + $2,000 additional)
  - 2008: $7,560 (includes new $2,000)
  - 2009-2013: Same percentage returns as Option B
  - 2013: $17,936
  - Analysis: "Buying the dip paid off. Return on total $12,000 invested: $5,936 (49.5%)"

  **Option D Outcome (Switch to Balanced):**
  - 2008: $6,300 (starting point)
  - 2009-2013: Moderate returns (half stocks, half bonds)
  - 2013: $10,800
  - Analysis: "Middle ground—recovered initial investment with modest gain"

  **LEARNING INSIGHTS DISPLAY:**
  - "The patient investor (Option B) outperformed the fearful seller (Option A) by $7,464"
  - "Historically, every market crash has been followed by recovery and new highs"
  - "Time horizon matters: With 5 years, recovery was possible. With 1 year, staying in stocks might have been too risky"
  - "Emotional discipline is as important as analytical knowledge"

  **ADDITIONAL SCENARIOS:**
  - **Scenario 2:** 2000 Dot-com bubble
  - **Scenario 3:** 2020 Pandemic crash (rapid recovery)
  - Each shows same pattern: Crash → Recovery → New Highs

  **TECHNICAL SPECIFICATIONS:**
  - Responsive timeline with touch/mouse controls
  - Smooth animations showing portfolio value changes
  - Print functionality for scenario outcomes
  - Comparison mode: See all four options side-by-side
  - Reflection prompts after seeing outcomes
  - Mobile-optimized with simplified visualization

## Skill Builder Assets (Integrated Across Day 2)

### Risk-Return Investment Analyzer (Comprehensive Tool)
- **Purpose:** Central interactive platform integrating all Day 2 activities
- **Components:** Risk Tolerance Assessment + Risk Metrics Calculator + Portfolio Builder + Historical Simulator
- **Design:** Unified interface with navigation between four modules
- **Progression:** Students complete in sequence, with each module building on previous learning
- **Data Persistence:** Saves progress across sessions, allows return to previous work
- **Export:** Comprehensive report combining all assessments and portfolio analyses

## Downloadable Resources (Printable PDFs for Accessibility)

### 1. Risk Tolerance Assessment Worksheet (PDF)
- **Purpose:** Paper-based version of digital assessment
- **Contents:**
  - All 11 questions with multiple-choice answer options
  - Scoring table with point values
  - Interpretation guide for Conservative/Moderate/Aggressive profiles
  - Space for recommended allocation based on score
  - Reflection questions for post-assessment analysis
- **Format:** 3-page PDF, printer-friendly (black and white)
- **Accessibility:** Large font, high contrast, clear structure

### 2. Risk Metrics Calculation Worksheets (PDF)
- **Purpose:** Manual calculation guide for students without technology access
- **Contents:**
  - Six investment data tables with 5-year historical returns
  - Step-by-step calculation templates for:
    - Average return
    - Standard deviation (simplified formula with worked example)
    - Beta interpretation guide
    - Sharpe ratio calculation
  - Comparison table to record all metrics
  - Analysis questions for each investment
- **Format:** 5-page PDF with clear calculation spaces
- **Accessibility:** Formula boxes, gridlines for organization

### 3. Portfolio Construction Worksheets (PDF)
- **Purpose:** Paper-based portfolio building for three investor profiles
- **Contents:**
  - Profile descriptions for Maria, David, and Sharon
  - Allocation tables with percentage columns
  - Portfolio metrics calculation guides
  - Growth projection tables (present value calculations)
  - Comparison matrix for all three portfolios
  - Reflection questions on appropriate risk levels
- **Format:** 4-page PDF with tables and calculation spaces
- **Accessibility:** Clear tables, ample writing space

### 4. Historical Market Data Analysis Guide (PDF)
- **Purpose:** Static version of historical volatility simulator
- **Contents:**
  - S&P 500 annual returns table (1990-2025)
  - Notable crash/recovery periods highlighted
  - 2008 crisis decision scenario with written explanation of four options
  - Outcome tables showing results of each decision
  - Charts showing long-term market growth despite volatility
  - Analysis questions about market timing and discipline
- **Format:** 3-page PDF with data tables and charts
- **Accessibility:** High-contrast charts, large data tables

### 5. Complete Risk-Return Analysis Report Template (PDF)
- **Purpose:** Comprehensive summary document combining all activities
- **Contents:**
  - Cover page with student name and date
  - Section 1: Risk Tolerance Assessment results
  - Section 2: Risk Metrics calculations for six investments
  - Section 3: Portfolio constructions for three profiles
  - Section 4: Historical volatility analysis and personal decision
  - Section 5: Personal Investment Plan
    - My risk tolerance profile: ___
    - My time horizon: ___
    - My recommended allocation: ___
    - My action steps: ___
  - Appendix: Key formulas and definitions
- **Format:** 8-page PDF template for completion
- **Use:** Can be used as take-home assignment or portfolio piece

## Technical Implementation Notes for Developers

### Development Priorities

**Phase 1: Core Functionality (High Priority)**
1. Risk Tolerance Assessment Tool (primary skill builder)
2. Risk Metrics Calculator (essential for learning objectives)
3. Portfolio Construction Tool (hands-on application)
4. Historical Volatility Simulator (emotional learning component)

**Phase 2: Supporting Visuals (Medium Priority)**
5. Risk-Return Scatterplot
6. Historical Market Returns Chart
7. Age-Based Portfolio Allocation Chart
8. Sharpe Ratio Comparison Bar Chart

**Phase 3: Enhancement Visuals (Lower Priority)**
9. Diversification Visual Demonstration
10. Beta Comparison Visualization

### Technical Requirements

**Browser Compatibility:**
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

**Responsive Design Breakpoints:**
- Desktop: 1920×1080 and above
- Laptop: 1366×768
- Tablet: 768×1024 (landscape and portrait)
- Mobile: 375×667 minimum (iPhone SE)

**Performance Targets:**
- Initial load: <3 seconds on 3G connection
- Interactive tool response: <100ms for calculations
- Smooth animations: 60fps
- Chart rendering: <500ms

**Accessibility (WCAG 2.1 AA Compliance):**
- Full keyboard navigation for all interactive elements
- Screen reader compatibility (ARIA labels on all inputs)
- High contrast mode support
- Adjustable text sizes (125%, 150%, 200%)
- Alternative text for all charts and visualizations
- Focus indicators clearly visible
- Error messages descriptive and helpful

**Data Storage:**
- LocalStorage for saving student progress
- No collection of personal financial data
- Optional database integration for multi-session persistence
- Export functionality (PDF, CSV, JSON)
- Clear data/reset functionality

**Security:**
- No backend required (client-side calculations)
- No transmission of personal data
- Input validation to prevent injection attacks
- Sanitization of user text inputs

### Calculation Accuracy

**Critical: Financial calculations must be precise**
- Use integers for currency (cents, not dollars) to avoid floating-point errors
- Round to 2 decimal places for display
- Validate all inputs (positive numbers, valid ranges)
- Handle edge cases (division by zero, negative standard deviation)

**Example of proper implementation:**
```javascript
// WRONG (floating-point errors)
const portfolioValue = 10000.50 * 0.10; // May give 1000.0499999999

// RIGHT (integer math)
const portfolioCents = 1000050; // Store as cents
const returnCents = Math.round(portfolioCents * 0.10);
const portfolioValue = returnCents / 100; // Convert to dollars for display
```

### Chart and Visualization Libraries

**Recommended:**
- Chart.js for standard charts (bar, line, pie)
- D3.js for complex custom visualizations if needed
- SVG for static infographics (better scaling than PNG)

**Requirements:**
- Responsive sizing (scale with viewport)
- Print-friendly (ensure charts visible in PDF export)
- Accessible (text alternatives, ARIA labels)
- Color-blind friendly palettes

### User Experience Guidelines

**Progressive Disclosure:**
- Don't overwhelm with all options at once
- Step-by-step guidance for complex tools
- "Help" icons with tooltips on technical terms
- Examples and demos before expecting independent work

**Error Prevention:**
- Input validation in real-time
- Clear constraints (total must equal 100%)
- Confirmation dialogs before destructive actions ("Reset All")
- Autosave to prevent data loss

**Feedback:**
- Loading indicators for calculations
- Success messages when actions complete
- Immediate validation feedback on inputs
- Progress indicators for multi-step processes

### Testing Recommendations

**User Testing:**
- Test with actual high school students before launch
- Observe where they get confused or stuck
- Collect feedback on clarity of instructions
- Iterate based on real user behavior

**Device Testing:**
- Test on low-end devices (not just latest iPhone)
- Verify performance on older browsers
- Check on small screens (iPhone SE, not just Max)
- Test with touch and mouse inputs

**Accessibility Testing:**
- Test with screen reader (NVDA, JAWS, VoiceOver)
- Navigate entirely with keyboard (no mouse)
- Test in high contrast mode
- Verify with zoom at 200%

**Calculation Testing:**
- Verify all formulas against known correct values
- Test edge cases (zero returns, extreme volatility)
- Validate against professional financial calculators
- Check rounding and precision

### Documentation Needed

**For Developers:**
- API documentation if building backend
- Component library for reusable elements
- Calculation formulas with references
- Setup guide for local development
- Deployment process documentation

**For Teachers:**
- Quick start guide for classroom use
- Troubleshooting common technical issues
- How to interpret student results
- Privacy and data security information

**For Students:**
- User guide for each tool
- Help system within application
- Tutorial videos (optional)
- FAQ for common questions

---

**Asset Specifications Status:** ✅ Complete and ready for development

**Total Interactive Assets:** 10 major tools + 5 printable PDFs
**Primary Skill Builder:** Risk-Return Investment Analyzer (integrated platform)
**Accessibility:** Full compliance with printable alternatives for all digital tools
**State Variables:** None required (L-64 is Tier 3, fully universal)

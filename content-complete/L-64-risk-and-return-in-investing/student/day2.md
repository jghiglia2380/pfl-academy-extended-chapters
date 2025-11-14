# L-64: Risk and Return in Investing - Learning Lab

> **Implementation Note:**
> Use the standardized header template (templates/student-header-template.html) for consistent styling.

## Learning Lab Overview
- **L-Chapter:** L-64: Risk and Return in Investing
- **Duration:** 55 minutes
- **Focus:** Hands-on analysis of risk-return tradeoffs through portfolio construction and risk metric calculations
- **Learning Format:** 90% activities, 10% facilitation and reflection

## Materials Needed
- Risk-Return Investment Analyzer (accessible via learning platform)
- Portfolio construction worksheets
- Risk metric calculator
- Historical market data visualizations
- Personal risk tolerance assessment tool

## Pre-Class Setup
1. Complete Day 1 content review
2. Think about your own risk tolerance and time horizon
3. Consider your financial goals (from earlier lessons)

## Learning Lab Activities

### Activity 1: Risk Tolerance Assessment and Analysis (12 minutes)
**Objective:** Determine your personal risk tolerance and understand how it should inform investment decisions

**Instructions:**
1. Complete the Interactive Risk Tolerance Assessment with three components:

   **PART A: Time Horizon Questions**
   - When do you expect to need this money? (Short-term: <5 years, Medium: 5-15 years, Long-term: 15+ years)
   - How stable is your income source?
   - Do you have an adequate emergency fund?
   - What percentage of your net worth is this investment?

   **PART B: Financial Situation Questions**
   - Current savings level (adequate, building, minimal)
   - Debt situation (none, manageable, high-interest)
   - Income stability (very stable, moderately stable, uncertain)
   - Other investments or assets

   **PART C: Emotional Temperament Questions**
   - If your $10,000 investment dropped to $7,000 in six months, would you:
     - Panic and sell immediately
     - Feel uncomfortable but hold
     - Stay calm and hold
     - See it as a buying opportunity
   - How would you react to seeing daily portfolio value fluctuations?
   - Have you ever made a financial decision you regretted based on fear or excitement?
   - How much portfolio volatility can you tolerate without losing sleep?

2. The tool calculates your risk tolerance score:
   - **Conservative (0-30 points):** Low risk tolerance
     - Appropriate investments: Savings accounts, CDs, government bonds, stable value funds
     - Typical portfolio: 20% stocks, 80% bonds/cash
     - Expected return: 3-5% annually with low volatility

   - **Moderate (31-60 points):** Balanced risk tolerance
     - Appropriate investments: Balanced funds, bond funds, large-cap stocks, REITs
     - Typical portfolio: 50-60% stocks, 40-50% bonds
     - Expected return: 6-8% annually with moderate volatility

   - **Aggressive (61-100 points):** High risk tolerance
     - Appropriate investments: Stock index funds, growth stocks, emerging markets, small-caps
     - Typical portfolio: 80-100% stocks, 0-20% bonds
     - Expected return: 8-12% annually with high volatility

3. Reflect on your results:
   - Does your calculated risk tolerance match your self-perception?
   - What surprised you about the assessment?
   - How might your risk tolerance change in 10, 20, or 30 years?
   - Are there specific factors (time horizon, financial situation, temperament) pulling you in different directions?

4. **Important insight:** Your risk tolerance should be the MINIMUM of your three components. If you have a long time horizon (high risk capacity) but panic during downturns (low emotional tolerance), your actual risk tolerance is low. Invest accordingly.

### Activity 2: Investment Risk Metrics Calculator (15 minutes)
**Objective:** Calculate and interpret standard deviation, beta, and Sharpe ratio for different investments

**Instructions:**
1. You'll analyze six different investment options using the Risk Metrics Calculator:

   **Investment A: U.S. Treasury Bonds**
   - Historical returns: Years 1-5: [3.2%, 2.8%, 3.5%, 3.0%, 3.1%]
   - Calculate average return: 3.12%
   - Calculate standard deviation: ~0.25% (very low volatility)
   - Beta: 0.05 (minimal market correlation)
   - Risk-free rate: 2.5%
   - Calculate Sharpe ratio: (3.12% - 2.5%) / 0.25% = 2.48 (excellent risk-adjusted return)

   **Investment B: Large-Cap Stock Index (S&P 500)**
   - Historical returns: Years 1-5: [12%, -8%, 22%, 15%, 8%]
   - Calculate average return: 9.8%
   - Calculate standard deviation: ~10.2% (moderate volatility)
   - Beta: 1.0 (by definition, tracks market)
   - Calculate Sharpe ratio: (9.8% - 2.5%) / 10.2% = 0.72

   **Investment C: Small-Cap Growth Stocks**
   - Historical returns: Years 1-5: [18%, -15%, 35%, 22%, -5%]
   - Calculate average return: 11%
   - Calculate standard deviation: ~19.4% (high volatility)
   - Beta: 1.4 (40% more volatile than market)
   - Calculate Sharpe ratio: (11% - 2.5%) / 19.4% = 0.44 (lower due to high volatility)

   **Investment D: Emerging Markets**
   - Historical returns: Years 1-5: [25%, -22%, 40%, 18%, -8%]
   - Calculate average return: 10.6%
   - Calculate standard deviation: ~25.1% (very high volatility)
   - Beta: 1.6 (60% more volatile than market)
   - Calculate Sharpe ratio: (10.6% - 2.5%) / 25.1% = 0.32 (lowest—high risk not well compensated)

   **Investment E: Balanced Fund (60/40 stocks/bonds)**
   - Historical returns: Years 1-5: [8%, -3%, 14%, 10%, 5%]
   - Calculate average return: 6.8%
   - Calculate standard deviation: ~6.2% (moderate-low volatility)
   - Beta: 0.6 (40% less volatile than market)
   - Calculate Sharpe ratio: (6.8% - 2.5%) / 6.2% = 0.69

   **Investment F: High-Yield Savings Account**
   - Historical returns: Years 1-5: [2.1%, 2.3%, 2.0%, 2.2%, 2.4%]
   - Calculate average return: 2.2%
   - Calculate standard deviation: ~0.15% (minimal volatility)
   - Beta: 0.0 (no market correlation)
   - Calculate Sharpe ratio: (2.2% - 2.5%) / 0.15% = -2.0 (negative—below risk-free rate)

2. Using the calculator, compute each metric:
   - **Average Return:** Sum all returns ÷ number of years
   - **Standard Deviation:** Shows how much returns vary from average
     - Formula: √[Σ(return - average)² ÷ (n-1)]
     - Interpretation: Higher = more volatile
   - **Beta:** Measures market sensitivity
     - Calculator uses regression analysis against market returns
     - Interpretation: >1.0 = more volatile than market, <1.0 = less volatile
   - **Sharpe Ratio:** Risk-adjusted return measure
     - Formula: (Average Return - Risk-Free Rate) ÷ Standard Deviation
     - Interpretation: Higher = better return per unit of risk

3. Answer analysis questions:
   - Which investment has the highest Sharpe ratio? What does this mean?
   - Which investment has the highest raw return? Highest risk?
   - Is the highest return investment also the best risk-adjusted performer? Why or why not?
   - How does beta affect your interpretation of an investment's riskiness?
   - For a 25-year-old investing for retirement, which investments seem most appropriate?
   - For a 62-year-old approaching retirement, which investments seem most appropriate?

4. **Key insight:** The "best" investment isn't the one with the highest return—it's the one with the best risk-adjusted return (Sharpe ratio) that matches your risk tolerance and time horizon. Sometimes a lower-return investment is the better choice.

### Activity 3: Portfolio Construction for Different Risk Profiles (18 minutes)
**Objective:** Build diversified portfolios aligned with different investor profiles and analyze their risk-return characteristics

**Instructions:**
1. You'll build three different portfolios using the Risk-Return Investment Analyzer, each for a different investor profile:

   **PROFILE 1: MARIA (Age 25, Aggressive Growth)**
   - **Situation:** Just started career, $45,000 salary, contributing $300/month to 401(k)
   - **Time horizon:** 40 years until retirement
   - **Risk tolerance:** High (can weather volatility, needs long-term growth)
   - **Goals:** Maximum long-term wealth accumulation

   **Build Maria's Portfolio (Total: 100%)**
   - Allocate percentages across the six investment options
   - Suggested aggressive allocation:
     - Treasury Bonds: 0%
     - Large-Cap Stocks: 50%
     - Small-Cap Growth: 25%
     - Emerging Markets: 15%
     - Balanced Fund: 10%
     - Savings Account: 0%

   **Calculate Portfolio Metrics:**
   - Weighted average return: (0.50 × 9.8%) + (0.25 × 11%) + (0.15 × 10.6%) + (0.10 × 6.8%) = 9.98%
   - Portfolio standard deviation: ~12.4% (calculated using correlation)
   - Portfolio beta: ~1.12 (slightly more volatile than market)
   - Portfolio Sharpe ratio: (9.98% - 2.5%) / 12.4% = 0.60

   **Projection:** $300/month for 40 years at 9.98% = approximately $1,623,000

   **PROFILE 2: DAVID (Age 45, Moderate Balance)**
   - **Situation:** Established career, $78,000 salary, has $150,000 saved already
   - **Time horizon:** 20 years until retirement
   - **Risk tolerance:** Moderate (needs growth but can't afford major setbacks)
   - **Goals:** Steady growth with manageable volatility

   **Build David's Portfolio (Total: 100%)**
   - Suggested moderate allocation:
     - Treasury Bonds: 20%
     - Large-Cap Stocks: 40%
     - Small-Cap Growth: 10%
     - Emerging Markets: 5%
     - Balanced Fund: 20%
     - Savings Account: 5%

   **Calculate Portfolio Metrics:**
   - Weighted average return: (0.20 × 3.12%) + (0.40 × 9.8%) + (0.10 × 11%) + (0.05 × 10.6%) + (0.20 × 6.8%) + (0.05 × 2.2%) = 7.31%
   - Portfolio standard deviation: ~7.8% (moderate volatility)
   - Portfolio beta: ~0.68 (less volatile than market)
   - Portfolio Sharpe ratio: (7.31% - 2.5%) / 7.8% = 0.62

   **Projection:** $500/month for 20 years at 7.31% = approximately $262,000 (plus growth on existing $150,000 → $597,000 total)

   **PROFILE 3: SHARON (Age 63, Conservative Preservation)**
   - **Situation:** Retiring in 2 years, $620,000 saved, needs income and stability
   - **Time horizon:** 2 years until retirement, then 20+ years in retirement
   - **Risk tolerance:** Low (cannot afford significant losses before retirement)
   - **Goals:** Capital preservation with modest growth, income generation

   **Build Sharon's Portfolio (Total: 100%)**
   - Suggested conservative allocation:
     - Treasury Bonds: 40%
     - Large-Cap Stocks: 25%
     - Small-Cap Growth: 0%
     - Emerging Markets: 0%
     - Balanced Fund: 25%
     - Savings Account: 10%

   **Calculate Portfolio Metrics:**
   - Weighted average return: (0.40 × 3.12%) + (0.25 × 9.8%) + (0.25 × 6.8%) + (0.10 × 2.2%) = 5.62%
   - Portfolio standard deviation: ~4.5% (low volatility)
   - Portfolio beta: ~0.43 (much less volatile than market)
   - Portfolio Sharpe ratio: (5.62% - 2.5%) / 4.5% = 0.69 (highest—excellent risk-adjusted return)

   **Projection:** $620,000 growing at 5.62% for 20 years = approximately $1,844,000

2. Compare the three portfolios:
   - Which has the highest expected return? Highest risk (standard deviation)?
   - Which has the best Sharpe ratio (risk-adjusted return)?
   - How does age/time horizon affect appropriate allocation?
   - What happens if you use Maria's portfolio for Sharon? (Calculate potential losses in bad year)
   - What happens if you use Sharon's portfolio for Maria? (Calculate opportunity cost over 40 years)

3. Experiment with allocation changes:
   - Increase Maria's emerging markets from 15% to 30%—what happens to risk and return?
   - Add 10% small-cap stocks to Sharon's portfolio—is this justified?
   - Make David's portfolio more conservative (70% bonds/cash)—how does this affect projected retirement savings?

4. **Critical lesson:** There is no "best" portfolio—only the portfolio best suited to YOUR situation. An aggressive portfolio that's perfect for a 25-year-old would be reckless for someone retiring in two years. Age-appropriate investing is essential.

### Activity 4: Historical Volatility Analysis and Decision-Making (10 minutes)
**Objective:** Analyze historical market volatility and make investment decisions under uncertainty

**Instructions:**
1. Review the Historical Market Performance visualization showing stock market returns for the past 30 years:

   **Notable periods:**
   - 2000-2002: Dot-com crash (-37% over 3 years)
   - 2003-2007: Recovery and growth (+102% over 5 years)
   - 2008: Financial crisis (-37% in single year)
   - 2009-2019: Longest bull market in history (+400% over 11 years)
   - 2020: Pandemic crash (-34% in 1 month) then rapid recovery (+65% by year-end)
   - 2022: Inflation/rate hikes (-18% for the year)

   **Average annual return over 30 years:** ~10.2%
   **Standard deviation:** ~18%
   **Best year:** +37.6%
   **Worst year:** -37.0%

2. Complete the "What Would You Do?" scenario:

   **Scenario:** You invested $10,000 in January 2008 in a stock index fund. By December 2008, it's worth $6,300 (down 37%). You need this money in 5 years for a house down payment.

   **Your options:**
   - **Option A:** Sell now, lock in $3,700 loss, move to safe bonds
   - **Option B:** Hold and hope for recovery
   - **Option C:** Invest more (buy while "on sale")
   - **Option D:** Switch to less volatile balanced fund

   **Analysis questions:**
   - What are the risks and benefits of each option?
   - What does historical data suggest typically happens after major crashes?
   - How does your 5-year time horizon affect your decision?
   - What would you do differently if you needed the money in 1 year vs. 15 years?

3. See the outcome: If you held through 2008, your $6,300 grew to:
   - 2010: $8,100 (getting closer)
   - 2012: $10,300 (back to breakeven)
   - 2013: $13,400 (30% profit)
   - 2019: $22,900 (129% profit from 2008 low)

4. **Key lessons:**
   - Market timing is nearly impossible—even professionals get it wrong
   - Time IN the market beats timing the market
   - Volatility is the price you pay for long-term returns
   - Your time horizon determines how much volatility you can tolerate
   - Selling during crashes locks in losses and misses the recovery

5. Reflection questions:
   - Knowing this history, how would you react to a similar crash today?
   - What strategies could help you avoid panic-selling during downturns?
   - How does understanding historical patterns change your investment approach?
   - Would you invest differently at age 25 vs. age 60 given this volatility?

## Reflection & Wrap-up (3 minutes)
1. **Personal commitment:** Based on today's activities, what's your personal investment approach?
   - My risk tolerance is: [Conservative / Moderate / Aggressive]
   - My current time horizon is: ___ years
   - My appropriate asset allocation is: ___% stocks, ___% bonds, ___% cash
   - One thing I'll do differently in my investing: ________________________________

2. **Key insight:** What was your biggest "aha" moment today about risk and return?

3. **Action item:** What specific step will you take in the next week to apply what you learned?

## Key Takeaways
- Risk tolerance depends on three factors: time horizon, financial situation, and emotional temperament—your actual tolerance is the minimum of these three
- Higher returns require accepting higher risk, but the "best" investment is determined by risk-adjusted returns (Sharpe ratio), not just raw returns
- Portfolio construction should match your life stage—aggressive growth for young investors with decades ahead, conservative preservation for those near retirement
- Standard deviation, beta, and Sharpe ratio are objective tools for measuring and comparing investment risk
- Historical market volatility shows dramatic short-term swings but positive long-term trends—time horizon determines whether volatility is your friend or enemy
- Age-appropriate investing is essential—what's perfect for a 25-year-old can be reckless for a 60-year-old, and vice versa

# L-65: Investment Portfolio Diversification - Learning Lab

> **Implementation Note:**
> Use the standardized header template (templates/student-header-template.html) for consistent styling.
> This includes:
> - Purple header with navigation menu (Home, Curriculum, Resources, Profile)
> - Left navigation with blue vertical indicators for active items and green checkmarks for completed items
> - Content styling using the standard component classes

## Learning Lab Overview
**L-Chapter:** 65 - Investment Portfolio Diversification
**Duration:** 55 minutes
**Focus:** Hands-on portfolio construction, correlation analysis, asset allocation optimization, and rebalancing practice
**Learning Format:** Activity-based stations with portfolio building tools and market simulations

## Materials Needed
- Portfolio Diversification Builder (digital tool)
- Correlation Matrix Analyzer (digital tool)
- Asset Allocation Optimizer (digital tool)
- Rebalancing Simulator (digital tool)
- Calculator (built-in or separate)

## Pre-Class Setup
Before beginning today's learning lab:
1. Ensure you can access all four digital tools
2. Have your notes from Day 1 available for reference
3. Be prepared to build and analyze multiple portfolio strategies
4. Clear calculator or have calculation tool ready

## Learning Lab Activities

### Activity 1: Correlation Detective Challenge (13 minutes)

**Objective:** Understand how correlation between investments affects portfolio risk

**Instructions:**
1. Using the Correlation Matrix Analyzer, you'll examine historical correlation data between different asset classes:
   - US Large-Cap Stocks
   - US Small-Cap Stocks
   - International Developed Market Stocks
   - Emerging Market Stocks
   - US Government Bonds
   - Corporate Bonds
   - Real Estate (REITs)
   - Gold
   - Commodities (broad basket)
2. The tool displays a correlation matrix showing how each asset pair has moved together historically (-1.0 to +1.0):
   - **+0.8 to +1.0:** Very high correlation (move together very closely)
   - **+0.5 to +0.8:** Moderate-high correlation (usually move together)
   - **+0.2 to +0.5:** Low-moderate correlation (some relationship)
   - **-0.2 to +0.2:** Very low/no correlation (independent movement)
   - **-0.5 to -0.2:** Low-moderate negative correlation
   - **-1.0 to -0.5:** Moderate-high negative correlation (tend to move oppositely)
3. Analyze the matrix to answer:
   - Which two assets have the **highest positive correlation**? (move most closely together)
   - Which two assets have the **lowest or negative correlation**? (move most independently or oppositely)
   - What's the correlation between **US stocks and US government bonds**? What does this mean for portfolio risk?
   - What's the correlation between **US large-cap and international developed markets**? Would combining them provide significant diversification?
4. **Scenario Testing:**
   - Build Portfolio A: 100% US Large-Cap Stocks
   - Build Portfolio B: 50% US Large-Cap, 50% US Government Bonds
   - Build Portfolio C: 40% US Large-Cap, 20% International, 20% Bonds, 10% Real Estate, 10% Gold
   - The tool simulates each portfolio through historical market periods and shows:
     - Maximum drawdown (largest peak-to-valley loss)
     - Volatility (standard deviation of returns)
     - Average annual return
5. Compare the three portfolios:
   - Which had the lowest maximum drawdown?
   - Which had the lowest volatility?
   - Did diversification significantly reduce risk compared to holding only stocks?
6. **Challenge:** Create a fourth portfolio that minimizes volatility while maintaining at least 7% average annual return. What combination achieves this?

**Time Allocation:**
- Examine correlation matrix and answer questions: 5 minutes
- Build and test three portfolios: 5 minutes
- Create optimized portfolio challenge: 2 minutes
- Brief partner discussion on findings: 1 minute

---

### Activity 2: Age-Based Allocation Strategy Builder (15 minutes)

**Objective:** Design appropriate asset allocations for investors at different life stages

**Instructions:**
1. Using the Asset Allocation Optimizer, you'll create portfolios for three investors at different ages:
   - **Investor 1 - Maya (Age 25):** Recent college grad, $400/month to invest, retirement age 65 goal
   - **Investor 2 - David (Age 45):** Mid-career professional, $800/month to invest, retirement age 67 goal
   - **Investor 3 - Patricia (Age 60):** Planning to retire in 7 years, $500/month to invest, needs income starting at 67
2. For each investor, determine an appropriate asset allocation considering:
   - **Time horizon:** Years until retirement
   - **Risk capacity:** Ability to recover from losses based on time available
   - **Income needs:** When they'll need to withdraw money
3. Build allocations by selecting percentages across:
   - **US Stocks** (Large-Cap, Small-Cap)
   - **International Stocks** (Developed Markets, Emerging Markets)
   - **Bonds** (Government, Corporate)
   - **Real Estate** (REITs)
   - **Cash/Stable Value**
4. The tool provides guidance:
   - **Suggested stock allocation:** "120 minus age" rule (120 - 25 = 95% stocks for Maya)
   - **Risk assessment:** Shows potential maximum drawdown and volatility for your allocation
   - **Expected returns:** Projects average annual return based on historical data
5. For each investor, create an allocation and the tool will project:
   - Total wealth at retirement age
   - Maximum loss they might experience during market crashes
   - Required recovery time after worst-case crash
6. **Analysis Questions:**
   - Why can Maya tolerate 90% stocks while Patricia should only hold 35-40%?
   - If David uses an overly conservative allocation (40% stocks), how much potential wealth does he sacrifice by retirement?
   - If Patricia uses an overly aggressive allocation (80% stocks), what risk does she face if a market crash happens at age 65-66?
7. **Real-World Application:**
   - If you're currently 18-20 years old and started investing $200/month, what allocation would you choose?
   - How would you adjust this allocation when you reach age 35? Age 50? Age 65?

**Time Allocation:**
- Review three investor profiles: 2 minutes
- Build allocation for Investor 1 (Maya): 4 minutes
- Build allocation for Investor 2 (David): 4 minutes
- Build allocation for Investor 3 (Patricia): 4 minutes
- Answer analysis questions: 1 minute

---

### Activity 3: Market Crisis Survival Simulation (14 minutes)

**Objective:** Experience how diversification protects wealth during market downturns

**Instructions:**
1. Using the Portfolio Diversification Builder, you'll build two contrasting portfolios and see how they perform through a simulated market crisis:
   - **Portfolio A - Concentrated:** 100% in one asset class (your choice: all stocks, all bonds, or all in one sector)
   - **Portfolio B - Diversified:** Spread across multiple asset classes using allocation principles from Day 1
2. Each portfolio starts with $50,000
3. The simulation runs through a **Major Market Crisis** scenario:
   - **Month 1-3:** Market decline begins, stocks drop 15%, bonds hold steady
   - **Month 4-6:** Crisis deepens, stocks drop another 20% (total -32% from start), bonds rise 5%
   - **Month 7-9:** Panic peak, stocks drop another 15% (total -41% from start), emerging markets down 50%, gold up 15%, bonds up another 3%
   - **Month 10-18:** Recovery begins, stocks rise 25% from bottom, bonds give back some gains
   - **Month 19-30:** Bull market, stocks rise another 35%, back to new highs
4. Watch the simulation and record:
   - **Maximum Loss:** Lowest portfolio value during the crisis
   - **Recovery Time:** Months until portfolio returns to starting $50,000
   - **Final Value:** Portfolio value at month 30
5. The simulation allows you to make decisions at key points:
   - **During the crash (Month 9):** Do you:
     - Panic sell everything to cash (locking in losses)?
     - Hold steady and do nothing?
     - Rebalance (sell bonds which held up, buy stocks on sale)?
   - **During recovery (Month 15):** Do you:
     - Start taking profits on stocks?
     - Continue holding or rebalancing?
     - Add new contributions?
6. Compare outcomes:
   - How much did Portfolio A (concentrated) lose at the worst point?
   - How much did Portfolio B (diversified) lose at the worst point?
   - Which recovered faster?
   - If you made panicked decisions (selling at the bottom), how much permanent wealth did you destroy?
   - If you rebalanced during the crisis (selling bonds, buying stocks), what was your final outcome?
7. **Reflection:**
   - Could you emotionally handle watching a concentrated portfolio drop 40-50%?
   - How did diversification change your max loss and recovery time?
   - What role did rebalancing play in the final outcome?

**Time Allocation:**
- Build Portfolio A (Concentrated): 2 minutes
- Build Portfolio B (Diversified): 3 minutes
- Run crisis simulation and make decisions: 6 minutes
- Compare outcomes and reflect: 3 minutes

---

### Activity 4: Rebalancing Practice Lab (8 minutes)

**Objective:** Practice rebalancing portfolios to maintain target allocations

**Instructions:**
1. Using the Rebalancing Simulator, you'll manage a portfolio over 10 years with annual rebalancing decisions
2. **Starting Portfolio:** $100,000 with 70/30 stock/bond target allocation
   - $70,000 in stock index fund
   - $30,000 in bond index fund
3. Each year, the tool shows:
   - How stocks and bonds performed (different returns each year)
   - Current portfolio values and allocation percentages
   - How far your allocation has drifted from the 70/30 target
4. You must decide:
   - **Rebalance:** Sell some of whichever grew more, buy more of what lagged, to restore 70/30
   - **Don't Rebalance:** Let the portfolio drift, accepting whatever allocation results
5. The simulation shows three parallel universes:
   - **Your Decisions:** The path based on your rebalancing choices
   - **Always Rebalance:** What happens if you rebalance every year without fail
   - **Never Rebalance:** What happens if you never rebalance once
6. Key decision year examples:
   - **Year 3:** Stocks have surged 65% total since start while bonds gained 12%. Your portfolio is now 78% stocks / 22% bonds. Do you rebalance?
   - **Year 7:** Stocks crashed 35% last year while bonds rose 8%. Your portfolio is now 58% stocks / 42% bonds. Do you rebalance?
7. At the end of 10 years, compare:
   - Final value of each strategy (Your Decisions vs. Always Rebalance vs. Never Rebalance)
   - Maximum drawdown (worst loss) experienced by each
   - How far allocation drifted in the "Never Rebalance" scenario
8. **Analysis:**
   - Did annual rebalancing improve returns, reduce risk, or both?
   - Was it harder to rebalance after stocks surged (selling winners) or after stocks crashed (buying losers)?
   - What allocation did the "Never Rebalance" portfolio end up with? Was it riskier than intended?
9. **Real-World Application:**
   - Set a personal rule: "I will rebalance my portfolio [annually / when allocation drifts 5+ percentage points] to maintain my target allocation."

**Time Allocation:**
- Review starting portfolio and rules: 1 minute
- Make rebalancing decisions for 10 simulated years: 5 minutes
- Compare three strategies and analyze results: 2 minutes

---

## Reflection & Wrap-up (5 minutes)

**Group Discussion Questions:**
1. What was the most surprising insight about diversification from today's activities?
2. After experiencing the market crisis simulation, how confident do you feel about staying invested during real crashes?
3. What asset allocation strategy will you use when you start investing (or if you already are)?
4. What's your personal rebalancing commitment? How often and under what conditions?

**Individual Reflection:**
Take 2 minutes to write responses to:
- One thing I learned about portfolio diversification that I didn't fully understand before
- One specific allocation or rebalancing strategy I will use in my future investing
- One action I'll take in the next 30 days related to portfolio diversification

## Key Takeaways

By the end of this learning lab, you should be able to:

1. **Analyze Correlation:** Identify which assets move together and which move independently, understanding that combining low-correlation assets reduces portfolio volatility

2. **Design Age-Appropriate Allocations:** Create suitable stock/bond allocations for different life stages, understanding why young investors can accept more risk while older investors need more stability

3. **Build Diversified Portfolios:** Construct portfolios spread across multiple asset classes, avoiding concentration risk while capturing growth across different markets

4. **Apply Rebalancing Discipline:** Restore portfolios to target allocations periodically, mechanically "buying low and selling high" without emotional decision-making

5. **Evaluate Risk-Return Tradeoffs:** Balance the desire for high returns with the need for manageable risk, finding the optimal point on the efficient frontier for your situation

6. **Survive Market Crises:** Understand that diversified portfolios reduce crashes from devastating to manageable, and that rebalancing during crises positions you for recovery

7. **Implement Systematic Strategies:** Commit to evidence-based allocation and rebalancing approaches rather than reacting emotionally to market swings

The portfolio diversification skills practiced today—correlation analysis, age-based allocation, crisis management, and disciplined rebalancing—are the foundation of successful long-term investing. These aren't theoretical concepts; they're practical tools that separate investors who build wealth steadily from those who experience boom-bust cycles and panic-driven mistakes. Every dollar you invest over your lifetime will benefit from the diversification principles practiced in this learning lab.

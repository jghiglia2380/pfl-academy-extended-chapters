# L-67 Assets: Investment Technology and Behavioral Investing

## Overview

This chapter requires five primary interactive tools and five corresponding printable PDF alternatives to support both Day 1 conceptual learning and Day 2 hands-on application. All tools are platform-agnostic (no state variables required) and focus on universal investment technology features and behavioral psychology principles. Each interactive tool has a printable PDF alternative for accessibility and technology equity.

---

## Day 1 Assets

### 1. Investment Platform Evaluator (Primary Skill Builder)

**Purpose:**
Enable students to compare different investment technology platforms (robo-advisors, online brokerages, investment apps) across multiple investor profiles, understanding how platform features, costs, and suitability vary based on individual circumstances.

**Format:**
Interactive web-based comparison tool with multi-profile selector, side-by-side platform comparison matrix, cost calculator, and recommendation engine.

**Inputs:**

1. **Investor Profile Selection:**
   - Dropdown menu with 4 pre-configured profiles:
     - Beginner with $500 (22-year-old, first job, knows nothing about investing)
     - DIY Enthusiast with $10,000 (28-year-old, enjoys research, wants control)
     - Busy Professional with $50,000 (35-year-old, wants solid returns without time investment)
     - Experienced Investor with $100,000 (45-year-old, managing retirement savings)
   - Option to create custom profile with manual inputs

2. **Custom Profile Inputs (if selected):**
   - Initial investment amount ($0-$500,000)
   - Monthly contribution ($0-$5,000)
   - Investment knowledge level (Beginner/Intermediate/Advanced)
   - Time available for investing (None/Minimal/Moderate/Extensive)
   - Primary goal (Retirement/Home purchase/General wealth/Other)
   - Risk tolerance (Conservative/Moderate/Aggressive)
   - Interest in stock picking (Yes/No)

3. **Platform Selection:**
   - Multi-select checkboxes to choose 2-4 platforms from:
     - **Robo-advisors:** Betterment, Wealthfront, Vanguard Digital Advisor, SoFi Automated, Schwab Intelligent
     - **Online Brokerages:** Fidelity, Charles Schwab, Vanguard, E*TRADE, TD Ameritrade
     - **Investment Apps:** Robinhood, Acorns, Stash, Public, M1 Finance

4. **Time Horizon Selection:**
   - Radio buttons: 10 years / 20 years / 30 years / 40 years
   - Affects cost projection calculations

**Expected Outputs:**

1. **Platform Comparison Matrix:**
   ```
   Feature              | Platform A    | Platform B      | Platform C
   ---------------------|---------------|-----------------|----------------
   Platform Type        | Robo-advisor  | Online Brokerage| Investment App
   Annual Advisory Fee  | 0.25%         | 0%              | $3/month
   Underlying Fund Fees | 0.08%         | 0.05%           | 0.12%
   Total Annual Cost    | 0.33%         | 0.05%           | Varies*
   Minimum to Start     | $0            | $0              | $0
   Auto-Rebalancing     | ✓ Yes         | ✗ Manual        | ✓ Yes
   Tax-Loss Harvesting  | ✓ ($10k+)     | ✗ Manual        | ✗ No
   Investment Choice    | Algorithm     | Full Control    | Pre-built pies
   Research Tools       | Basic         | Extensive       | Minimal
   Fractional Shares    | ✓ Yes         | ✓ Yes           | ✓ Yes
   Human Advisor        | Premium tier  | Available       | ✗ No
   Mobile App Quality   | Excellent     | Good            | Excellent
   Educational Content  | Strong        | Excellent       | Moderate
   Suitability Score    | 9/10          | 6/10            | 7/10
   ```

2. **Cost Analysis Table:**
   ```
   Platform      | Annual Cost Year 1 | 10-Year Total | 30-Year Total
   --------------|--------------------|--------------|--------------
   Betterment    | $33               | $1,847       | $14,203
   Fidelity DIY  | $10               | $856         | $5,421
   Acorns        | $36               | $2,124       | $6,892**

   *Assumes 7% annual return, initial $10,000 + $200/month
   **Subscription fee becomes smaller % as balance grows
   ```

3. **Visual Outputs:**
   - **Cost Comparison Bar Chart:** 30-year total fees side-by-side
   - **Feature Availability Matrix:** Color-coded (green = has, red = doesn't have, yellow = partial)
   - **Suitability Radar Chart:** Shows fit across dimensions (cost, ease, features, control, education)
   - **Growth Projection Line Graph:** Account value over time after fees for each platform

4. **Recommendation Engine:**
   ```
   BEST FIT FOR THIS PROFILE:

   PRIMARY RECOMMENDATION: Betterment
   Reasoning:
   - Hands-off approach matches "minimal time available"
   - Automatic rebalancing and tax-loss harvesting add value
   - 0.25% fee reasonable for $50,000+ balance
   - Strong educational content supports learning

   RUNNER-UP: Fidelity
   Reasoning:
   - Lowest cost option (0.05% total)
   - Would save ~$8,700 over 30 years vs. Betterment
   - But requires manual rebalancing and tax management
   - Better IF investor willing to spend 2-3 hours/year managing

   NOT RECOMMENDED: Acorns
   Reasoning:
   - Subscription fee too expensive for this balance size
   - Limited features vs. alternatives
   - Better suited for micro-investors with <$5,000
   ```

5. **Trade-Off Analysis:**
   - "You'll pay approximately $8,700 more in fees over 30 years with Betterment vs. Fidelity DIY"
   - "If Betterment's automation prevents one panic-sell during a market crash, it could save 10-20× the fee difference"
   - "Break-even analysis: If you value your time at $30/hour, Betterment saves ~$1,500 in time value over 30 years"

**Interaction Model:**

1. User selects investor profile from dropdown → Platform data and suitability scores auto-calculate
2. User selects 2-4 platforms to compare → Comparison matrix populates
3. User adjusts time horizon slider → Cost projections update in real-time
4. User clicks on any platform name → Detailed feature breakdown expands
5. User clicks "Why this recommendation?" → Reasoning panel displays
6. User toggles priority sliders (cost vs. features vs. ease) → Recommendation recalculates
7. User clicks "Save Comparison" → Generates shareable summary
8. User clicks "Print Report" → Creates formatted PDF with all comparisons and rationale

**Design Notes:**

- **Responsive Design:** Must work seamlessly on mobile, tablet, desktop
- **Real-Time Updates:** All calculations update instantly as inputs change
- **Data Currency:** Platform fees and features should be updated quarterly (maintenance requirement)
- **Visual Hierarchy:**
  - Large, clear platform names with logos
  - Color coding: Robo-advisors (blue), Brokerages (green), Apps (purple)
  - Cost differences highlighted in red/green (higher/lower than average)
  - Suitability scores use 10-point scale with visual stars
- **Accessibility:**
  - Screen reader compatible with ARIA labels
  - Keyboard navigation support (tab through platforms)
  - High contrast mode toggle
  - Font size adjustable (+/- buttons)
  - Alt text for all charts and graphs
- **Error Handling:**
  - Validate numeric inputs (no negatives, reasonable ranges)
  - Warn if inputs seem unrealistic ("$500,000 monthly contribution seems high. Verify?")
  - Graceful degradation if platform data unavailable ("Data currently unavailable for this platform")
  - Save user work if browser crashes (localStorage)
- **User Experience:**
  - Tooltips on hover for all features (explain "tax-loss harvesting," "expense ratio," etc.)
  - Comparison limited to 4 platforms maximum (avoid overwhelming users)
  - "Reset to Defaults" button to clear custom inputs
  - Progress indicator showing "2 of 4 platforms selected"

**Technical Specifications:**

```javascript
// Platform data structure
const platformData = {
  betterment: {
    name: "Betterment",
    type: "robo-advisor",
    advisory_fee: 0.0025,  // 0.25%
    fund_expense_ratio: 0.0008,  // 0.08% average
    minimum_investment: 0,
    features: {
      auto_rebalancing: true,
      tax_loss_harvesting: { available: true, minimum: 10000 },
      investment_choice: "algorithm-selected",
      research_tools: "basic",
      fractional_shares: true,
      human_advisor: "premium",
      mobile_app: "excellent",
      educational_content: "strong"
    },
    suitability_scores: {
      beginner_500: 8,
      diy_10000: 5,
      busy_50000: 9,
      experienced_100000: 7
    }
  },
  // ... similar structures for other platforms
};

// Cost calculation function
function calculateTotalCost(platform, initialAmount, monthlyContribution, years, annualReturn = 0.07) {
  let balance = initialAmount;
  let totalFees = 0;

  for (let year = 0; year < years; year++) {
    // Add monthly contributions
    for (let month = 0; month < 12; month++) {
      balance += monthlyContribution;
      balance *= (1 + annualReturn / 12);
    }

    // Calculate and subtract fees
    const annualFee = balance * (platform.advisory_fee + platform.fund_expense_ratio);
    totalFees += annualFee;
    balance -= annualFee;
  }

  return {
    finalBalance: balance,
    totalFees: totalFees,
    feePercentage: (totalFees / (initialAmount + monthlyContribution * 12 * years)) * 100
  };
}

// Suitability scoring algorithm
function calculateSuitability(platform, profile) {
  let score = 5; // Start at neutral

  // Adjust based on experience level
  if (profile.experience === "beginner" && platform.type === "robo-advisor") score += 2;
  if (profile.experience === "advanced" && platform.type === "brokerage") score += 2;

  // Adjust based on time available
  if (profile.time_available === "none" && platform.features.auto_rebalancing) score += 1;
  if (profile.time_available === "extensive" && platform.features.research_tools === "extensive") score += 1;

  // Adjust based on account size and fees
  if (profile.balance < 5000 && platform.subscription_fee) score -= 2;
  if (profile.balance > 100000 && platform.advisory_fee > 0.003) score -= 1;

  // Cap at 10, floor at 1
  return Math.max(1, Math.min(10, score));
}
```

---

## Day 2 Assets

### 2. Behavioral Bias Self-Assessment Tool

**Purpose:**
Help students identify their personal susceptibility to four major behavioral biases (loss aversion, recency bias, confirmation bias, herd mentality) through scenario-based questions with immediate feedback and personalized risk profile.

**Format:**
Interactive quiz with 10 scenario-based questions, instant scoring, detailed results breakdown, and personalized bias risk profile with mitigation strategies.

**Inputs:**

1. **10 Scenario-Based Questions:**

Each question presents a realistic investing scenario with 4 answer choices designed to reveal bias tendencies.

**Example Question 1 (Loss Aversion):**
```
You bought Stock A at $100/share. It's now worth $70/share.
At the same time, Stock B (which you don't own) has dropped from $100 to $70,
and analysts say both stocks have equal prospects for recovery.

What would you most likely do?

A) Hold Stock A (hoping it recovers to break even) but not buy Stock B
B) Sell Stock A and buy Stock B instead (both at $70, same prospects)
C) Hold Stock A AND buy Stock B (both good opportunities at current price)
D) Sell Stock A to cut losses, and don't buy Stock B

[This tests: Loss aversion - treating owned stocks differently than non-owned stocks
even with identical prospects]
```

**Example Question 2 (Recency Bias):**
```
The stock market has risen 20% per year for the past 3 years. Your investment
account has grown nicely. A friend suggests you should invest more aggressively
to take advantage of the strong market.

How do you react?

A) Invest more - the market momentum will likely continue
B) Stay with current strategy - past performance doesn't predict future
C) Actually reduce stock exposure - what goes up often comes down
D) Ask professional advice before changing anything

[This tests: Recency bias - assuming recent trends will continue indefinitely]
```

**Example Question 3 (Confirmation Bias):**
```
You invested in a clean energy company because you believe in sustainability.
Recent news:
- Positive article: "Clean energy is the future" (general industry)
- Negative article: "Your company loses major contract, profit margins declining"

Which do you pay more attention to?

A) The positive article - it confirms the industry is growing
B) Both equally - I want full information
C) The negative article - company-specific bad news concerns me
D) Neither - I'll wait for next earnings report

[This tests: Confirmation bias - seeking information that confirms existing beliefs]
```

**Example Question 4 (Herd Mentality):**
```
A cryptocurrency has skyrocketed 400% this year. All your friends are talking
about it, financial media covers it constantly, and your Uber driver just told
you he's investing in it.

What's your reaction?

A) I should invest too - everyone can't be wrong
B) Interesting, but I'll research carefully before considering it
C) This sounds like a bubble - I'll avoid it
D) I'll invest a small amount just in case it keeps rising

[This tests: Herd mentality - following the crowd vs. independent thinking]
```

2. **Demographic Questions (Optional):**
   - Age range
   - Investing experience (None/Beginner/Intermediate/Advanced)
   - Risk tolerance (Conservative/Moderate/Aggressive)
   - Used to personalize feedback

**Expected Outputs:**

1. **Overall Bias Risk Profile:**
   ```
   YOUR BEHAVIORAL PROFILE

   Loss Aversion:     ████████░░ HIGH (8/10)
   Recency Bias:      █████░░░░░ MODERATE (5/10)
   Confirmation Bias: ██████░░░░ MODERATE (6/10)
   Herd Mentality:    ███░░░░░░░ LOW (3/10)

   Overall Risk Level: MODERATE-HIGH
   You show strong loss aversion tendencies with moderate confirmation bias.
   These are your primary investing risks.
   ```

2. **Detailed Bias Analysis:**

For each bias, provide:

```
LOSS AVERSION - HIGH RISK (8/10)

What This Means:
You tend to feel losses more intensely than equivalent gains, causing you to:
- Hold losing investments too long (hoping to break even)
- Sell winning investments too quickly (to "lock in" gains)
- Make decisions based on purchase price rather than current prospects
- Avoid risk after experiencing losses

Why This Matters:
Research shows investors hold losing stocks an average of 124 days while
selling winners after just 104 days - exactly backward from optimal strategy.
This bias can cost you thousands in unrealized gains over time.

Real-World Example:
You bought Stock A at $50. It's now $30. You hold it because selling would
"make the loss real." Meanwhile, a better investment opportunity passes by
because your money is trapped in the loser.

Your Antidote Strategies:
1. Set stop-loss rules BEFORE buying: "If any stock drops 20%, I automatically
   re-evaluate with fresh eyes as if deciding whether to buy it today."
2. Evaluate investments based on current prospects, not purchase price
3. Ask: "If I didn't already own this, would I buy it today at current price?"
4. Track what you could have earned elsewhere (opportunity cost)
```

3. **Comparison to Average Investor:**
   ```
   YOU vs. AVERAGE INVESTOR

   Loss Aversion:     You: 8/10  │  Average: 7/10  [Slightly Higher ↑]
   Recency Bias:      You: 5/10  │  Average: 6/10  [Slightly Lower ↓]
   Confirmation Bias: You: 6/10  │  Average: 6/10  [Same →]
   Herd Mentality:    You: 3/10  │  Average: 5/10  [Much Lower ↓↓]

   Your Strength: You're less susceptible to herd mentality than most people.
                  This protects you during market manias and bubbles.

   Your Weakness: Higher loss aversion means you need strong rules to prevent
                  holding losers too long and selling winners too early.
   ```

4. **Personalized Action Plan:**
   ```
   YOUR TOP 3 PRIORITY RULES

   Based on your bias profile, these rules will protect you most:

   1. LOSS AVERSION COUNTER:
      "If any investment drops 25%, I will re-evaluate with fresh eyes as if
      I were deciding whether to buy it today at the current price."

   2. CONFIRMATION BIAS COUNTER:
      "Before making any investment change, I will actively seek and read
      at least one article that disagrees with my view."

   3. GENERAL PROTECTION:
      "I will review my written investment plan before making ANY change
      to my portfolio. No emotional decisions."
   ```

5. **Visual Outputs:**
   - Radar chart showing bias scores across four dimensions
   - Percentile ranking vs. other students/users
   - Risk level indicator (Low/Moderate/High) with color coding
   - Suggested reading and resources based on highest-risk biases

**Interaction Model:**

1. User starts quiz → Questions presented one at a time
2. User selects answer → Immediate visual confirmation (no right/wrong shown yet)
3. User completes all 10 questions → Progress bar shows completion
4. User clicks "Get Results" → Scoring calculation runs
5. Results display with animated charts → Bias scores reveal progressively
6. User clicks on any bias name → Detailed explanation expands
7. User clicks "Why did I score this way?" → Shows their specific answers that contributed to score
8. User clicks "Download Report" → PDF with full results and strategies
9. User clicks "Share Anonymously" → Adds their data to class/aggregate comparison (optional)

**Design Notes:**

- **No Judgment:** Emphasize biases are normal, not personality flaws
- **Privacy:** Assure students results are private unless they choose to share
- **Accuracy:** Questions validated against behavioral economics research
- **Engagement:** Use relatable scenarios, not abstract theory
- **Actionable:** Every bias includes specific counter-strategies
- **Visual:** Charts and graphs make abstract concepts concrete
- **Progressive Disclosure:** Start with summary, allow drilling into details
- **Positive Framing:** Highlight strengths (low herd mentality) not just weaknesses

**Scoring Algorithm:**

```javascript
const biasQuestions = {
  loss_aversion: [1, 5, 9],  // Question numbers that test this bias
  recency_bias: [2, 6, 10],
  confirmation_bias: [3, 7],
  herd_mentality: [4, 8]
};

const questionWeights = {
  // Each answer weighted by how strongly it indicates the bias
  question_1: {
    A: 3,  // Strong loss aversion (treating owned stock differently)
    B: 0,  // No bias (rational comparison)
    C: 0,  // No bias (rational opportunity assessment)
    D: 2   // Moderate loss aversion (avoiding further pain)
  },
  // ... similar for all questions
};

function calculateBiasScore(userAnswers, biasType) {
  const relevantQuestions = biasQuestions[biasType];
  let totalScore = 0;
  let maxPossible = relevantQuestions.length * 3;  // Max 3 points per question

  relevantQuestions.forEach(qNum => {
    const userAnswer = userAnswers[qNum];
    totalScore += questionWeights[`question_${qNum}`][userAnswer];
  });

  // Convert to 10-point scale
  return Math.round((totalScore / maxPossible) * 10);
}
```

---

### 3. Investment Decision Simulator

**Purpose:**
Allow students to experience realistic investment scenarios that trigger behavioral biases, make decisions under pressure, and see outcomes based on their choices—learning through experiential simulation.

**Format:**
Interactive branching scenario simulator with three distinct scenarios (market crash, hot stock FOMO, confirmation trap), realistic market data, emotional feedback indicators, and outcome analysis.

**Inputs:**

1. **Scenario Selection:**
   - User chooses which scenario to run first (or tool presents sequentially)
   - Scenarios: Market Crash / Hot Stock / Confirmation Trap

2. **User Decisions at Key Choice Points:**

Each scenario has 2-4 decision points where users choose actions.

**Scenario A: The Market Crash**

**Setup:**
- User starts with $10,000 portfolio (60% stocks, 40% bonds)
- Market context shown: "Strong bull market for 3 years, your portfolio up 25%"

**Month 1 Decision Point:**
```
MARKET UPDATE: Down 8% in one month

Headlines streaming:
- "Worst month in 5 years"
- "Analysts predict continued volatility"
- "Should you get out now?"

Your portfolio: $10,000 → $9,520

What do you do?
A) Sell everything to cash - stop the bleeding
B) Sell stocks, keep bonds - reduce risk
C) Hold steady - stick to the plan
D) Buy more stocks - they're on sale

[User selects, sees immediate psychological feedback]
```

**Month 2 Decision Point:**
```
MARKET UPDATE: Down another 12%

Headlines:
- "Market enters correction territory"
- "Investors flee to safety"
- "Is this the big one?"

Your portfolio:
- If you held: $9,520 → $8,378 (down 16% total)
- If you sold in Month 1: $9,520 in cash (avoided drop)

Your decision?
[Same options as Month 1, but context different based on prior choice]
```

**Month 3-12 Resolution:**
```
MARKET UPDATE: Recovering...

Months 3-6: Market rises 6%, then 4%, then 5%, then 3%
Months 7-12: Continued recovery, ends year up 8% from Month 2 low

YOUR OUTCOME:
Path 1 (Held steady):     $10,000 → $8,378 → $10,754 (up 7.5% for year)
Path 2 (Sold in Month 1): $9,520 in cash (missed 14% recovery)
Path 3 (Bought in Month 2): $8,378 + bought more → $11,892 (up 18.9%)
Path 4 (Sold in Month 2): $8,378 in cash (missed 28% recovery)
```

**Scenario B: The Hot Stock**

**Setup:**
- User has $10,000 in diversified portfolio
- Portfolio has been growing steadily (8% this year)

**Decision Point:**
```
THE SITUATION:

Your friend: "Bro, I made 300% on this cryptocurrency! It's going to the moon!"

Social media: Everyone posting screenshots of gains
Financial media: "Is crypto the future of money?"
Your Uber driver: "I just invested my savings in Bitcoin"

The crypto in question has risen 400% this year.

Your current portfolio is boring but solid: up 8%, well-diversified.

What percentage of your portfolio do you invest in the hot crypto?

A) 0% - Stick to my plan, ignore the hype
B) 5% - Small speculative bet I can afford to lose
C) 20% - Significant allocation, don't want to miss out
D) 50%+ - Major reallocation, this is the opportunity

[User selects]
```

**Outcome Reveal:**
```
WHAT HAPPENED:

Historically, 95% of investments that experience 400% gains in one year
underperform the market over the next 5 years.

YOUR SCENARIO:
The crypto you considered rose another 50% over next 2 months (FOMO intensifies!)
Then crashed 80% over the following year.

YOUR OUTCOME:
Choice A (0%):    Portfolio continues steady growth: $10,000 → $11,469 (up 14.7%)
Choice B (5%):    Minor damage: $10,000 → $11,165 (up 11.7%, -$304 vs. plan)
Choice C (20%):   Significant damage: $10,000 → $9,987 (down 0.1%, -$1,482 vs. plan)
Choice D (50%+):  Devastating: $10,000 → $7,234 (down 27.7%, -$4,235 vs. plan)

LESSON: Herd mentality and FOMO drive people into assets near peak prices.
When your barber and Uber driver are giving investment tips, it's often
near the top of a bubble.
```

**Scenario C: The Confirmation Trap**

**Setup:**
- User invested $2,000 in clean energy company based on conviction
- 6 months later, stock is down 30% ($2,000 → $1,400)

**Decision Point:**
```
THE SITUATION:

You invested $2,000 in CleanPower Corp at $40/share because you believe
clean energy is the future. The stock is now $28/share (-30%).

RECENT NEWS:

Positive Article (general industry):
"Clean Energy Is The Future: Global Investment Surges"
- Industry growing 25% annually
- Government support increasing
- Long-term outlook strong

Negative Article (your specific company):
"CleanPower Corp Loses Major Contract"
- $50M contract cancelled by largest customer
- Profit margins declining from 15% to 8%
- Competitors gaining market share
- CEO sold personal shares

Which article do you focus on?

Your decision:
A) Ignore bad news, buy more - clean energy is the future!
B) Hold and hope - it will recover eventually
C) Sell half, reinvest in diversified clean energy ETF
D) Sell all, admit this specific company has problems

[User selects]
```

**Outcome Reveal with Analysis:**
```
WHAT HAPPENED:

The industry thesis was correct: Clean energy sector rose 28% over next year.

But your specific company continued struggling:
- Lost another major contract
- Stock dropped to $18/share (down 55% from your purchase)
- While sector competitors averaged +28%

ANALYSIS OF YOUR DECISION:

Choice A (Buy more): Lost $1,100 total (down 55%)
- Confirmation bias prevented objective evaluation
- You confused industry trends with company-specific problems
- Doubled down on a losing position

Choice B (Hold and hope): Lost $600 (down 30% while sector up 28%)
- Loss aversion kept you from selling
- Missed 58% relative to sector ETF

Choice C (Sell half, diversify): Broke even
- Sold $700 at $28, invested in ETF that grew to $896
- Kept $700 in stock, now worth $450
- Total: $1,346 (close to original $1,400, vs. $3,230 if fully in ETF)

Choice D (Sell all, diversify): Won $792 (up 56%)
- Sold $1,400 at $28, invested in clean energy ETF
- ETF grew 28%: $1,400 → $1,792
- Admitted mistake, preserved capital, stayed in sector

LESSON: Confirmation bias prevented you from seeing company-specific
problems separate from industry trends. The winning move was admitting
the specific company mistake while staying true to the clean energy thesis.
```

3. **Emotional State Indicators:**
   - Throughout scenarios, show emotional pressure gauge
   - "Stress level: HIGH - This is when mistakes happen"
   - "FOMO intensifying - Your brain wants to follow the crowd"
   - "Loss aversion triggered - Pain feels unbearable"

**Expected Outputs:**

1. **Decision Path Visualization:**
   - Flowchart showing user's choices and alternative paths
   - "You chose X. If you had chosen Y, outcome would be..."

2. **Bias Identification:**
   ```
   BIASES DETECTED IN YOUR DECISIONS:

   Scenario A (Market Crash):
   ✗ Sold in Month 1: Recency bias + Loss aversion
     (Recent drops felt permanent, couldn't tolerate pain)

   Scenario B (Hot Stock):
   ✗ Invested 20%: Herd mentality + FOMO
     (Everyone buying felt like validation, feared missing out)

   Scenario C (Confirmation):
   ✗ Held and hoped: Confirmation bias + Loss aversion
     (Focused on positive industry news, ignored company problems)
   ```

3. **Performance Scorecard:**
   ```
   YOUR PERFORMANCE:

   Decisions Made: 3 scenarios
   Optimal Decisions: 1 of 3
   Total Return: -8.3% (vs. +12.7% if optimal choices)
   Cost of Biases: $2,083 on $10,000 portfolio

   Primary Bias Pattern: Loss aversion leading to poor hold decisions
   ```

4. **Learning Insights:**
   ```
   WHAT YOU LEARNED:

   ✓ Market timing is extremely difficult - staying invested usually wins
   ✓ FOMO and herd mentality drive buying near peaks
   ✓ Confirmation bias prevents objective re-evaluation
   ✓ Emotional decisions made during stress usually underperform

   YOUR ACTION ITEMS:
   1. Create rule: "No selling during drops less than 30%"
   2. Create rule: "No buying trends until 72 hours after hearing about them"
   3. Create rule: "Actively seek contradicting evidence before any decision"
   ```

**Interaction Model:**

1. User enters simulator → Chooses scenario or starts with Scenario A
2. Context and setup display → User reads situation
3. Decision point appears → User selects from options
4. Emotional feedback shows → "Stress level HIGH, bias alert: Recency bias"
5. Next period unfolds → Based on user's decision
6. Additional decision points → User continues through scenario
7. Final outcome reveals → All paths shown (chosen and alternatives)
8. Bias analysis displays → Which biases influenced decisions
9. User clicks "Try again with different choices" → Can replay scenario
10. User clicks "Next scenario" → Moves to next simulation
11. After all scenarios → Summary performance scorecard
12. User clicks "Save Results" → Added to personal dashboard

**Design Notes:**

- **Realism:** Use actual market patterns and realistic price movements
- **Emotional Impact:** Create real stress through realistic scenarios
- **No Judgment:** Frame as learning opportunity, not test
- **Branching Complexity:** Show how different choices cascade into different outcomes
- **Visual Timeline:** Display market movements graphically, not just numbers
- **Comparison:** Always show "what if" alternatives to highlight decision impact
- **Replay Value:** Allow users to try different strategies
- **Educational:** Debrief each scenario with bias education

**Technical Specifications:**

```javascript
// Scenario data structure
const marketCrashScenario = {
  name: "Market Crash",
  initial_balance: 10000,
  initial_allocation: { stocks: 0.6, bonds: 0.4 },

  timeline: [
    {
      month: 1,
      market_change: -0.08,
      headlines: [
        "Worst month in 5 years",
        "Analysts predict continued volatility",
        "Should you get out now?"
      ],
      decision_prompt: "Your portfolio: $10,000 → $9,520. What do you do?",
      choices: [
        { id: "A", text: "Sell everything to cash", bias: ["loss_aversion", "recency_bias"] },
        { id: "B", text: "Sell stocks, keep bonds", bias: ["loss_aversion"] },
        { id: "C", text: "Hold steady", bias: [] },
        { id: "D", text: "Buy more stocks", bias: [], optimal: true }
      ]
    },
    // ... more timeline periods
  ],

  outcomes: {
    "C-C-C": { final_value: 10754, return: 0.0754, description: "Held steady throughout" },
    "A-A-A": { final_value: 9520, return: -0.0480, description: "Sold and stayed in cash" },
    "D-D-D": { final_value: 11892, return: 0.1892, description: "Bought during dips" },
    // ... all possible paths
  }
};

function calculateOutcome(userPath, scenario) {
  // userPath = ["C", "C", "C"] - user's choice at each decision point
  const pathKey = userPath.join("-");
  return scenario.outcomes[pathKey];
}

function identifyBiases(userChoices, scenario) {
  const biasesDetected = [];

  userChoices.forEach((choice, index) => {
    const decisionPoint = scenario.timeline[index];
    const choiceData = decisionPoint.choices.find(c => c.id === choice);

    if (choiceData.bias.length > 0) {
      biasesDetected.push({
        period: index + 1,
        choice: choiceData.text,
        biases: choiceData.bias
      });
    }
  });

  return biasesDetected;
}
```

---

### 4. Bias-Counter Rules Builder

**Purpose:**
Help students create specific, actionable, personalized investment rules that counter their identified behavioral biases and can be realistically followed when emotions run high.

**Format:**
Interactive rule creation wizard with templates, specificity checker, personal bias integration, and accountability features.

**Inputs:**

1. **Bias Profile Import:**
   - Automatically imports results from Behavioral Bias Self-Assessment
   - Highlights user's #1 and #2 highest-risk biases
   - Suggests rule categories based on bias profile

2. **Rule Category Selection:**
   ```
   Select rule categories to create (choose 3-5):

   □ BUYING RULES (Prevent buying high / FOMO)
   □ SELLING RULES (Prevent panic selling / loss locking)
   □ PORTFOLIO MAINTENANCE (Prevent drift / keep discipline)
   □ INFORMATION DIET (Prevent overreaction to news)
   □ DECISION PROCESS (Prevent emotional choices)
   □ ACCOUNT MONITORING (Prevent obsessive checking)
   ```

3. **Rule Template Selection:**

For each category, provide templates users can customize:

**Buying Rules Templates:**
```
Template 1: "I will invest $___ on [frequency] regardless of market conditions"
            (Dollar-cost averaging - counters recency bias & timing)

Template 2: "I will wait [time period] before investing in anything I heard
            about from social media or friends"
            (Waiting period - counters herd mentality & FOMO)

Template 3: "I will not invest in anything until I can explain why in writing"
            (Written rationale - counters impulse & poor research)

Template 4: "I will limit speculative investments to ___% of my portfolio"
            (Position sizing - limits damage from mistakes)

Template 5: "I will only buy when I've researched at least ___ opposing viewpoints"
            (Seek disagreement - counters confirmation bias)
```

**Selling Rules Templates:**
```
Template 1: "I will never sell based on a market drop of less than ___%"
            (Drop threshold - prevents panic selling from normal volatility)

Template 2: "I will wait ___ hours/days before acting on any urge to panic sell"
            (Cooling-off period - prevents emotional decisions)

Template 3: "I will re-evaluate losing investments based on fundamentals, not price"
            (Rational analysis - counters loss aversion & sunk cost)

Template 4: "I will ask: 'Would I buy this today?' before deciding to hold losers"
            (Fresh perspective - counters status quo bias)

Template 5: "I will never check my account during market hours"
            (Reduced monitoring - prevents reactionary trading)
```

**Portfolio Rules Templates:**
```
Template 1: "I will rebalance to target allocation every [quarterly/annually]"
            (Scheduled rebalancing - maintains discipline)

Template 2: "I will review my written investment plan before making ANY change"
            (Plan consultation - prevents impulse)

Template 3: "I will not make changes based on financial media headlines"
            (Ignore noise - prevents overreaction)

Template 4: "I will only invest money I won't need for ___ years"
            (Time horizon - prevents forced selling)
```

4. **Customization Fields:**

For each selected template, user fills in blanks:
- Dollar amounts
- Time periods
- Percentages
- Specific triggers

5. **Accountability Selection:**
```
Who will help you stick to these rules?

□ Share with accountability partner (friend/family member)
□ Set calendar reminders to review rules monthly
□ Print and post near workspace
□ Add to investment account profile
□ Join online community committed to disciplined investing
```

**Expected Outputs:**

1. **Personalized Rule Set:**

```
YOUR INVESTMENT RULES
Created: [Date]
Based on Behavioral Profile: High Loss Aversion, Moderate Confirmation Bias

═════════════════════════════════════════════════════════

BUYING RULES (Prevent FOMO & Poor Timing)

1. REGULAR INVESTING:
   "I will invest $200 on the 1st of every month regardless
   of market conditions, headlines, or recent performance."

   Why this matters for you: Counters recency bias (buying more
   when market is up, less when down). Automates behavior.

2. SOCIAL MEDIA COOLING-OFF:
   "I will wait 72 hours before investing in anything I first
   heard about from social media, friends, or water cooler talk."

   Why this matters for you: Counters herd mentality. Allows
   FOMO emotions to subside. Creates research period.

3. WRITTEN RATIONALE:
   "I will not invest in any individual stock until I can write
   a one-page explanation of why I'm buying, what could prove me
   wrong, and my sell criteria."

   Why this matters for you: Counters confirmation bias. Forces
   you to consider opposing viewpoints before committing.

═════════════════════════════════════════════════════════

SELLING RULES (Prevent Panic & Loss Locking)

4. NO PANIC SELLING:
   "I will never sell based on a market drop of less than 30%
   without waiting 7 days and re-reading this rule set."

   Why this matters for you: Counters loss aversion & recency bias.
   Normal market drops (10-20%) happen frequently. Prevents selling
   at bottoms when pain is highest.

5. FRESH EYES EVALUATION:
   "If any investment drops 25% from purchase price, I will
   re-evaluate it as if I were deciding whether to buy it TODAY
   at the CURRENT price, ignoring what I paid."

   Why this matters for you: Counters loss aversion. Purchase price
   is irrelevant to current prospects. Focuses on forward-looking
   analysis.

6. MONITORING LIMITS:
   "I will check my investment account no more than once per week,
   and NEVER during market hours or market crash periods."

   Why this matters for you: Reduces emotional reactions. Frequent
   checking increases stress and poor decisions.

═════════════════════════════════════════════════════════

PORTFOLIO MAINTENANCE RULES

7. SCHEDULED REBALANCING:
   "I will rebalance my portfolio back to target allocation
   (70% stocks / 30% bonds) every January 1st, regardless of
   market performance."

   Why this matters for you: Automatically sells high (winners that
   grew) and buys low (losers that declined). Mechanical discipline.

8. PLAN CONSULTATION:
   "I will review my written investment plan before making ANY
   change to my portfolio. No exceptions."

   Why this matters for you: Prevents emotional decisions. Your
   plan was made during calm rational moments, not stress.

═════════════════════════════════════════════════════════

DECISION PROCESS RULES

9. SEEK DISCONFIRMING EVIDENCE:
   "Before making any investment change, I will actively search
   for and read at least one article or analysis that disagrees
   with my view."

   Why this matters for you: Directly counters confirmation bias.
   Exposes you to perspectives you're naturally avoiding.

10. 48-HOUR RULE:
    "Any urge to make an unplanned portfolio change must wait
    48 hours. After 48 hours, if I still think it's the right
    move, I'll do it."

    Why this matters for you: Emotional decisions feel urgent but
    rarely are. Time reveals whether it's rational or reactionary.

═════════════════════════════════════════════════════════

COMMITMENT

I commit to following these rules for the next 12 months. I understand
they're designed to protect me from my identified behavioral biases,
especially loss aversion and confirmation bias.

I will review these rules monthly on the [1st] of each month.

Accountability partner: [Name]

Signed: _______________  Date: _______________
```

2. **Rule Strength Checker:**

For each rule, tool evaluates and scores:

```
RULE: "I will try not to panic sell during crashes"

Strength Assessment:
Specificity:    ⚠️  2/5 (Too vague - what's "panic"? what's "crash"?)
Actionability:  ⚠️  2/5 ("Try" isn't actionable - will you or won't you?)
Measurability:  ❌ 1/5 (Can't measure compliance)
Trigger:        ❌ 1/5 (No clear trigger defined)

Overall Score: 6/20 - NEEDS IMPROVEMENT

Suggestion:
"I will never sell based on a market drop of less than 30% without
waiting 7 days and consulting my investment plan."

New Assessment:
Specificity:    ✓  5/5 (Clear threshold: 30% drop)
Actionability:  ✓  5/5 (Clear action: don't sell, or wait 7 days)
Measurability:  ✓  5/5 (Can track: Did I follow this? Yes/No)
Trigger:        ✓  5/5 (Clear trigger: any drop approaching 30%)

Overall Score: 20/20 - STRONG RULE ✓
```

3. **Bias Coverage Analysis:**

```
BIAS PROTECTION COVERAGE

Your rules address:
✓ Loss Aversion:      5 rules (Strong coverage)
✓ Confirmation Bias:  2 rules (Moderate coverage)
✓ Recency Bias:       3 rules (Good coverage)
✓ Herd Mentality:     2 rules (Good coverage)

Gaps identified:
⚠️  No rule prevents overtrading (consider adding position size limits)
⚠️  No rule addresses information overload (consider limiting news consumption)
```

4. **Printable Commitment Card:**

Wallet-sized card that summarizes top 3 rules:

```
┌─────────────────────────────────────┐
│   MY INVESTMENT COMMITMENTS         │
├─────────────────────────────────────┤
│                                     │
│ 1. NEVER SELL ON DROPS <30%         │
│    Wait 7 days. Re-read plan.       │
│                                     │
│ 2. INVEST $200 MONTHLY              │
│    Every 1st, no matter what.       │
│                                     │
│ 3. WAIT 72 HOURS ON FOMO            │
│    Social media tips = research.    │
│                                     │
│ These rules protect me from:        │
│ • Panic selling (loss aversion)     │
│ • Buying high (FOMO/herd)           │
│ • Poor timing (recency bias)        │
│                                     │
│ Review monthly. Share with [Name].  │
│ Created: [Date]                     │
└─────────────────────────────────────┘
```

**Interaction Model:**

1. User's bias profile auto-loads → Top biases highlighted
2. User selects rule categories → Relevant templates appear
3. User chooses template → Customization fields activate
4. User fills in specifics → Rule strength checker evaluates in real-time
5. Tool suggests improvements → "Make this more specific by..."
6. User finalizes rule → Added to rule set
7. User repeats for 3-10 rules → Building complete rule system
8. Tool checks bias coverage → Identifies gaps, suggests additional rules
9. User reviews complete set → Can edit, reorder, or remove rules
10. User adds accountability → Selects partners, reminders
11. User commits → Signs and dates digitally
12. User downloads → Gets PDF, wallet card, and calendar file

**Design Notes:**

- **Guidance, Not Prescription:** Suggest but don't mandate rules
- **Personalization:** Tie every rule to user's specific bias profile
- **Realistic Standards:** Encourage 3-5 strong rules, not 20 weak ones
- **Quality Over Quantity:** Better to follow 3 rules perfectly than 10 poorly
- **Real-World Application:** Rules must be practically followable
- **Accountability Built In:** Social commitment increases adherence
- **Review Mechanism:** Calendar reminders to revisit rules monthly

---

### 5. Long-Term Cost Visualization Calculator

**Purpose:**
Demonstrate the compounding impact of investment fees over long time periods (10, 20, 30, 40 years) to help students understand why seemingly small percentage differences matter enormously.

**Format:**
Interactive calculator with visual growth projections, fee comparison charts, and breakeven analysis.

**Inputs:**

1. **Investment Parameters:**
   - Initial investment amount ($0-$500,000)
   - Monthly contribution ($0-$5,000)
   - Time horizon (slider: 10/20/30/40 years)
   - Expected annual return (default 7%, adjustable 4-10%)

2. **Platform Fee Comparison:**
   - Select 2-4 platforms to compare
   - Tool auto-populates fees for selected platforms
   - Option to enter custom fee percentages

**Expected Outputs:**

1. **Side-by-Side Comparison Table:**

```
SCENARIO: $500/month for 40 years at 7% annual return

Platform          | Fee   | Ending Value | Fees Paid | You Keep
------------------|-------|--------------|-----------|-------------
Platform A (0.50%)| 0.50% | $1,142,000   | $187,000  | $1,142,000
Platform B (0.25%)| 0.25% | $1,217,000   | $112,000  | $1,217,000
Platform C (0.10%)| 0.10% | $1,293,000   | $36,000   | $1,293,000
Platform D (0.03%)| 0.03% | $1,319,000   | $11,000   | $1,319,000

Total invested: $240,000
Difference (A vs. D): $177,000 kept with lowest fee option
```

2. **Visual Growth Chart:**

Line graph showing account value over time for each platform:
- X-axis: Years (0-40)
- Y-axis: Account value ($0-$1,500,000)
- Multiple lines (color-coded by platform)
- Gap between lines widens over time (compound effect visualization)
- Shaded area shows "money lost to fees"

3. **Fee Impact Breakdown:**

```
THE COST OF FEES OVER 40 YEARS

0.47% Fee Difference (0.50% vs. 0.03%)
└─ Costs you $177,000 over 40 years
   └─ That's $368/month in lost wealth
      └─ Or 74% of your monthly contribution amount!

Put differently:
• You contribute: $500/month for 40 years = $240,000
• Platform A (0.50% fee) fees eat: $187,000 (78% of your contributions!)
• Platform D (0.03% fee) fees eat: $11,000 (5% of your contributions)

The 0.47% difference compounds to $177,000.
```

4. **Breakeven Analysis:**

```
WHEN IS HIGHER FEE WORTH IT?

Platform A (0.50% robo-advisor) vs. Platform D (0.03% DIY index)

Fee difference: $177,000 over 40 years = $369/month average

Platform A provides:
✓ Automatic rebalancing (saves ~2 hours/year)
✓ Tax-loss harvesting (saves ~0.2% in taxes on large accounts)
✓ Behavioral protection (prevents panic selling)

BREAKEVEN CALCULATION:

Time saved: 2 hours/year × 40 years = 80 hours
Value at $50/hour: $4,000 total time value

Tax savings: ~0.2% on $600,000 average balance = $1,200/year × 40 = $48,000

Behavioral protection value:
If robo-advisor prevents ONE panic-sell during a crash (avoiding 15-20% loss),
that saves $150,000-$200,000 on a $1M portfolio.

VERDICT: The 0.50% fee can be worth it IF it prevents behavioral mistakes.
If you're disciplined and can avoid panic selling, DIY saves $177,000.
```

5. **Interactive "What If" Scenarios:**

```
WHAT IF YOU:

• Started 10 years earlier? (Same $500/month, 50 years total)
  Difference grows to $387,000 (0.50% vs. 0.03% fee)

• Doubled contributions? ($1,000/month instead of $500)
  Difference grows to $354,000 (fees scale with account size)

• Got 1% lower returns? (6% instead of 7% annual)
  Difference shrinks to $118,000 (but still significant)

• Started with $10,000? (Instead of $0)
  Difference grows to $201,000 (initial lump sum amplifies fees)
```

6. **Monthly Cost Visualization:**

```
FEES AS MONTHLY COST

Platform A (0.50% fee):
Year 1:  $3/month    Year 10: $38/month   Year 20: $95/month
Year 30: $211/month  Year 40: $475/month

Platform D (0.03% fee):
Year 1:  $0/month    Year 10: $2/month    Year 20: $6/month
Year 30: $13/month   Year 40: $28/month

In Year 40, you're paying $447/month MORE in fees with Platform A.
That's almost as much as your $500 monthly contribution!
```

**Interaction Model:**

1. User enters investment parameters → Tool calculates growth
2. User selects platforms to compare → Fee data auto-loads
3. Charts animate growth over time → Visual impact of compounding fees
4. User adjusts time horizon slider → All calculations update in real-time
5. User clicks "Show breakdown" → Detailed fee analysis expands
6. User clicks "What if?" scenarios → Explores sensitivity to assumptions
7. User clicks "Print comparison" → PDF report generates
8. User clicks "Save to profile" → Adds to personal investment dashboard

**Design Notes:**

- **Visual Impact:** Make fee differences visceral and concrete
- **Long-Term Focus:** Emphasize 30-40 year horizons (retirement reality)
- **Real Numbers:** Use realistic contribution amounts ($200-$1,000/month)
- **Nuance:** Show when higher fees might be worth it (behavioral protection)
- **Interactive:** Let users adjust all assumptions to explore
- **Educational:** Explain compound interest, not just show numbers

---

## Printable PDF Alternatives

All five interactive tools have printable alternatives for accessibility, technology failure backup, and student preference.

### 1. Platform Comparison Worksheet (PDF)

**Content:**
- Pre-filled comparison matrix for 3 platforms (Betterment, Fidelity, Robinhood)
- Blank rows for student notes and calculations
- Cost calculation template with formulas shown
- Decision matrix with scoring rubric
- Space for written justification of choice

**Format:** 2-page printable worksheet, black and white printer-friendly

---

### 2. Behavioral Bias Self-Assessment (Paper Quiz)

**Content:**
- 10 scenario-based questions with A/B/C/D answers
- Answer key with bias identification
- Scoring instructions and tables
- Interpretation guide for each bias level
- Action plan template

**Format:** 4-page booklet (fold 11x17 into 8.5x11 booklet)

---

### 3. Investment Decision Scenarios (Paper Branching)

**Content:**
- Three scenarios on separate pages
- "Choose Your Own Adventure" style branching
- "If you chose A, turn to page X" structure
- Outcome summaries for each path
- Bias identification checklist

**Format:** 6-page packet, one scenario per 2 pages

---

### 4. Investment Rules Builder Worksheet

**Content:**
- Rule templates pre-printed
- Fill-in-the-blank customization sections
- Rule strength self-assessment checklist
- Commitment card template to cut out
- Accountability partner agreement

**Format:** 3-page worksheet with perforated wallet card

---

### 5. Fee Impact Calculator (Excel Template Alternative)

**Content:**
- Pre-built Excel spreadsheet with formulas
- Input cells highlighted in yellow
- Automatic calculations for 4 platforms
- Chart templates that auto-populate
- Print-optimized layout

**Format:** Excel file (.xlsx) and PDF instructions

---

## Asset Development Priority

**High Priority (Must Build First):**
1. Investment Platform Evaluator (Day 1 primary skill builder)
2. Behavioral Bias Self-Assessment (Day 2 Activity 2, foundation for other activities)
3. Platform Comparison Worksheet PDF (backup for #1)

**Medium Priority (Build Next):**
4. Investment Decision Simulator (Day 2 Activity 3, high engagement value)
5. Bias-Counter Rules Builder (Day 2 Activity 4, capstone of learning)
6. Behavioral Quiz PDF (backup for #2)

**Lower Priority (Nice-to-Have):**
7. Long-Term Cost Visualization (simple calculator, can use Excel temporarily)
8. Decision Scenarios PDF (backup for #4)
9. Rules Builder Worksheet PDF (backup for #5)
10. Excel template for cost calculator

**All printable PDFs should be created** regardless of interactive tool priority, for accessibility compliance.

---

## Technical Implementation Notes

### Data Maintenance Requirements

**Quarterly Updates Needed:**
- Platform fees (check betterment.com, fidelity.com, etc.)
- Platform features (new offerings, discontinued services)
- Minimum investment requirements
- Fund expense ratios

**Annual Updates:**
- Market return assumptions (verify 7% is still reasonable)
- Platform availability (new platforms, mergers, closures)
- Behavioral research (new biases identified, refined scoring)

### Integration Points

**Between Tools:**
- Bias Assessment results should flow into Rules Builder
- Platform Evaluator comparisons can save to Decision Simulator
- Cost Calculator should reference platforms from Evaluator
- All tools share common platform database

**With Student Dashboard:**
- Save comparison results for later reference
- Track rule adherence over time
- Monitor bias assessment scores (if retaken)
- Link to external resources and readings

### Accessibility Compliance

**All tools must support:**
- Screen readers (ARIA labels, semantic HTML)
- Keyboard-only navigation (no mouse required)
- High contrast mode (WCAG AA minimum)
- Font size adjustment (+/- 200%)
- Alternative text for all charts/graphs
- Printable alternatives for technology equity

### Mobile Optimization

**Critical considerations:**
- Comparison matrices must be horizontally scrollable on phones
- Charts must be readable on small screens
- Touch targets minimum 44x44 pixels
- Input fields large enough for mobile keyboards
- Multi-step processes saved (prevent data loss on app switching)

---

## Assessment Integration

These assets support both formative and summative assessment:

**Formative:**
- Platform Evaluator: Check understanding of fee structures
- Bias Quiz: Immediate feedback on self-awareness
- Decision Simulator: Identify misconceptions in real-time
- Rules Builder: Verify specificity and actionability of rules

**Summative:**
- Save all tool outputs to student portfolio
- Generate comprehensive "Investment Readiness" report
- Track growth from pre-assessment to post-assessment
- Use for final project: "Personal Investment Plan"

---

**Total Assets:** 5 interactive tools + 5 printable PDF alternatives = 10 total assets

**Development Time Estimate:**
- Interactive tools: 40-60 hours (all five)
- Printable PDFs: 10-15 hours (all five)
- Total: 50-75 hours for complete asset package

**Student Engagement Time:**
- Day 1: ~12 minutes with Platform Evaluator
- Day 2: ~42 minutes across all four activities (plus 3 min visualization)
- Total: ~54 minutes of hands-on tool interaction

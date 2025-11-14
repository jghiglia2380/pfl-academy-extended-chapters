# L-62: Investment Portfolio Strategies - Assets Specification

## Day 1 Assets

### 1. Asset Allocation Visual Calculator
**Purpose:** Interactive tool showing how stock/bond splits affect risk and return

**Inputs:** Slider from 0-100% stocks
**Outputs:** Expected return, volatility range, historical worst year, best year

---

### 2. Lifecycle Allocation Comparison Chart
**Purpose:** Visual showing how allocation should evolve with age

**Format:** Line graph with age (20-80) on X-axis, stock % on Y-axis
**Shows:** Conservative, moderate, aggressive lifecycle paths

---

## Day 2 Assets (Learning Lab)

### 1. Advanced Portfolio Builder (Primary Skill Builder)

**Section A: Lifecycle Portfolio Constructor**
- Build portfolios for ages 25, 45, 60
- Select specific funds/ETFs from curated list
- Calculate projections over different time horizons
- Feedback on allocation appropriateness

**Section B: Historical Scenario Tester**
- Test portfolios through 2008 crisis, 2020 COVID, 1970s stagflation
- Calculate losses, recovery times, final outcomes
- Visual representation of portfolio resilience

**Section C: Rebalancing Simulator**
- Start with target allocation
- Simulate 5 years of uneven returns
- Compare rebalanced vs. non-rebalanced outcomes
- Calculate rebalancing benefit

**Section D: Tax Efficiency Optimizer**
- Given taxable + IRA accounts
- Test different asset location strategies
- Calculate 20-year after-tax wealth differences
- Recommend optimal location

**Section E: Investment Policy Statement Generator**
- Guided questionnaire
- Auto-generates personalized IPS with:
  - Target allocation
  - Specific fund selections
  - Rebalancing rules
  - Review schedule
  - Adjustment triggers
- Downloadable PDF document

---

### 2. Rebalancing Calculator
**Purpose:** Calculate exact buy/sell amounts to rebalance portfolio

**Inputs:**
- Current allocation ($ in each asset class)
- Target allocation (%)
- Rebalancing threshold (optional)

**Outputs:**
- How much to sell/buy of each asset
- Step-by-step instructions
- Tax impact estimate (if taxable account)

---

### 3. Asset Location Optimizer
**Purpose:** Determine which investments go in which account types

**Inputs:**
- Available accounts (401k, IRA, Roth, taxable)
- Investment holdings
- Target overall allocation

**Outputs:**
- Optimal placement: "Hold bonds in traditional IRA, stocks in Roth and taxable"
- Estimated annual tax savings
- 20-year projected benefit

---

### 4. Historical Return Database
**Purpose:** Research actual historical performance of different allocations

**Data:**
- Annual returns for stocks, bonds, cash (1926-present)
- Various allocation performance (100/0, 80/20, 60/40, etc.)
- Inflation data
- Best/worst years for each allocation

**Interactive Features:**
- Select time period
- Compare allocations
- Calculate what $10,000 invested in [year] would be worth today

---

## Printable Resources

### 1. Portfolio Planning Worksheet (2 pages)
- Goal identification
- Time horizon calculation
- Risk tolerance assessment
- Asset allocation determination
- Specific fund selection
- Rebalancing schedule

### 2. Investment Policy Statement Template (3 pages)
- Formal document template students can complete
- Sections: Goals, Allocation, Management Rules, Review Schedule
- Space for signatures/dates (makes it "official")

### 3. Asset Location Quick Reference (1 page)
- Table showing which investments belong in which account types
- Tax-inefficient → IRA/401k
- Tax-efficient → taxable or Roth
- Quick decision flowchart

### 4. Rebalancing Schedule Template (1 page)
- Calendar reminder template
- Tracking sheet for annual rebalancing
- Before/after allocation columns

### 5. Fund Selection Criteria Checklist (1 page)
- Low expenses (<0.20%)
- Broad diversification
- Reputable company
- Index vs. active considerations
- Top recommended funds by category

## Technical Requirements

**Calculations:**
- Compound interest with regular contributions
- Weighted portfolio returns
- Standard deviation for volatility
- Tax calculations (brackets, capital gains rates)
- Rebalancing amounts (algebraic solutions)

**Data Requirements:**
- Historical return data (stocks, bonds, inflation) 1926-present
- Current fund expense ratios (updated quarterly)
- Tax brackets (current year)
- Fund holdings for major ETFs/mutual funds

**User Experience:**
- Real-time recalculation as inputs change
- Visual charts (allocation pies, growth projections, historical performance)
- Save/export functionality
- Mobile-responsive design
- Print-optimized layouts

## Development Priority
1. Advanced Portfolio Builder (comprehensive primary tool)
2. Historical Return Database (critical for scenario testing)
3. Asset Location Optimizer
4. Printable Investment Policy Statement template
5. Rebalancing Calculator

# Asset Specifications for L-50: Supply and Demand in Personal Finance

## Day 1 Assets

### 1. Supply and Demand Curves Interactive Visualization
- **Purpose:** Help students understand how supply and demand curves work and interact
- **Format/Inputs:** Interactive web-based visualization
- **Expected Outputs:** Clear understanding of curve shapes, movements, and equilibrium
- **Interaction Model:** Drag sliders to adjust price, watch quantity change along curves
- **Design Notes:**
  - Two-panel display: Left panel shows demand curve, right shows supply curve
  - Central panel combines both to show equilibrium
  - Price slider (vertical): Drag to see quantity demanded and supplied at each price
  - Visual indicators:
    - At prices above equilibrium: Show surplus (distance between Qd and Qs)
    - At prices below equilibrium: Show shortage
    - At equilibrium: Highlight intersection point
  - Animated arrows showing price pressure (surplus → prices fall, shortage → prices rise)
  - Real-world example selector: Used cars, concert tickets, housing
  - Color coding: Demand curve (blue), Supply curve (red), Equilibrium (green)
  - Mobile-responsive with touch-friendly controls

### 2. Demand Shifters Interactive Tool
- **Purpose:** Demonstrate how non-price factors shift demand curves
- **Format/Inputs:** Interactive selector with visual curve shifts
- **Expected Outputs:** Understanding of what causes demand curves to move
- **Interaction Model:** Select factor, choose direction, see curve shift
- **Design Notes:**
  - **Factor Selector Buttons:**
    1. Income (increase/decrease)
    2. Price of Substitutes (increase/decrease)
    3. Price of Complements (increase/decrease)
    4. Tastes (favorable/unfavorable change)
    5. Expectations (future price up/down)
    6. Number of Buyers (increase/decrease)
  - **Visual Response:**
    - Original demand curve shown in blue
    - New demand curve appears in green (shift right) or orange (shift left)
    - Animation showing smooth transition
    - New equilibrium point highlighted
    - Price and quantity changes shown numerically
  - **Real-World Examples:**
    - Each factor includes 2-3 concrete examples
    - Example: "Income increases → Demand for restaurants shifts right"
  - **Quiz Mode:** Shows scenario, student predicts direction of shift, instant feedback
  - Responsive design for mobile/desktop

### 3. Supply Shifters Interactive Tool
- **Purpose:** Demonstrate how production factors shift supply curves
- **Format/Inputs:** Interactive selector with visual curve shifts
- **Expected Outputs:** Understanding of what causes supply curves to move
- **Interaction Model:** Select factor, choose direction, see curve shift
- **Design Notes:**
  - **Factor Selector Buttons:**
    1. Input Costs (increase/decrease)
    2. Technology (improve/worsen)
    3. Number of Sellers (increase/decrease)
    4. Expectations (future price up/down)
    5. Government Policy (tax/subsidy)
    6. Natural Events (positive/negative shock)
  - **Visual Response:**
    - Original supply curve in red
    - New supply curve in green (shift right) or orange (shift left)
    - Animated transition
    - New equilibrium highlighted
    - Price and quantity changes shown
  - **Real-World Examples:**
    - "Lumber prices rise → Supply of new homes shifts left"
    - "Automation improves → Supply of manufactured goods shifts right"
  - Pair with Demand Shifters tool for combined analysis
  - Mobile-responsive

### 4. Market Equilibrium Simulator
- **Purpose:** Show how markets self-adjust to equilibrium through surpluses and shortages
- **Format/Inputs:** Animated simulation with user controls
- **Expected Outputs:** Understanding of market clearing process
- **Interaction Model:** Set price above/below equilibrium, watch adjustment process
- **Design Notes:**
  - **Setup Phase:**
    - Display supply and demand curves
    - Show equilibrium price and quantity
  - **User Controls:**
    - "Set Price Above Equilibrium" button
    - "Set Price Below Equilibrium" button
    - Speed slider (slow motion to fast forward)
  - **Simulation:**
    - Above equilibrium: Show surplus inventory piling up, sellers lowering prices, convergence to equilibrium
    - Below equilibrium: Show customers competing for limited goods, prices rising, convergence
    - Animated arrows and annotations explaining forces
  - **Real-World Scenarios:**
    - Pandemic hand sanitizer (demand spike)
    - Housing shortage (supply constrained)
    - Black Friday sales (temporary price drop)
  - **Key Insight Display:** "Markets naturally move toward equilibrium through price adjustments"
  - Pause/play controls for classroom presentation
  - Step-through mode for detailed analysis

### 5. Pandemic Hand Sanitizer Case Study Interactive
- **Purpose:** Walk through the famous supply/demand shock example from COVID-19
- **Format/Inputs:** Multi-step interactive case study
- **Expected Outputs:** Deep understanding of how markets respond to shocks
- **Interaction Model:** Progress through timeline, see supply/demand shifts
- **Design Notes:**
  - **Timeline:**
    - **Feb 2020:** Normal market (D₀, S₀, P=$3)
    - **March 2020:** Pandemic hits (D shifts massively right, P spikes to $12-15)
    - **April 2020:** Supply responds (new entrants, S shifts right)
    - **May-June 2020:** New equilibrium (P falls to $4-5)
  - **Each Step Shows:**
    - Graph with curve positions
    - Price and quantity
    - Explanation of forces
    - Real photos/headlines from that period
  - **Interactive Elements:**
    - "What happens next?" prediction quiz
    - "Why did prices spike?" multiple choice
    - "How did market self-correct?" explanation
  - **Lessons Highlighted:**
    - High prices signal scarcity
    - Profit opportunities attract new supply
    - Markets self-adjust (though it takes time)
    - Price controls would have created worse shortages
  - Links to news articles and data from period
  - Downloadable as PDF case study

### 6. Movement vs. Shift Comparison Tool
- **Purpose:** Help students distinguish between moving along curves vs. shifting curves
- **Format/Inputs:** Side-by-side comparison with examples
- **Expected Outputs:** Clear understanding of critical distinction
- **Interaction Model:** Flashcard-style scenarios with visual feedback
- **Design Notes:**
  - **Two Panels:**
    - **Left: Movement Along Curve** (price change only)
      - Shows curve staying in place
      - Price changes, quantity responds along existing curve
      - Example: "Price of gas rises from $3 to $4 → you buy less"
    - **Right: Shift of Curve** (non-price factor changes)
      - Shows entire curve moving left or right
      - Price may or may not change
      - Example: "Your income doubles → demand for cars shifts right"
  - **Practice Mode:**
    - 20 scenarios presented randomly
    - Student identifies: "Movement or Shift?"
    - Immediate feedback with explanation
    - Score tracking
  - **Common Mistakes Highlighted:**
    - "Price change → MOVEMENT (not shift!)"
    - "Income change → SHIFT"
  - **Visual Cues:**
    - Movement: Dot sliding along curve (animated)
    - Shift: Entire curve sliding left/right (animated)
  - Color coding for clarity
  - Mobile-friendly

---

## Day 2 Assets

### 1. Market Analyzer Tool (PRIMARY SKILL BUILDER)
- **Purpose:** Systematic framework for analyzing any market's supply/demand factors
- **Format/Inputs:** Multi-step analysis wizard with real-time calculations
- **Expected Outputs:** Complete market analysis with predictions and personal action plan
- **Interaction Model:** Guided form with dropdown selectors, text inputs, and visual feedback

**Step 1: Select Market**
- Dropdown options:
  - {{STATE_NAME}} Housing Market
  - {{STATE_NAME}} Labor Market (specific career)
  - Consumer Electronics
  - Used Car Market
  - Rental Market
  - Custom (user enters)

**Step 2: Current Equilibrium**
- Input fields:
  - Current price: $________
  - Current quantity: ________
  - Market description: Text area
- Data auto-populated for {{STATE_NAME}} markets when available

**Step 3: Demand Analysis**
- Table with rows for each demand factor:
  - Income levels
  - Prices of related goods
  - Consumer tastes/preferences
  - Expectations about future
  - Number of buyers
- For each factor:
  - Effect: Increase / Decrease / Neutral (dropdown)
  - Strength: Low / Medium / High (dropdown)
  - Explanation: Text input
- Auto-calculation: Net demand shift (Right / Left / Stable)
- Visual: Demand curve position shown on graph

**Step 4: Supply Analysis**
- Table with rows for each supply factor:
  - Input costs
  - Technology
  - Number of sellers
  - Expectations
  - Government policy
  - Natural events/shocks
- Same structure as demand analysis
- Auto-calculation: Net supply shift
- Visual: Supply curve position shown on graph

**Step 5: Predict New Equilibrium**
- Based on Step 3 and 4 inputs, tool predicts:
  - Price direction: ↑ / ↓ / →
  - Quantity direction: ↑ / ↓ / →
  - Timeline estimate: Days / Weeks / Months / Years
- Visual: Combined supply/demand graph showing shifts and new equilibrium
- Confidence level: How certain is this prediction? (based on strength ratings)

**Step 6: Personal Decision**
- Guided prompts based on market selected:
  - "What should you do?"
  - "When should you act?"
  - "What's your backup plan?"
  - "Potential savings/gains: $________"
- Action plan generator
- Calendar integration (set reminder to review)

**Step 7: Monitor and Adjust**
- Indicators to track: Checklist
- What would change your decision?: Text input
- Review date: Date picker
- Save analysis for later comparison

**Technical Specifications:**
- Real-time graph updates as user inputs data
- Save/load functionality (localStorage or user account)
- Export to PDF with full analysis
- Share link (generates unique URL)
- {{STATE_NAME}}-specific data integration
- Mobile-responsive design
- Works offline (progressive web app)

**Data Integration:**
- Pulls current {{STATE_NAME}} housing prices from API
- Labor market data from BLS
- Historical price trends for context
- Forecast models for comparison

### 2. {{STATE_NAME}} Housing Market Dashboard
- **Purpose:** Comprehensive view of {{STATE_NAME}} housing supply/demand factors
- **Format/Inputs:** Interactive data dashboard with filters and visualizations
- **Expected Outputs:** Evidence-based understanding of {{STATE_NAME}} housing market
- **Interaction Model:** Filter by region, time period, property type; explore data visually

**Key Metrics Displayed:**
- Median home price: {{STATE_MEDIAN_HOME_PRICE}}
- Median rent: {{STATE_MEDIAN_RENT}}/month
- Inventory levels (months of supply)
- Days on market
- Price trends (YoY, 5-year)
- Affordability index

**Demand Factor Cards:**
- Population growth rate (+/- %)
- Employment rate
- Median income trends
- Mortgage rate trends
- Each card shows: Current value, trend arrow, chart

**Supply Factor Cards:**
- New construction permits
- Housing starts
- Construction costs index
- Land availability
- Zoning changes

**Interactive Features:**
- **Regional Filter:** Select county/metro area within {{STATE_NAME}}
- **Time Selector:** 1 year / 3 years / 5 years / 10 years
- **Property Type:** Single-family / Condo / Apartment
- **Comparison Mode:** Compare {{STATE_NAME}} to neighboring states

**Visualizations:**
- Line graph: Price trends over time
- Bar chart: Supply vs. demand pressure by region
- Heat map: {{STATE_NAME}} map showing price levels by area
- Scatter plot: Price vs. income by county

**Scenario Planning:**
- "What if mortgage rates rise 2%?" button
- "What if new construction doubles?" button
- Shows predicted effect on equilibrium

**Data Sources:**
- Zillow API
- {{STATE_NAME}} Realtor Association
- Census Bureau
- Federal Reserve (mortgage rates)

**Export Options:**
- Download data as CSV
- Print summary report
- Share specific charts

### 3. {{STATE_NAME}} Labor Market Explorer
- **Purpose:** Help students research careers using supply/demand framework
- **Format/Inputs:** Searchable database of careers with supply/demand analysis
- **Expected Outputs:** Informed career decisions based on market analysis
- **Interaction Model:** Search careers, filter by factors, compare options

**Career Database:**
- 200+ careers with data for each:
  - Job title
  - Description
  - Starting salary in {{STATE_NAME}}
  - 10-year salary projection
  - Job growth rate (demand indicator)
  - Education/training required (supply barrier)
  - Current unemployment rate in field
  - Number of annual job openings in {{STATE_NAME}}
  - Automation risk score

**Search and Filter:**
- **Search bar:** Type career name or keyword
- **Filter by Industry:** Healthcare, Tech, Education, Trades, Business, etc.
- **Filter by Education:** High school, Associate's, Bachelor's, Graduate
- **Filter by Demand:** High growth / Moderate / Declining
- **Filter by Supply:** Shortage / Balanced / Oversaturated
- **Filter by Salary:** $30k-50k / $50k-75k / $75k-100k / $100k+

**Career Detail View:**
- **Demand Analysis:**
  - Industry growth trends
  - Demographic drivers (e.g., aging population → healthcare demand)
  - Technology impact
  - {{STATE_NAME}}-specific demand factors
  - Graph showing job posting trends
- **Supply Analysis:**
  - Number of graduates/completers per year
  - Barriers to entry (education, licensing, skills)
  - Competition level
  - Geographic concentration
  - Graph showing worker supply trends
- **Market Outlook:**
  - Demand vs. supply assessment
  - Wage trend prediction
  - Job security rating
  - Career advancement potential
- **{{STATE_NAME}} Specifics:**
  - Major employers in state
  - Regional variations (metro vs. rural)
  - State-specific regulations or requirements
  - Links to {{STATE_NAME}} training programs

**Comparison Tool:**
- Select up to 3 careers
- Side-by-side comparison table
- Visual comparison charts
- "Best fit" recommendation based on user priorities

**Career Planning Worksheet:**
- Save favorite careers
- Rate careers on personal criteria
- Export comparison as PDF
- Create action plan (education needed, timeline, steps)

**Data Sources:**
- Bureau of Labor Statistics (BLS)
- {{STATE_NAME}} Department of Labor
- O*NET database
- Industry reports

### 4. Price Elasticity Calculator and Timing Tool
- **Purpose:** Help students identify price-sensitive purchases and optimize timing
- **Format/Inputs:** Calculator with purchase category selector
- **Expected Outputs:** Elasticity classification and money-saving timing recommendations
- **Interaction Model:** Select purchase, answer questions, get strategy recommendations

**Purchase Category Selector:**
- Dropdown with common purchases:
  - Smartphone
  - Laptop/Computer
  - Car (new/used)
  - Apartment rental
  - Textbooks
  - Concert/Event tickets
  - Airline tickets
  - Clothing
  - Electronics
  - Furniture
  - Custom (user enters)

**Elasticity Assessment Questions:**
For selected purchase:
1. "How many close substitutes exist?" (None / Few / Many)
2. "How urgently do you need this?" (Immediately / Within weeks / Can wait months)
3. "What % of your budget does it represent?" (Small / Moderate / Large)
4. "Is it a necessity or luxury?" (Necessity / Nice to have / Luxury)
5. "How often do you buy this?" (Daily / Weekly / Rarely)

**Elasticity Classification:**
Based on answers, tool classifies:
- **Highly Elastic** (Price sensitive - you have leverage)
- **Moderately Elastic**
- **Inelastic** (Price insensitive - limited leverage)

**For Each Classification, Tool Provides:**

**Highly Elastic:**
- "You have strong negotiating power!"
- Strategies:
  - Wait for sales/promotions
  - Shop multiple sellers
  - Consider alternatives/substitutes
  - Negotiate price
  - Buy off-season or at low-demand times
- Timing recommendations:
  - Cars: End of month/quarter/year
  - Clothing: End of season
  - Electronics: After new model released
  - Event tickets: Day-of or resale market

**Inelastic:**
- "Limited negotiating power—focus on reducing quantity"
- Strategies:
  - Shop for best available price (small savings)
  - Find long-term substitutes
  - Reduce consumption frequency
  - Look for generic/alternative brands
  - Check for discounts (student, bulk, membership)
- Examples:
  - Gas: Drive less, carpool, efficient vehicle
  - Prescription meds: Generic, compare pharmacies
  - Utilities: Reduce usage, improve efficiency

**Supply and Demand Timing Analysis:**
- "When is supply highest for this product?"
- "When is demand lowest?"
- Visual calendar showing optimal purchase windows
- Example for smartphones:
  - High supply: After new model launches (old inventory)
  - Low demand: Non-holiday periods
  - Best time: February-March (post-holiday, pre-summer)

**Expected Savings Calculator:**
- Input typical price: $________
- Tool estimates savings from optimal timing: $________
- Annual savings if applied to all purchases: $________

**Personal Purchase Plan:**
- Item I'm planning to buy: ________
- Elasticity: ________
- Optimal timing: ________
- Expected savings: $________
- Reminder set for: [Date picker]
- Alternative if price too high: ________

**Technical Specifications:**
- Mobile-responsive
- Save purchase plans
- Calendar integration for reminders
- Track actual vs. expected savings
- Gamification: "Total saved this year" counter

### 5. Combined Supply and Demand Shift Analyzer
- **Purpose:** Practice analyzing scenarios with simultaneous shifts
- **Format/Inputs:** Scenario-based practice with instant feedback
- **Expected Outputs:** Mastery of multi-factor analysis
- **Interaction Model:** Read scenario, predict outcome, check answer

**Scenario Bank:**
20+ realistic scenarios, each with:
- Description of event/situation
- Questions:
  - "Does demand shift? If so, which direction?"
  - "Does supply shift? If so, which direction?"
  - "What happens to equilibrium price?"
  - "What happens to equilibrium quantity?"
  - "What's the timeline for adjustment?"

**Example Scenarios:**

**Scenario 1: New Tech Product Launch**
- "Apple announces iPhone 16 with revolutionary features"
- Demand: Shifts right (increased desirability)
- Supply: Unchanged initially (takes time to ramp production)
- Price: Increases (demand > supply)
- Quantity: Increases slightly (supply constrained)
- Timeline: 3-6 months until supply catches up

**Scenario 2: {{STATE_NAME}} Economic Boom**
- "{{STATE_NAME}} attracts major employer, 10,000 high-paying jobs"
- Housing demand: Shifts right (more buyers, higher incomes)
- Housing supply: Shifts right slightly (incentive to build), but slower than demand
- Price: Increases (demand outpaces supply)
- Quantity: Increases
- Timeline: Years (housing construction is slow)

**Scenario 3: Oil Supply Shock**
- "OPEC reduces oil production by 20%"
- Demand: Unchanged short-term (inelastic)
- Supply: Shifts left (less production)
- Price: Increases significantly
- Quantity: Decreases
- Timeline: Months (demand eventually falls as prices rise)

**Scenario 4: Automation in Manufacturing**
- "Factories adopt AI robots, cutting production costs 40%"
- Demand: Unchanged (consumer preference unchanged)
- Supply: Shifts right (lower costs enable more production)
- Price: Decreases
- Quantity: Increases
- Timeline: Years (gradual adoption)

**Student Workflow:**
1. Read scenario
2. Make predictions (dropdowns for each question)
3. Submit
4. Instant feedback showing:
   - Correct answer
   - Explanation of economic forces
   - Visual graph showing shifts
   - Related real-world examples
5. Move to next scenario

**Difficulty Levels:**
- **Level 1:** Single shift (either supply or demand, not both)
- **Level 2:** Double shift (both shift same direction)
- **Level 3:** Opposite shifts (supply up, demand down - requires careful analysis)
- **Level 4:** Multi-factor with ambiguous outcomes

**Progress Tracking:**
- Scenarios completed: X/20
- Accuracy rate: Y%
- Mastery by category: Supply shifts (90%), Demand shifts (85%), Combined (70%)
- Recommendations for practice

**Classroom Mode:**
- Teacher dashboard to assign specific scenarios
- Class leaderboard (optional)
- Export results for grading

---

## Downloadable Resources (Printable PDFs)

### 1. Supply and Demand Analysis Worksheet
- **Purpose:** Structured note-taking for Day 1
- **Format:** 2-page PDF
- **Content:**
  - **Page 1:** Key concepts
    - Law of Demand definition and graph
    - Law of Supply definition and graph
    - Equilibrium explanation
    - Practice: Label curves, identify equilibrium
  - **Page 2:** Shifters reference
    - 5 demand shifters with examples
    - 6 supply shifters with examples
    - Practice scenarios: Identify which shifter and direction
  - Answer key for teachers

### 2. Day 2 Learning Lab Activity Packet
- **Purpose:** All Day 2 activities in printable format
- **Format:** 10-page PDF packet
- **Content:**
  - **Pages 1-2:** {{STATE_NAME}} Housing Market Analysis (tables and questions)
  - **Pages 3-4:** {{STATE_NAME}} Labor Market Analysis (career comparison tables)
  - **Pages 5-6:** Price Elasticity Classification (table and strategies)
  - **Pages 7-8:** Market Analyzer Tool (blank template)
  - **Pages 9-10:** Reflection questions and self-assessment
  - State-specific version with {{STATE_NAME}} data pre-filled

### 3. {{STATE_NAME}} Market Data Fact Sheet
- **Purpose:** Quick reference for state-specific market information
- **Format:** 2-page double-sided reference card
- **Content (Front):**
  - Housing: Median price, rent, inventory, trends
  - Labor: Unemployment rate, major industries, wage growth
  - Demographics: Population growth, age distribution, income levels
  - Economic indicators: GDP growth, business climate ranking
- **Content (Back):**
  - Supply factors affecting {{STATE_NAME}} markets
  - Demand factors affecting {{STATE_NAME}} markets
  - Regional variations within state
  - Comparison to neighboring states
  - Resources for ongoing market research
  - Links to {{STATE_NAME}} economic data sources

### 4. Supply and Demand Vocabulary Glossary
- **Purpose:** Reference for key terms
- **Format:** 2-page PDF
- **Content:**
  - Law of Demand
  - Law of Supply
  - Equilibrium
  - Surplus
  - Shortage
  - Demand shifters (with examples)
  - Supply shifters (with examples)
  - Elasticity
  - Substitutes
  - Complements
  - Each term includes:
    - Clear definition
    - Example in context
    - Relevance to personal finance
    - {{STATE_NAME}}-specific application where relevant

### 5. Market Timing Strategy Guide
- **Purpose:** Practical guide for timing purchases to save money
- **Format:** 1-page calendar-style guide
- **Content:**
  - Month-by-month purchase timing recommendations
  - **January:** Gym equipment, decorations
  - **February:** Winter coats, TVs (post-Super Bowl)
  - **March:** Luggage, older smartphone models
  - **April:** Vacuums, sneakers
  - **May:** Mattresses, refrigerators
  - **June:** Tools, outdoor furniture
  - **July:** Summer clothing, grills
  - **August:** School supplies, outdoor equipment
  - **September:** Cars (new models arriving), grills
  - **October:** Denim, bikes
  - **November:** TVs and electronics (Black Friday)
  - **December:** Cars (end of year), gym memberships
  - Supply/demand explanation for each
  - Expected savings ranges

### 6. Career Market Research Template
- **Purpose:** Structured framework for researching career supply/demand
- **Format:** 2-page PDF worksheet
- **Content:**
  - **Page 1:** Career analysis framework
    - Career field: __________
    - Demand factors checklist
    - Supply factors checklist
    - Salary data ({{STATE_NAME}} specific)
    - Job growth projections
    - Education/training required
  - **Page 2:** Decision matrix
    - Compare 3 careers side-by-side
    - Rate on multiple criteria
    - Final recommendation
  - Resources for {{STATE_NAME}} career research

---

## Asset Development Priority

**Phase 1 (Essential for Launch):**
1. Market Analyzer Tool (primary skill builder)
2. Supply and Demand Curves Interactive Visualization
3. Market Equilibrium Simulator
4. Day 2 Learning Lab Activity Packet (printable)
5. {{STATE_NAME}} Market Data Fact Sheet

**Phase 2 (Enhances Experience):**
6. {{STATE_NAME}} Housing Market Dashboard
7. {{STATE_NAME}} Labor Market Explorer
8. Demand Shifters Interactive Tool
9. Supply Shifters Interactive Tool
10. Movement vs. Shift Comparison Tool

**Phase 3 (Nice to Have):**
11. Price Elasticity Calculator and Timing Tool
12. Combined Supply and Demand Shift Analyzer
13. Pandemic Hand Sanitizer Case Study Interactive
14. Supply and Demand Analysis Worksheet (printable)
15. Vocabulary Glossary
16. Market Timing Strategy Guide
17. Career Market Research Template

---

## Technical Implementation Notes

**State-Specific System Requirements:**
- All tools must pull {{STATE_NAME}}-specific data:
  - Median home price: {{STATE_MEDIAN_HOME_PRICE}}
  - Median rent: {{STATE_MEDIAN_RENT}}
  - Unemployment rate: {{STATE_UNEMPLOYMENT_RATE}}
  - Major industries: {{STATE_MAJOR_INDUSTRIES}}
  - Population and demographic trends
- State determined at district/admin level
- All content automatically displays correct {{STATE_NAME}} data
- Monthly data updates for housing and labor markets

**Accessibility:**
- WCAG 2.1 AA compliance
- Keyboard navigation for all interactive tools
- Screen reader compatible (ARIA labels)
- Color-blind friendly palettes
- Text alternatives for graphs
- Adjustable text size

**Data Sources:**
- Zillow API (housing data)
- Bureau of Labor Statistics (labor market, wages)
- {{STATE_NAME}} Department of Labor
- Federal Reserve Economic Data (FRED)
- Census Bureau (demographics)
- {{STATE_NAME}} Realtor Association
- Industry-specific data providers

**Performance Requirements:**
- Interactive tools update in real-time (<100ms)
- Mobile-optimized for 3G connections
- All PDFs under 2MB
- Responsive design: mobile, tablet, desktop
- Cross-browser compatibility

**Asset File Naming Convention:**
- `l50-{asset-name}-{version}.{ext}`
- Example: `l50-market-analyzer-v1.html`
- Example: `l50-activity-packet-{{STATE_CODE}}-v1.pdf`
- Example: `l50-supply-demand-viz-v1.js`

**Integration Points:**
- Market Analyzer embeds in Day 2 student content
- {{STATE_NAME}} dashboards link from teacher guides
- Downloadable PDFs linked from both student and teacher materials
- Data APIs refresh automatically
- User progress saved in LMS database

---

## Assessment Integration

**Formative Assessment:**
- Embedded quiz questions in interactive tools
- Immediate feedback on scenario predictions
- Self-check opportunities throughout

**Summative Assessment:**
- Completed Market Analyzer (graded on analysis quality)
- Housing market analysis (graded on application of concepts)
- Career research project (graded on supply/demand analysis)
- Elasticity and timing plan (graded on strategy)

**Rubrics Provided:**
- For each major activity
- Clear criteria for performance levels
- Aligned with learning objectives from architecture.json

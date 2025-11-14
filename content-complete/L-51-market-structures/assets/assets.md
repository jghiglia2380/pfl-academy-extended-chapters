# Asset Specifications for L-51: Market Structures and Consumer Choice

## Day 1 Assets

### 1. Market Structure Comparison Table Interactive
- **Purpose:** Visual comparison of four market structures with sortable/filterable data
- **Format/Inputs:** Interactive table with expandable rows
- **Expected Outputs:** Clear understanding of how structures differ
- **Interaction Model:** Click to expand details, sort by characteristics
- **Design Notes:**
  - Main table with columns: Perfect Competition | Monopolistic Competition | Oligopoly | Monopoly
  - Row categories:
    - Number of Sellers
    - Product Type
    - Barriers to Entry
    - Price Control
    - Consumer Surplus
    - Examples
  - Click each cell to expand with detailed explanation
  - Color coding: Green (consumer-friendly) → Red (seller-friendly)
  - Mobile-responsive with collapsible rows
  - "Quiz Mode": Hides one column, students guess characteristics

### 2. Consumer Surplus Visualization
- **Purpose:** Show how consumer surplus changes across market structures
- **Format/Inputs:** Animated graph showing surplus areas
- **Expected Outputs:** Understanding that monopoly reduces surplus
- **Interaction Model:** Slider to change market structure, see surplus change
- **Design Notes:**
  - Supply/demand graph with shaded consumer surplus area
  - Slider: Perfect Competition → Monopolistic → Oligopoly → Monopoly
  - As slider moves right:
    - Price increases
    - Quantity decreases
    - Consumer surplus (blue area) shrinks
    - Producer surplus (red area) grows
    - Deadweight loss (grey triangle) appears/grows
  - Numerical display: "Consumer surplus: $X, Producer surplus: $Y, Deadweight loss: $Z"
  - Real-world price examples for each structure
  - Mobile-friendly

### 3. Barriers to Entry Analyzer
- **Purpose:** Help students understand what creates different market structures
- **Format/Inputs:** Interactive checklist that predicts market structure
- **Expected Outputs:** Understanding of how barriers determine structure
- **Interaction Model:** Check boxes for barriers present, tool predicts structure
- **Design Notes:**
  - **Barrier Checklist:**
    - ☐ High capital requirements (need $1M+ to start)
    - ☐ Economies of scale (large firms have cost advantage)
    - ☐ Government regulation (licenses, patents, permits)
    - ☐ Control of essential resources
    - ☐ Network effects (product more valuable with more users)
    - ☐ Brand loyalty
    - ☐ Switching costs for customers
  - **Prediction Algorithm:**
    - 0-1 barriers checked → Likely Perfect or Monopolistic Competition
    - 2-3 barriers → Likely Oligopoly
    - 4+ barriers → Likely Monopoly
  - **Examples for each barrier type**
  - **Create Your Own:** Input industry, check barriers, predict structure
  - Compare prediction to reality

### 4. Real-World Company Classifier
- **Purpose:** Practice identifying market structures using real companies
- **Format/Inputs:** Drag-and-drop sorting game
- **Expected Outputs:** Ability to classify actual markets
- **Interaction Model:** Drag company logos into correct structure category
- **Design Notes:**
  - Four bins: Perfect Competition | Monopolistic Competition | Oligopoly | Monopoly
  - 20+ company logos/cards to sort:
    - Starbucks, local restaurants (Monopolistic)
    - Apple, Samsung, Google phones (Oligopoly)
    - Electric companies, water utilities (Monopoly)
    - Wheat farmers, stock traders (Perfect)
  - Instant feedback: ✓ or ✗ with explanation
  - Scoring system
  - Difficulty levels:
    - Easy: Clear examples
    - Medium: Debatable cases
    - Hard: Requires market definition (e.g., "Is Amazon a monopoly?")
  - Leaderboard for classroom competition
  - Mobile-responsive drag-and-drop

### 5. Pricing Power Spectrum Interactive
- **Purpose:** Visualize how pricing power increases from competition to monopoly
- **Format/Inputs:** Interactive spectrum with draggable slider
- **Expected Outputs:** Understanding of pricing power continuum
- **Interaction Model:** Drag slider, see how price/output change
- **Design Notes:**
  - Horizontal spectrum:
    ```
    Low Prices ←——————————————————→ High Prices
    (Consumer Benefit)          (Seller Benefit)

    Perfect → Monopolistic → Oligopoly → Monopoly
    ```
  - Drag slider along spectrum
  - Display shows:
    - Market characteristics
    - Typical price markup (% above cost)
    - Consumer negotiating power
    - Real-world examples
    - "If you were buying in this market, what should you do?"
  - Visual: Changes background color (green → yellow → orange → red)
  - Comparison tool: Select two products, compare structures
  - Mobile-friendly

### 6. Monopoly Types Explainer
- **Purpose:** Distinguish between natural, legal, and market power monopolies
- **Format/Inputs:** Interactive diagram with case studies
- **Expected Outputs:** Understanding of why monopolies exist and how to address each type
- **Interaction Model:** Click each type for detailed explanation and examples
- **Design Notes:**
  - Three branches from "Monopoly":
    1. **Natural Monopoly**
       - Definition: One firm more efficient than many
       - Examples: Electricity, water, gas, rail infrastructure
       - Government response: Price regulation
       - Why it makes sense: Avoid duplication of expensive infrastructure
    2. **Legal Monopoly**
       - Definition: Government grants exclusive rights
       - Examples: Patents (drugs), copyrights (books), licenses (spectrum)
       - Government response: Time limits, public purpose
       - Why it makes sense: Encourage innovation/investment
    3. **Market Power Monopoly**
       - Definition: Dominance through business practices
       - Examples: Standard Oil (historical), current debates (big tech)
       - Government response: Antitrust enforcement
       - Why it's problematic: No legitimate justification
  - Each type includes:
    - Case study example
    - Graph showing pricing/output
    - Consumer impact
    - Policy implications
  - Quiz: Given scenario, identify monopoly type

---

## Day 2 Assets

### 1. Market Structure Identifier Tool (PRIMARY SKILL BUILDER)
- **Purpose:** Systematic decision tree for classifying any market
- **Format/Inputs:** Step-by-step wizard with branching logic
- **Expected Outputs:** Market structure classification with consumer strategy
- **Interaction Model:** Answer questions, tool guides to classification

**Step 1: Seller Count**
- Input: "How many sellers can you realistically choose from?"
  - 1 → Proceed to Monopoly verification
  - 2-10 → Proceed to Oligopoly verification
  - 10+ → Proceed to Competition verification

**Step 2a: Monopoly Verification**
- "Is there truly no substitute?"
  - Yes → MONOPOLY
  - No → "You may be defining market too narrowly. Expand definition."
- "Why does this monopoly exist?"
  - Natural (infrastructure)
  - Legal (patent/license)
  - Market power (dominance)
- **Recommended Strategy:** Display monopoly tactics (minimize consumption, seek substitutes, time-of-use pricing)

**Step 2b: Oligopoly Verification**
- "Are there high barriers to entry?" (capital, regulation, scale)
  - Yes → OLIGOPOLY
  - No → Probably monopolistic competition with consolidation
- "Do firm prices move together?"
  - Yes → Confirms oligopoly (coordination)
  - No → Check for monopolistic competition
- **Recommended Strategy:** Display oligopoly tactics (compare all players, negotiate, threaten to switch)

**Step 2c: Competition Verification**
- "Are products identical or differentiated?"
  - Identical → PERFECT COMPETITION
    - **Strategy:** Buy cheapest, products are same
  - Differentiated → MONOPOLISTIC COMPETITION
    - **Strategy:** Assess if differentiation is worth premium

**Output Screen:**
- Market structure classification
- Confidence level (based on answers)
- Detailed consumer strategy
- Expected price range
- Negotiation tips specific to structure
- Examples of similar markets

**Save and Track Feature:**
- Save classifications for regular purchases
- Track if strategies worked
- Update based on market changes

**Technical Specifications:**
- Mobile-first design
- Save progress
- Export PDF summary
- Integration with purchase tracking (links to Activity 1)

### 2. Consumer Strategy Generator
- **Purpose:** Create customized action plans for each purchase based on market structure
- **Format/Inputs:** Purchase-specific strategy builder
- **Expected Outputs:** Detailed action plan with savings estimates
- **Interaction Model:** Select purchase, input details, get tailored strategy

**Input Fields:**
- Purchase/service: __________
- Current cost: $__________/month
- Market structure: (from identifier tool)
- Current provider: __________
- Contract status: Month-to-month / Annual / Fixed term expires: ____

**Strategy Generation (based on structure):**

**Perfect Competition:**
- "Shop by price alone - products are identical"
- Generates: List of comparison shopping tools
- Action: "Use [PriceGrabber/Google Shopping] to find lowest price"
- Estimated savings: 5-10% (marginal in perfect competition)

**Monopolistic Competition:**
- "Evaluate if brand premium is worth it to YOU"
- Questions:
  - "What do you value about current choice?"
  - "What alternatives exist?"
  - "Have you tried alternatives?"
- Action: "Try [Alternative] for 1 month, compare quality"
- Estimated savings: 15-30% (switching to value brand)

**Oligopoly:**
- "Compare all major players and negotiate"
- Generates: Competitor comparison table
- Negotiation script customized to service
- "Call retention: [Scripted phone conversation]"
- Best timing: "Negotiate when: [Contract expires / Competitor has promotion / Annual renewal]"
- Estimated savings: 10-25% (successful negotiation)

**Monopoly:**
- "Reduce consumption since price is fixed"
- Generates: Consumption reduction tactics
- "Calculate tier structure: You're in tier [X], costing $[Y]. Reduce to tier [X-1] to save $[Z]"
- Long-term: "Consider alternatives: [Solar panels / Streaming / etc.]"
- Estimated savings: 10-20% (usage reduction)

**Action Plan Output:**
- Step-by-step checklist
- Timeline (do by when)
- Expected savings (monthly and annual)
- Success metrics (how to know if working)
- Calendar reminders
- Follow-up review date

**Tracking:**
- Mark action as "Completed"
- Input actual savings
- Compare to estimate
- Share success stories (anonymized leaderboard)

### 3. Negotiation Simulator
- **Purpose:** Practice negotiating with oligopoly providers
- **Format/Inputs:** Interactive role-play with AI responses
- **Expected Outputs:** Confidence and skills for real negotiations
- **Interaction Model:** Conversation simulator with branching dialogue

**Scenarios:**
1. Cell phone plan negotiation
2. Internet service negotiation
3. Car insurance negotiation
4. Cable/streaming bundle negotiation

**For each scenario:**

**Setup:**
- Current bill: $X/month
- Competitor offer: $Y/month (must research real offer first)
- Goal: Match competitor or better

**Dialogue Options:**
- Multiple choice responses at each turn
- AI simulates customer service representative
- Responses vary based on:
  - How demanding vs. polite student is
  - Whether they threaten to switch
  - Whether they have specific competitor offer
  - Their tenure as customer

**Possible Outcomes:**
- ✓ Success: Matched/beat competitor (save $Z/month)
- Partial: Small discount but not goal
- ✗ Failed: No discount, needs to switch or accept price

**Feedback:**
- "Good job using specific competitor offer"
- "Try being more direct: 'Can you match this?'"
- "Retention department has more power - ask to be transferred"

**Best Practices Taught:**
- Have specific competitor offer researched
- Be polite but firm
- Express loyalty but willingness to switch
- Ask for retention/loyalty department
- Get offer in writing
- Don't accept first "no"

**Practice Mode:**
- Unlimited attempts
- See different AI responses
- Learn from mistakes

**Graded Mode:**
- One attempt
- Scored on outcome
- Feedback on approach

### 4. {{STATE_NAME}} Market Structure Map
- **Purpose:** Visualize which market structures dominate different sectors in {{STATE_NAME}}
- **Format/Inputs:** Interactive sector-by-sector breakdown
- **Expected Outputs:** Understanding of local market landscape
- **Interaction Model:** Click sectors to see structure details

**Sectors Displayed:**
- Utilities (Electric, Gas, Water)
- Telecommunications (Cell, Internet, Cable)
- Healthcare (Hospitals, Insurance, Pharmacies)
- Banking & Finance
- Retail (Groceries, Clothing, General)
- Restaurants & Food Service
- Transportation (Auto, Public Transit)
- Housing (Buy, Rent)
- Insurance (Auto, Home, Health)
- Education (K-12, Higher Ed)

**For Each Sector:**
- Market structure classification
- Major players (with logos)
- Number of options for average {{STATE_NAME}} resident
- Price range
- Whether regulated
- Consumer power level (Low/Medium/High)
- Tips for maximizing value

**Interactive Features:**
- Filter by: "Where I have most power" / "Where I have least power"
- Sort by: "Most expensive" / "Most competitive" / "Most regulated"
- Compare: Side-by-side of two sectors
- "My Spending": Input monthly spending in each sector
  - Tool calculates: % in competitive vs. non-competitive markets
  - Highlights: Where you have most opportunity to save

**{{STATE_NAME}} Specifics:**
- Uses actual provider names: {{STATE_UTILITY_PROVIDERS}}, {{STATE_TELECOM_PROVIDERS}}
- Real market data for state
- Links to state regulatory agencies
- Comparison to neighboring states

### 5. Regulation Impact Analyzer
- **Purpose:** Explore how government regulation affects prices and choices in different market structures
- **Format/Inputs:** Scenario simulator showing regulated vs. unregulated outcomes
- **Expected Outputs:** Nuanced understanding of regulation trade-offs
- **Interaction Model:** Toggle regulation on/off, see market changes

**Scenarios:**

**Scenario 1: Utility Monopoly**
- **Unregulated:**
  - Price: $200/month (monopoly sets profit-maximizing price)
  - Quality: Minimal investment (no competition pressure)
  - Access: Only profitable areas served
- **Regulated:**
  - Price: $120/month (set by public utility commission)
  - Quality: Required service standards
  - Access: Universal service mandate
- **Trade-off:** Lower prices and universal access, but less innovation and potential inefficiency

**Scenario 2: Ride-Sharing (Oligopoly becoming Monopolistic Competition)**
- **Regulated (Old taxis):**
  - Price: High (regulated rates, medallion limits supply)
  - Quality: Variable
  - Options: Few (limited medallions)
- **Less Regulated (Uber/Lyft):**
  - Price: Lower (competition)
  - Quality: Rating system enforces quality
  - Options: Many drivers
- **Trade-off:** Benefits consumers but disrupts traditional industry, worker protections debated

**Scenario 3: Pharmaceutical Patents (Legal Monopoly)**
- **With Patent (20 years):**
  - Price: $500/month (monopoly pricing)
  - Innovation: High (companies invest in R&D knowing they'll have monopoly)
  - Access: Limited (many can't afford)
- **After Patent Expires (Generic competition):**
  - Price: $50/month (competitive market)
  - Innovation: Less (no profit incentive)
  - Access: Much better (affordable)
- **Trade-off:** Monopoly encourages innovation but limits access; need balance

**Student Task:**
- For each scenario, answer:
  - "Which outcome do you prefer?"
  - "What's the best policy?"
  - "Who wins? Who loses?"
- No single "right answer" - encourages critical thinking

**{{STATE_NAME}} Application:**
- Real examples from state
- Recent regulatory changes and impacts
- Student advocacy: "If you could change one {{STATE_NAME}} regulation, what would it be?"

### 6. Savings Calculator and Tracker
- **Purpose:** Calculate and track actual savings from applying market structure strategies
- **Format/Inputs:** Spreadsheet-style tracker with projections
- **Expected Outputs:** Motivation through quantified savings
- **Interaction Model:** Input purchases and strategies, see savings accumulate

**Input Table:**

| Purchase | Structure | Current Cost | Strategy | Est. Savings | Actual Savings | Status |
|----------|-----------|--------------|----------|--------------|----------------|--------|
| Cell phone | Oligopoly | $50/mo | Negotiate | $10/mo | $__ /mo | Pending / Completed |
| Electricity | Monopoly | $80/mo | Reduce usage | $12/mo | $__/mo | Pending / Completed |
| Coffee | Mon. Comp. | $100/mo | Switch to local | $30/mo | $__/mo | Pending / Completed |

**Calculations:**
- Total monthly savings: $__
- Annual savings: $__ × 12 = $__
- 5-year savings with 5% compound interest: $__
- "What you could buy with this": [Car down payment / Vacation / Emergency fund]

**Tracking Features:**
- Mark strategy as implemented
- Update with actual savings
- Compare estimate to reality
- Success rate: __% of estimates achieved
- Biggest win: $__ from [Strategy]
- Next opportunity: [Suggestion]

**Gamification:**
- Savings milestones: $100, $500, $1000 saved
- Badges: "Negotiator" (successful phone negotiation), "Minimalist" (reduced monopoly usage)
- Class leaderboard (optional, anonymized)
- Share success stories

**Export:**
- PDF summary
- CSV for Excel
- Share plan with family

---

## Downloadable Resources (Printable PDFs)

### 1. Market Structure Classification Worksheet
- **Purpose:** Structured note-taking for Day 1
- **Format:** 2-page PDF
- **Content:**
  - Page 1: Four structures comparison table (fill-in-the-blank)
  - Page 2: Classification practice (10 examples to classify)
  - Answer key for teachers

### 2. Day 2 Learning Lab Activity Packet
- **Purpose:** All activities in printable format
- **Format:** 8-page PDF
- **Content:**
  - Pages 1-2: Activity 1 - Purchase classification tables
  - Pages 3-4: Activity 2 - Consumer strategies by structure
  - Pages 5-6: Activity 3 - {{STATE_NAME}} industry analysis
  - Page 7: Activity 4 - Market Structure Identifier decision tree
  - Page 8: Savings tracker and action plan
  - State-specific version with {{STATE_NAME}} examples

### 3. {{STATE_NAME}} Market Structure Reference Card
- **Purpose:** Quick reference for state industries
- **Format:** 2-sided laminated card
- **Content (Front):**
  - {{STATE_NAME}} major providers by sector
  - Market structure for each
  - Regulatory agencies
- **Content (Back):**
  - Consumer strategies by structure
  - Negotiation tips
  - When to contact regulators
  - {{STATE_NAME}} consumer protection resources

### 4. Negotiation Script Templates
- **Purpose:** Word-for-word scripts for common negotiations
- **Format:** 1-page PDF per service type
- **Content:**
  - Cell phone negotiation
  - Internet negotiation
  - Insurance negotiation
  - Cable/streaming negotiation
  - Each includes:
    - Opening line
    - Response to "best we can do"
    - How to escalate to retention
    - When to walk away
    - Follow-up if successful

### 5. Market Structure Vocabulary Glossary
- **Purpose:** Reference for key terms
- **Format:** 2-page PDF
- **Content:**
  - Perfect competition
  - Monopolistic competition
  - Oligopoly
  - Monopoly
  - Barriers to entry
  - Consumer surplus
  - Producer surplus
  - Deadweight loss
  - Natural monopoly
  - Legal monopoly
  - Tacit collusion
  - Price leadership
  - Each with: definition, example, personal finance relevance

---

## Asset Development Priority

**Phase 1 (Essential for Launch):**
1. Market Structure Identifier Tool (primary skill builder)
2. Market Structure Comparison Table Interactive
3. Consumer Strategy Generator
4. Day 2 Learning Lab Activity Packet
5. {{STATE_NAME}} Market Structure Reference Card

**Phase 2 (Enhances Experience):**
6. {{STATE_NAME}} Market Structure Map
7. Negotiation Simulator
8. Consumer Surplus Visualization
9. Savings Calculator and Tracker
10. Negotiation Script Templates

**Phase 3 (Nice to Have):**
11. Barriers to Entry Analyzer
12. Real-World Company Classifier
13. Pricing Power Spectrum Interactive
14. Monopoly Types Explainer
15. Regulation Impact Analyzer
16. Vocabulary Glossary

---

## Technical Implementation Notes

**State-Specific Requirements:**
- Pull {{STATE_NAME}} provider data
- {{STATE_UTILITY_PROVIDERS}}
- {{STATE_TELECOM_PROVIDERS}}
- {{STATE_MAJOR_RETAILERS}}
- {{STATE_HEALTHCARE_MARKET}}
- Update annually as markets change

**Accessibility:**
- WCAG 2.1 AA compliance
- Keyboard navigation
- Screen reader compatible
- Color-blind friendly
- Text alternatives

**Data Sources:**
- {{STATE_NAME}} Public Utility Commission
- FCC (telecom data)
- State insurance department
- Consumer reports
- Industry associations

**Performance:**
- Real-time updates
- Mobile-optimized
- Works offline (PWA for identifier tool)
- Cross-browser compatible

**Asset File Naming:**
- `l51-{asset-name}-{version}.{ext}`
- Example: `l51-market-identifier-v1.html`
- Example: `l51-activity-packet-{{STATE_CODE}}-v1.pdf`

**Integration:**
- Identifier tool embeds in Day 2 content
- {{STATE_NAME}} map links from teacher guides
- Downloadable PDFs linked throughout
- User data saved in LMS database

---

## Assessment Integration

**Formative:**
- Interactive tool completion tracking
- Classification accuracy in games
- Negotiation simulator scores

**Summative:**
- Completed Market Structure Identifier analyses
- Consumer strategy action plans
- {{STATE_NAME}} industry classification
- Savings tracker (estimated vs. actual)

**Rubrics:**
- Classification accuracy (40%)
- Strategy appropriateness (30%)
- Implementation plan quality (20%)
- Savings realism (10%)

# Asset Specifications for L-58: Supply, Demand, and Market Structures

## Day 1 Assets

### 1. Supply and Demand Curves Interactive Diagram
- **Purpose:** Visual representation of supply and demand curves with equilibrium point
- **Format/Inputs:** Interactive SVG or HTML5 Canvas with draggable elements
- **Expected Outputs:** Clear understanding of curve relationships and equilibrium concept
- **Interaction Model:**
  - Display supply curve (upward sloping) and demand curve (downward sloping)
  - Hover over curves to see descriptions ("As price rises, quantity supplied increases")
  - Click on equilibrium point to highlight and show P* and Q* values
  - Toggle annotations on/off for simpler view
- **Design Notes:**
  - X-axis: Quantity (0 to 100 units)
  - Y-axis: Price ($0 to $100)
  - Use contrasting colors: Blue for demand, Red for supply
  - Equilibrium point marked with large dot and dashed lines to axes
  - Labels: "Equilibrium Price (P*)" and "Equilibrium Quantity (Q*)"
  - Include arrows showing curve directions and what they represent
  - Responsive design for mobile viewing

### 2. Consumer and Producer Surplus Visualization
- **Purpose:** Show graphically where consumer and producer surplus exist
- **Format/Inputs:** Annotated graph (SVG or interactive HTML5)
- **Expected Outputs:** Visual understanding of surplus as area between curves and price
- **Interaction Model:**
  - Static display with clear shading
  - Optional: Click "Consumer Surplus" to highlight that area, click "Producer Surplus" to highlight
  - Tooltip on hover showing "This area represents the benefit consumers receive"
- **Design Notes:**
  - Same supply-demand graph as Asset #1
  - Consumer surplus: Shaded area above price line, below demand curve (light blue)
  - Producer surplus: Shaded area below price line, above supply curve (light red/pink)
  - Labels clearly pointing to each area
  - Include example calculation: "If willing to pay $80 but price is $50, surplus = $30"
  - Show total surplus = consumer surplus + producer surplus

### 3. Market Structure Comparison Matrix
- **Purpose:** Side-by-side comparison of perfect competition, oligopoly, and monopoly
- **Format/Inputs:** Interactive table/matrix (HTML with CSS styling)
- **Expected Outputs:** Quick reference guide for distinguishing market types
- **Interaction Model:**
  - Click on any cell to expand with more details
  - Highlight row on hover to compare across structures
  - Filter to show only specific characteristics
- **Design Notes:**
  - Columns: Perfect Competition | Oligopoly | Monopoly
  - Rows: Number of firms, Product type, Entry barriers, Pricing power, Consumer surplus, Examples
  - Use visual indicators: ✓ (high), ~ (moderate), ✗ (low/none)
  - Color coding: Green (consumer-friendly), Yellow (moderate), Red (consumer-unfriendly)
  - Include real company logos in "Examples" row where appropriate
  - Mobile-responsive: Stack columns vertically on small screens

### 4. Equilibrium Shift Animations
- **Purpose:** Demonstrate how supply or demand shifts affect equilibrium
- **Format/Inputs:** Animated diagrams or step-by-step interactive presentations
- **Expected Outputs:** Intuitive understanding of market dynamics
- **Interaction Model:**
  - Four separate animations (or tabs to switch between):
    1. Demand increases (curve shifts right)
    2. Demand decreases (curve shifts left)
    3. Supply increases (curve shifts right)
    4. Supply decreases (curve shifts left)
  - Play/pause controls
  - Step-through buttons to advance frame-by-frame
  - Reset button to return to original equilibrium
- **Design Notes:**
  - Each animation shows:
    - Original equilibrium (P1, Q1)
    - The shift happening (curve moves with arrow)
    - New equilibrium (P2, Q2)
  - Display "Before" and "After" values clearly
  - Include real-world trigger: "New technology reduces production costs" → supply shifts right
  - Smooth animation (2-3 seconds per shift)
  - Highlight how BOTH price and quantity change

### 5. Price Change Scenarios Infographic
- **Purpose:** Real-world examples of supply-demand dynamics affecting prices
- **Format/Inputs:** Scrollable infographic or card-based layout
- **Expected Outputs:** Connection between theory and real price movements
- **Interaction Model:** Static or simple scroll-reveal animation
- **Design Notes:**
  - 6 real-world scenarios presented as cards:
    1. **Hurricane → Gasoline Shortage**: Supply ↓ → Price ↑
    2. **Celebrity Endorsement → Product Popularity**: Demand ↑ → Price ↑
    3. **Economic Recession → Luxury Goods**: Demand ↓ → Price ↓
    4. **New Factory → Increased Production**: Supply ↑ → Price ↓
    5. **Summer → Air Conditioning**: Demand ↑ (seasonal) → Price ↑
    6. **Bumper Crop → Abundant Harvest**: Supply ↑ → Price ↓
  - Each card includes:
    - Icon/image representing scenario
    - Headline: "What happened"
    - Graph showing curve shift
    - Price change indicator: ↑ or ↓
    - Student application: "When to buy: NOW or WAIT?"

## Day 2 Assets

### 1. Market Dynamics Simulator (PRIMARY SKILL BUILDER)
- **Purpose:** Comprehensive interactive tool for manipulating supply-demand curves and comparing market structures
- **Format/Inputs:** Web application with multiple modules
- **Expected Outputs:** Hands-on exploration of equilibrium changes, surplus calculations, and market structure impacts
- **Interaction Model:** Tabbed interface with 4 main modules
- **Design Notes:**

  **Module 1: Equilibrium Challenge Mode**
  - **Interface:**
    - Central graph area showing supply and demand curves
    - Slider controls to shift demand curve (left/right)
    - Slider controls to shift supply curve (left/right)
    - Reset button to return to baseline
    - Scenario selector dropdown (smartphone market, housing market, gasoline market, etc.)
  - **Functionality:**
    - Start with equilibrium at specified P and Q
    - User selects a scenario from dropdown (e.g., "Factory fire reduces production")
    - User predicts outcome (price up/down, quantity up/down) via multiple choice
    - User shifts appropriate curve to new position
    - System calculates new equilibrium and displays
    - Feedback: "Correct! Supply decreased, causing price to rise from $800 to $950 and quantity to fall from 10,000 to 7,500"
  - **Metrics Displayed:**
    - Original price and quantity
    - New price and quantity
    - Percentage change in each
    - Consumer surplus before and after (shaded areas)
    - Producer surplus before and after
  - **Scenarios Included:**
    1. Positive product review (demand ↑)
    2. Manufacturing disruption (supply ↓)
    3. Economic recession (demand ↓)
    4. New technology (supply ↑)
    5. Complementary good price drop (demand ↑)
    6. Input cost increase (supply ↓)

  **Module 2: Market Structure Comparison**
  - **Interface:**
    - Product selector (internet service, electricity, gasoline, groceries, etc.)
    - Market structure toggle: Perfect Competition | Oligopoly | Monopoly
    - Baseline demand and cost inputs (pre-populated but editable)
    - Results display panel
  - **Functionality:**
    - User selects standard product (e.g., "100 Mbps internet")
    - User sets baseline demand and per-unit cost
    - User toggles between market structures
    - System calculates and displays outcomes for each structure
  - **Outputs for Each Structure:**
    - **Perfect Competition (many firms):**
      - Market price ≈ cost + small margin
      - Quantity: High (efficient allocation)
      - Consumer surplus: Maximum
      - Producer surplus: Normal profits only
      - Total surplus: Maximized
    - **Oligopoly (3-5 firms):**
      - Market price > cost + moderate margin
      - Quantity: Moderate (some restriction)
      - Consumer surplus: Reduced
      - Producer surplus: Above-normal profits
      - Total surplus: Some deadweight loss
    - **Monopoly (1 firm):**
      - Market price >> cost + large margin
      - Quantity: Low (significant restriction)
      - Consumer surplus: Minimal
      - Producer surplus: Maximum (captures most surplus)
      - Total surplus: Significant deadweight loss
  - **Visual Display:**
    - Side-by-side comparison charts
    - Bar graphs showing price differences
    - Pie charts showing surplus distribution
    - Highlighted differences: "Monopoly charges 65% more than competition!"

  **Module 3: Elasticity Explorer**
  - **Interface:**
    - Product selector with elasticity presets:
      - Gasoline (inelastic)
      - Prescription medications (highly inelastic)
      - Restaurant meals (elastic)
      - Luxury goods (highly elastic)
    - Supply shock slider (-50% to +50%)
    - Demand elasticity adjuster (for custom scenarios)
  - **Functionality:**
    - User selects product or sets custom elasticity
    - User applies supply shock (e.g., -10% supply reduction)
    - System shows price and quantity changes
    - Comparison display shows inelastic vs. elastic responses
  - **Key Visualization:**
    - Two side-by-side graphs:
      - Left: Inelastic demand (steep curve) → large price change, small quantity change
      - Right: Elastic demand (flat curve) → small price change, large quantity change
    - Annotation: "10% supply reduction causes 25% price increase for inelastic goods but only 8% price increase for elastic goods"
  - **Budget Impact Calculator:**
    - Input: Current monthly spending on product
    - Input: Expected supply shock
    - Output: New monthly cost based on elasticity
    - Recommendation: "Budget cushion needed: $35/month"

  **Module 4: Personal Purchase Planner**
  - **Interface:**
    - Product description field
    - Market structure classifier (guided questions)
    - Supply-demand pattern inputs
    - Strategic recommendation engine
  - **Functionality:**
    - User enters product they plan to buy
    - Guided questions help classify market structure:
      - "How many sellers in your area?" → Many / Few / One
      - "Are products identical or differentiated?" → Identical / Differentiated
      - "Can you easily switch sellers?" → Yes / No
    - User researches and inputs:
      - Current price range
      - Seasonal demand patterns (if any)
      - Recent supply changes (new models, shortages)
      - Price trends (rising, falling, stable)
  - **Outputs:**
    - Market structure classification with confidence level
    - Optimal timing recommendation: "BUY NOW" or "WAIT UNTIL [period]"
    - Expected savings from optimal timing
    - Alternative strategies if immediate purchase needed
    - Negotiation leverage points identified
  - **Example Output:**
    - "Your market: Oligopoly (3 major dealers + small independents)"
    - "Current conditions: High inventory (supply up), winter season (demand down)"
    - "Recommendation: BUY NOW - conditions favor buyers"
    - "Strategy: Visit dealers end-of-month, mention competitor prices, emphasize immediate purchase ability"
    - "Expected savings: $800-1,200 (5-8% below average)"

  **General Simulator Features:**
  - Save scenarios to compare later
  - Export results as PDF report
  - Share link to specific scenario
  - Glossary sidebar with key terms
  - Help tooltips on all interactive elements
  - Tutorial mode for first-time users
  - Progress tracker (scenarios completed)

### 2. Price Analysis Worksheet
- **Purpose:** Structured template for researching real product markets
- **Format/Inputs:** Digital form (Google Sheets template) or printable PDF
- **Expected Outputs:** Completed market analysis for student's chosen product
- **Interaction Model:**
  - Fill-in template with guided prompts
  - Can be completed digitally or printed
  - Formulas auto-calculate where applicable (digital version)
- **Design Notes:**
  - **Section 1: Product Information**
    - Product name/description
    - Target budget
    - Purchase timeline
  - **Section 2: Market Structure Analysis**
    - Number of sellers (count)
    - Market classification (checkbox: Competition / Oligopoly / Monopoly)
    - Product differentiation level (1-10 scale)
    - Barriers to entry assessment
  - **Section 3: Supply-Demand Research**
    - Current prices from 3+ sellers (data table)
    - Price range (auto-calc: high - low)
    - Average price (auto-calc)
    - Seasonal demand pattern (description field)
    - Supply conditions (dropdown: Constrained / Normal / Abundant)
    - Recent trends (checkbox: Rising / Stable / Falling)
  - **Section 4: Strategic Plan**
    - Optimal purchase timing (date range)
    - Justification (text field)
    - Expected savings ($ or %)
    - Alternative if must buy immediately
    - Negotiation leverage points (bullet list)
  - **Section 5: Reflection**
    - Confidence in analysis (1-10 scale)
    - Information gaps identified
    - Next research steps

### 3. Consumer Surplus Maximization Scenarios
- **Purpose:** Practice applying economic concepts to purchasing decisions
- **Format/Inputs:** Interactive quiz/scenario tool
- **Expected Outputs:** Strategic thinking reinforcement
- **Interaction Model:**
  - Present scenario with multiple choice strategies
  - User selects strategy and provides reasoning
  - System provides feedback and optimal answer
  - Score tracking across scenarios
- **Design Notes:**
  - 10+ scenarios covering various markets:
    - Airline tickets (oligopoly, dynamic pricing)
    - Apartment rental (seasonal demand)
    - Electronics (oligopoly with frequent model changes)
    - Groceries (competitive with promotions)
    - Gym membership (oligopoly with negotiation potential)
    - Concert tickets (elasticity based on artist popularity)
    - Used cars (timing around month-end, seasons)
    - Textbooks (monopoly on required books)
    - Gasoline (inelastic demand, supply shocks)
    - Clothing (seasonal clearance cycles)
  - Each scenario includes:
    - Context description
    - Budget constraint
    - 4-5 strategy options
    - Reasoning prompt
    - Feedback explaining optimal choice
    - Estimated surplus gained
  - Gamification: Total surplus accumulated across all scenarios
  - Leaderboard option for class competition

### 4. Market Research Guide
- **Purpose:** Step-by-step instructions for investigating real markets
- **Format/Inputs:** Printable checklist or digital guide (PDF or web page)
- **Expected Outputs:** Structured approach to market analysis
- **Interaction Model:** Reference document with examples
- **Design Notes:**
  - **Step 1: Identify Market Structure**
    - Questions to ask: "How many sellers? Can I switch easily? Are products identical?"
    - Decision tree leading to classification
    - Examples: "3 wireless carriers in your area = oligopoly"
  - **Step 2: Research Supply Conditions**
    - Where to look: Inventory levels, production news, seasonal patterns
    - Tools: Google Trends, industry reports, dealer inventory counters
    - Red flags: "Low inventory" signs, "Limited supply" messaging
  - **Step 3: Analyze Demand Patterns**
    - Seasonal calendars by product type
    - Economic indicators affecting demand
    - Trend analysis tools
  - **Step 4: Find Price Data**
    - Comparison shopping sites to check
    - Historical price trackers (CamelCamelCamel, Google Shopping insights)
    - How to document price ranges
  - **Step 5: Determine Timing**
    - Decision matrix: Supply (high/low) × Demand (high/low) → Buy now or wait?
    - Risk assessment: Cost of waiting vs. potential savings
  - **Step 6: Develop Strategy**
    - Negotiation tactics by market structure
    - Leverage points to emphasize
    - Walk-away alternatives

### 5. Market Strategy Planner Template
- **Purpose:** Finalized purchasing plan based on analysis
- **Format/Inputs:** One-page template (PDF or digital form)
- **Expected Outputs:** Actionable purchasing strategy
- **Interaction Model:** Fill-in template with date tracking
- **Design Notes:**
  - **Header Section:**
    - Product: ___
    - Target price: ___
    - Max budget: ___
    - Purchase deadline: ___
  - **Market Analysis Summary:**
    - Market structure: ___
    - Current supply conditions: ___
    - Current demand conditions: ___
    - Price trend: ___
  - **Strategy:**
    - Optimal timing: ___
    - Specific tactics: ___
    - Sellers to approach: ___
    - Negotiation points: ___
  - **Execution Checklist:**
    - [ ] Research completed
    - [ ] Price alerts set
    - [ ] Financing pre-approved (if applicable)
    - [ ] Alternatives identified
    - [ ] Timing confirmed
  - **Results Tracking:**
    - Final price paid: ___
    - Target price: ___
    - Savings achieved: ___
    - Strategy effectiveness: ___

## Downloadable Resources (Printable PDFs)

### 1. Supply and Demand Graphing Practice Worksheet
- **Purpose:** Offline practice for students without device access
- **Format:** Printable PDF with blank graphs and scenarios
- **Content:**
  - 8 blank supply-demand graphs
  - 8 scenarios describing market changes
  - Students draw curve shifts and identify new equilibrium
  - Answer key on final page

### 2. Market Structure Quick Reference Card
- **Purpose:** Portable summary of market structures
- **Format:** Tri-fold card (printable on one sheet)
- **Content:**
  - Front: Perfect competition characteristics and examples
  - Middle: Oligopoly characteristics and examples
  - Back: Monopoly characteristics and examples
  - Inside: Consumer strategies for each market type
  - Wallet-sized when folded

### 3. Consumer Surplus Calculation Guide
- **Purpose:** Step-by-step guide for calculating surplus
- **Format:** Printable PDF with examples
- **Content:**
  - Formula: Consumer Surplus = Willingness to Pay - Price Paid
  - 5 worked examples with different scenarios
  - Practice problems with answer key
  - Visual representations of surplus as area on graph

### 4. Real Market Analysis Template (Print Version)
- **Purpose:** Offline version of Price Analysis Worksheet
- **Format:** Printable PDF (2 pages)
- **Content:** All sections from digital worksheet adapted for handwriting

### 5. Economic Decision-Making Flowchart
- **Purpose:** Visual guide for applying supply-demand analysis to purchases
- **Format:** Large-format poster (11x17) or standard printable
- **Content:**
  - Start: "Planning a purchase?"
  - Decision nodes:
    - What market structure? → Different paths
    - Supply high or low? → Different timing recommendations
    - Demand high or low? → Different strategies
  - End: Actionable recommendation
  - Examples at each decision point

## Asset Implementation Notes

### Technical Requirements
- All interactive tools must be:
  - Responsive (mobile-friendly)
  - Accessible (WCAG 2.1 AA compliant)
  - Fast-loading (< 3 seconds on 3G)
  - Browser-compatible (Chrome, Firefox, Safari, Edge)

### State-Specific Customization
- This chapter is Tier 3 (fully agnostic) - no state variables required
- Optional: Local examples can be added to scenarios (local businesses, regional markets)
- Market structure examples should use nationally recognized brands plus local options

### Data Sources
- Price data: Integrate APIs where available (Google Shopping, BLS CPI data)
- Market examples: Real companies and products, updated annually
- Scenarios: Based on actual economic events, updated with current examples

### Offline Accessibility
- Every interactive tool must have printable PDF alternative
- Worksheets designed for completion without technology
- Teacher can facilitate all activities without digital tools if necessary

### Student Data Privacy
- No personal financial data collected
- Research activities use hypothetical or public data only
- Optional: Save scenarios to local storage only (not server)

### Instructor Customization
- Teachers can add custom scenarios relevant to their region
- Editable templates allow for course-specific modifications
- Examples can be swapped for more relevant local alternatives

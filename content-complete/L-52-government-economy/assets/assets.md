# L-52: Government and the Economy - Personal Impact
## Assets and Resources Specification

This document specifies all interactive tools, downloadable materials, and additional resources for L-52.

---

## Interactive Tools (Skill Builders)

### 1. Policy Impact Analyzer Tool

**Purpose:** Systematic framework for analyzing any government policy

**Type:** Interactive decision tree and analysis template

**Location:** Embedded in Day 2, Activity 4

**Functionality:**

**Step 1: Policy Classification**
- Radio buttons for policy type:
  - Tax
  - Subsidy
  - Price control
  - Regulation
  - Public good provision
  - Redistribution

**Step 2: Market Failure Identification**
- Checkboxes for market failure types:
  - Monopoly
  - Externality
  - Public good
  - Information asymmetry
  - Inequality
  - None (not addressing market failure)

**Step 3: Winners and Losers Table**
- Input fields for stakeholder groups:
  - You personally
  - Your demographic
  - Taxpayers
  - Specific industry
  - Future generations
- For each: Win/Lose selection, magnitude estimate

**Step 4: Effectiveness Assessment**
- Radio buttons:
  - Yes, fully achieves goal
  - Partially achieves goal
  - No, does not achieve goal
  - Unclear/too soon to tell

**Step 5: Opportunity Cost**
- Text area: "What else could resources be used for?"
- Radio buttons: "Is this the best use?" (Yes/Maybe/No)

**Step 6: Recommendation**
- Radio buttons:
  - Support (benefits exceed costs)
  - Support with modifications (specify)
  - Oppose (costs exceed benefits)
  - Uncertain (need more information)
- Text area: Key evidence for position
- Slider: Confidence level (1-10)

**Output:**
- Generates structured policy analysis report
- Saves to user profile
- Can export as PDF
- AI feedback on analysis quality and completeness

**Technical Implementation:**
- React component with form state management
- localStorage for saving in-progress analysis
- Integration with Supabase for persistent storage
- PDF generation library for export
- AI integration for feedback (Claude API)

---

### 2. Tax Burden Calculator

**Purpose:** Calculate personal tax burden from income

**Type:** Interactive calculator

**Location:** Day 2, Activity 1, Part A

**Functionality:**

**Inputs:**
- Gross income (slider or text input: $0-$200,000)
- State selection (dropdown with all 50 states)
- Filing status (single, married filing jointly, etc.)
- Number of dependents

**Calculations:**
- Federal income tax (using current tax brackets)
- Social Security tax (6.2% up to wage base)
- Medicare tax (1.45%)
- State income tax (state-specific rates)
- Estimated sales tax (based on spending patterns)
- Property tax (optional, if homeowner)
- Gas tax (estimate based on driving)

**Output:**
- Total tax burden ($)
- Effective tax rate (%)
- Breakdown by category (pie chart)
- Comparison to {{STATE_NAME}} average
- Interactive visualization showing where money goes

**Technical Implementation:**
- JavaScript calculator with current year tax tables
- Chart.js for visualizations
- State tax data JSON file
- Responsive design for mobile

---

### 3. Government Services Value Estimator

**Purpose:** Estimate value of government services used

**Type:** Interactive checklist and calculator

**Location:** Day 2, Activity 1, Part B

**Functionality:**

**Service Categories:**
- Education (K-12, public university)
- Public safety (police, fire)
- Infrastructure (roads, bridges, public transit)
- Parks and recreation
- Libraries
- Healthcare (if applicable)
- Social services

**For each service:**
- Checkbox: Do you use this?
- Slider: How much do you use? (1-10 scale)
- Auto-calculates estimated private cost
- Shows comparison value

**Output:**
- Total value of services ($)
- Comparison to taxes paid
- Net recipient or net contributor status
- Visualization of services used (bar chart)
- Lifetime projection

**Technical Implementation:**
- React component with conditional rendering
- Service cost database (typical private costs)
- Chart.js for visualizations
- Age-based lifetime projection calculator

---

### 4. Cost-Benefit Analysis Framework

**Purpose:** Guide students through systematic policy evaluation

**Type:** Interactive worksheet with AI assistance

**Location:** Day 2, Activity 2

**Functionality:**

**6-Step Guided Process:**

**Step 1: Problem Identification**
- Text area: Describe the problem
- Dropdown: Select market failure type (if any)
- AI feedback on problem framing

**Step 2: Benefits Analysis**
- Add stakeholder groups (dynamic form)
- For each: Description of benefit, estimated value
- Total benefits calculation
- AI suggests additional beneficiaries to consider

**Step 3: Costs Analysis**
- Add stakeholder groups (dynamic form)
- For each: Description of cost, estimated value
- Total costs calculation
- AI suggests additional costs to consider

**Step 4: Unintended Consequences**
- Text area: List potential unintended consequences
- AI suggestions based on similar policies
- Historical examples database

**Step 5: Alternatives**
- Add alternative policies (dynamic form)
- For each: Description, estimated effectiveness
- Comparison table

**Step 6: Recommendation**
- Radio buttons: Implement/Modify/Reject
- Text area: Reasoning
- Slider: Confidence level (1-10)
- Text area: What information would increase confidence?

**Output:**
- Complete cost-benefit analysis report
- Comparison to expert analyses (if available)
- AI feedback on analysis quality
- Can save and share

**Technical Implementation:**
- Multi-step form with progress indicator
- AI integration (Claude API) for suggestions and feedback
- Database of example policies and outcomes
- Export to PDF functionality

---

### 5. Regulation Impact Analyzer

**Purpose:** Analyze specific regulations in detail

**Type:** Structured analysis template with research integration

**Location:** Day 2, Activity 3

**Functionality:**

**Input:**
- Select {{STATE_NAME}} (dropdown)
- Select regulation type (occupational licensing, environmental, zoning, etc.)
- Auto-loads specific regulations for that state

**Analysis Template:**
1. **What does regulation require?**
   - Pre-populated description (editable)
   - Links to official regulation text

2. **Intended problem**
   - Text area with AI suggestions

3. **Effectiveness**
   - Radio buttons: Yes/Partially/No
   - Text area: Evidence

4. **Costs (3 categories)**
   - To consumers
   - To businesses
   - To society
   - Each with text area and optional $ estimate

5. **Benefits**
   - Text area with AI suggestions

6. **Who's harmed/who benefits**
   - Text areas

7. **Verdict**
   - Radio buttons: Keep/Reform/Repeal
   - If Reform: Text area for proposed changes
   - Text area: Evidence supporting position

**Research Integration:**
- Links to state regulation databases
- Academic studies on regulation effectiveness (when available)
- Comparison to other states' approaches

**Output:**
- Complete regulation analysis report
- Comparison to expert opinions
- Reform proposal (if applicable)
- Can export as policy brief

**Technical Implementation:**
- State regulation database (JSON)
- External API integration for regulation text (regulations.gov)
- AI assistance for analysis
- Document export functionality

---

## Downloadable Materials

### Day 1 Materials

**1. Market Failures Reference Sheet**
- PDF summary of five market failures
- Examples of each
- Government solutions overview
- 2 pages, printable

**2. Supply & Demand with Government Policies Worksheet**
- Blank supply/demand graphs
- Practice problems: Draw effects of taxes, subsidies, price controls
- Answer key (separate file for teachers)
- 3 pages

**3. {{STATE_NAME}} Policy Overview**
- State-specific document with:
  - Tax rates (income, sales, property, gas)
  - Major regulations
  - Government services provided
  - Comparison to neighboring states
- Customized per state
- 4 pages

### Day 2 Materials

**4. Tax Burden Calculation Worksheet**
- Step-by-step guide to calculating personal tax burden
- Tables for federal and state taxes
- Space for students to fill in their calculations
- 2 pages, Excel and PDF versions

**5. Cost-Benefit Analysis Template**
- Blank template following 6-step framework
- Can be used for any policy
- Includes prompting questions
- 3 pages

**6. Regulation Analysis Template**
- Blank template for analyzing regulations
- Includes research questions and data sources
- 2 pages

**7. Policy Brief Writing Guide**
- Format and structure for policy briefs
- Examples of strong policy briefs
- Rubric for self-assessment
- 4 pages

**8. Political Economy Spectrum Handout**
- Visual representation of political economy philosophies
- Descriptions of each position
- Famous economists associated with each view
- 1 page, color

### Complete Chapter Package

**9. L-52 Complete Downloads (ZIP file)**
Contains all above materials plus:
- Glossary of key terms
- Discussion question cards (printable)
- Exit ticket templates
- Assessment rubrics

---

## Additional Resources

### Interactive External Tools

**1. Tax Foundation - State Tax Calculator**
- URL: https://taxfoundation.org/state-tax-calculator/
- Compare tax burdens across states
- Interactive tool with detailed breakdowns

**2. USA Government Budget Visualization**
- URL: https://www.usaspending.gov/
- Interactive visualization of federal spending
- See where tax dollars go

**3. Regulation Tracker**
- URL: https://www.reginfo.gov/
- Database of federal regulations
- Track new regulations and their economic impact

**4. State Policy Database**
- URL: State-specific legislative websites
- Custom links for each {{STATE_NAME}}
- Track state-level policies

### Curated Articles and Videos

**5. Market Failures Explained**
- Khan Academy video series on market failures
- 5-10 minute videos for each type
- Includes practice questions

**6. "I, Pencil" Essay**
- Classic essay by Leonard Read
- Illustrates complex market coordination
- Free online, 10-minute read

**7. Freakonomics Podcast: Government Policy Episodes**
- Episode: "How Much Does Government Really Cost You?"
- Episode: "Is College Worth It? A Data-Driven Answer"
- Episode: "Do Minimum Wage Increases Hurt Workers?"

**8. Tax Policy Center Resources**
- Nonpartisan analysis of tax policies
- State-specific data
- URL: https://www.taxpolicycenter.org/

**9. Brookings Institution & AEI Policy Analyses**
- Left-leaning (Brookings) and right-leaning (AEI) think tanks
- Compare analyses of same policy
- Shows how different values lead to different conclusions

### Academic Resources

**10. Journal of Economic Perspectives**
- Accessible academic articles on policy
- Free access for students
- URL: https://www.aeaweb.org/journals/jep

**11. NBER Working Papers**
- Latest economic research on policy impacts
- Summaries accessible to students
- URL: https://www.nber.org/papers

### {{STATE_NAME}}-Specific Resources

**12. {{STATE_NAME}} Legislative Website**
- Custom URL for each state
- Track bills and policy debates
- Contact representatives

**13. {{STATE_NAME}} Department of Revenue**
- Official tax information
- Forms and calculators
- Custom URL for each state

**14. {{STATE_NAME}} Budget Documents**
- See how state spends money
- Revenue sources
- Custom URL for each state

---

## Visual Assets

### Infographics

**1. Five Market Failures Infographic**
- Visual representation of each market failure
- Examples and solutions
- Suitable for classroom display
- Available in color and B&W

**2. How a Tax Affects Markets**
- Supply/demand diagram with tax
- Shows deadweight loss
- Color-coded for clarity

**3. Types of Government Intervention**
- Visual decision tree
- When to use taxes vs. subsidies vs. regulation
- Flowchart format

**4. Political Economy Spectrum**
- Visual continuum from market to government
- Famous economists and their positions
- Policy examples at each point

### Diagrams

**5. Tax Incidence Diagrams**
- Shows who really pays taxes (economic vs. legal incidence)
- Multiple examples (elastic vs. inelastic demand)

**6. Deadweight Loss from Price Controls**
- Rent control example
- Minimum wage example
- Shows shortage/surplus areas

**7. Externality Diagrams**
- Negative externality (pollution) with social cost curve
- Positive externality (education) with social benefit curve
- Shows optimal tax/subsidy

### Charts and Graphs

**8. State Tax Comparison Charts**
- Bar charts comparing {{STATE_NAME}} to other states
- Multiple tax types
- Updated annually

**9. Government Spending Breakdown**
- Pie chart of federal budget
- Pie chart of typical state budget
- Customizable for {{STATE_NAME}}

**10. Historical Regulation Trends**
- Line graph showing regulation growth over time
- By industry
- Shows regulation vs. deregulation periods

---

## Implementation Notes

### For Developers

**Interactive Tools:**
- All tools should be responsive (mobile-friendly)
- Save progress automatically (localStorage and Supabase)
- Include keyboard navigation and ARIA labels (accessibility)
- Provide print-friendly versions
- AI integration should be optional (work without if API unavailable)

**Downloadable Materials:**
- All PDFs should be ADA-compliant
- Provide both PDF and editable formats (Word, Excel)
- Include teacher answer keys as separate files
- Generate state-specific versions automatically

**External Resources:**
- Verify all URLs annually (links change)
- Provide archived versions if available
- Include "Last Checked" dates
- Have fallback resources if primary unavailable

### For Content Team

**State Customization:**
- All {{STATE_NAME}} variables must be replaced with actual state data
- Maintain database of state-specific information
- Update annually with new tax rates and regulations
- Verify accuracy with official state sources

**Currency:**
- Review all examples and data annually
- Update policy debates to reflect current issues
- Refresh video and article recommendations
- Archive outdated materials but keep accessible

### For Teachers

**Required Materials:**
- Policy Impact Analyzer (core skill builder)
- Tax Burden Calculator
- Cost-Benefit Analysis Framework
- Market Failures Reference Sheet
- {{STATE_NAME}} Policy Overview

**Optional Enhancements:**
- Additional curated resources based on current events
- Guest speaker from state legislature or policy organization
- Field trip to state capitol (if feasible)
- Policy debate or mock legislative session

---

## Assessment Assets

**1. Exit Ticket: Market Failure Identification**
- Describe one market failure you observe
- Identify which type
- Suggest government solution
- Evaluate if benefits exceed costs

**2. Policy Analysis Rubric**
- Scoring guide for cost-benefit analyses
- Criteria: problem identification, comprehensiveness, critical thinking, evidence use
- 4-point scale with descriptors

**3. Regulation Deep Dive Rubric**
- Scoring guide for regulation analyses
- Criteria: accuracy, depth of analysis, consideration of trade-offs
- 4-point scale with descriptors

**4. Chapter Assessment: Policy Evaluation**
- Comprehensive assessment of L-52 concepts
- Mix of multiple choice, short answer, and analysis questions
- Includes case study for application
- Answer key and rubric included

---

## Technical Specifications

### API Integrations

**Required:**
- Anthropic Claude API (for AI feedback and suggestions)
- Chart.js library (for visualizations)
- State tax data API (or JSON database)
- Supabase (for data persistence)

**Optional:**
- Regulations.gov API (for regulation text)
- USA Spending API (for federal budget data)
- State legislative APIs (varies by state)

### Data Requirements

**State Tax Data JSON Structure:**
```json
{
  "state": "STATE_NAME",
  "income_tax": {
    "type": "flat" | "progressive",
    "rates": [...]
  },
  "sales_tax": 0.05,
  "gas_tax": 0.30,
  "property_tax_avg": 5000,
  ...
}
```

**Regulation Database JSON Structure:**
```json
{
  "state": "STATE_NAME",
  "regulations": [
    {
      "id": "occ_license_cosmetology",
      "name": "Cosmetology Licensing",
      "type": "occupational_licensing",
      "hours_required": 1500,
      "fee": 5000,
      ...
    }
  ]
}
```

---

## Maintenance Schedule

**Monthly:**
- Verify external resource links
- Check for broken downloads
- Review AI feedback quality

**Quarterly:**
- Update policy examples with current debates
- Review and refresh video recommendations
- Check for new academic resources

**Annually:**
- Update all state tax data
- Refresh regulation information
- Review and update all downloadable PDFs
- Verify compliance with educational standards
- Update infographics and visual assets

---

## Accessibility Compliance

All assets must meet:
- WCAG 2.1 Level AA standards
- Screen reader compatibility
- Keyboard navigation support
- Color contrast requirements
- Alternative text for all images
- Captions for videos
- Downloadable materials in accessible formats

---

## Notes

- All dollar amounts should be clearly marked as "current year" or specific year
- Policy examples should be updated to reflect current debates
- State-specific content requires ongoing maintenance
- AI feedback should guide students without providing answers
- Balance between depth and accessibility for high school level
- Include both liberal and conservative perspectives on policy debates
- Emphasize evidence-based analysis over ideology

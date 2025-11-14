# L-60: Understanding Financial Contracts - Assets Specification

This document specifies all interactive tools, downloadable resources, and assets needed for L-60: Understanding Financial Contracts.

## Day 1 Assets

### 1. Contract Analysis Tool (Primary Skill Builder)

**Purpose:** Allows students to practice identifying essential contract elements, key terms, and red flags in four common financial contract types

**Format/Inputs:**
- Interactive web-based tool
- Presents four complete contract scenarios in readable format:
  1. Apartment lease agreement (residential rental)
  2. Cell phone service contract (mobile carrier agreement)
  3. Gym membership agreement (fitness facility)
  4. Personal loan contract (unsecured personal loan)
- For each contract, students interact with highlighting/marking tools to identify:
  - The five essential elements (offer, acceptance, consideration, capacity, legality)
  - Key financial terms (payment amounts, fees, interest rates, penalties)
  - Red flag clauses (automatic renewal, arbitration, liability limitations, etc.)
  - Termination provisions
  - Total cost calculation fields

**Expected Outputs:**
- Contract safety score (0-100) for each contract based on:
  - How consumer-friendly the terms are
  - How many red flags are present
  - Whether all essential elements are clear and fair
- Feedback on student's identification accuracy:
  - Elements correctly identified (green highlights)
  - Elements missed (yellow highlights with explanations)
  - Common red flags present in each contract
- Total cost calculation for each contract over its full term
- Suggested questions to ask before signing each type of contract

**Interaction Model:**
1. Student selects a contract type to analyze
2. Contract text displays in readable format with highlighting tools
3. Student uses color-coded markers to identify:
   - Blue: Offer
   - Green: Acceptance
   - Purple: Consideration
   - Orange: Capacity provisions
   - Yellow: Legality confirmation
   - Red: Red flag clauses
4. Student inputs numerical data in calculator fields:
   - Monthly payment amount
   - One-time fees
   - Potential penalties
   - Contract duration
5. Tool calculates total cost and generates safety score
6. Student receives immediate feedback on accuracy
7. Can compare safety scores across all four contract types
8. Can review missed elements with explanations

**Design Notes:**
- Contracts should be real or realistic (not obviously simplified)
- Text should be formatted as actual contracts appear (including fine print sections)
- Use actual legal language but ensure contracts are high-school readable
- Include visual indicators of where students have marked elements
- Progress bar shows completion (identified X of 5 essential elements, etc.)
- Final summary screen compares all four contracts side-by-side
- Mobile-responsive design for device flexibility
- Save/bookmark feature allows students to return to partially completed analysis
- Feedback should be educational, not just "correct/incorrect"

## Day 2 Assets

### 2. Contract Elements Finder (Activity 1 Tool)

**Purpose:** Rapid scavenger hunt game to identify the five essential contract elements in excerpts from six different real-world contracts

**Format/Inputs:**
- Interactive timed activity tool
- Presents contract excerpts (not full contracts, just relevant sections)
- Six contract types:
  1. Apartment lease
  2. Auto loan
  3. Credit card agreement
  4. Cell phone service
  5. Gym membership
  6. Employment offer letter
- Timer counts down (or up) to track speed
- Students mark text to identify elements

**Expected Outputs:**
- Accuracy score: X out of 30 elements correctly identified (5 elements × 6 contracts)
- Time to completion
- Comparison of student's performance across contract types (e.g., "You identified elements fastest in employment offers but struggled with credit card agreements")
- Feedback on each missed element explaining where it was and why it matters

**Interaction Model:**
1. Tool presents contract excerpt with five highlighting tools (one per element)
2. Student reads excerpt and marks where each element appears
3. When all five are marked (or student clicks "next"), tool shows feedback
4. Green checkmarks for correct identifications
5. Explanations for missed elements with highlighting showing correct location
6. Automatic progression to next contract type
7. Final summary dashboard showing overall accuracy and timing

**Design Notes:**
- Excerpts should be 1-2 paragraphs, not full contracts (focus on sections with elements)
- Clear visual distinction between the five highlighting tools
- Undo/redo functionality
- "Hint" button for struggling students (shows one element location)
- Leaderboard option for competitive classrooms (optional)
- Responsive design for various devices
- Timer can be turned off for students needing accommodations

### 3. Fine Print Analyzer (Activity 2 Tool)

**Purpose:** Three-round challenge to identify fees, red flags, and hidden obligations in contract fine print

**Format/Inputs:**
- Three-round interactive tool
- **Round 1 (Fee Identification):** Three contracts with all fees to find
  - Apartment lease with various fees scattered throughout
  - Gym membership with hidden ongoing costs
  - Personal loan with origination, late, and prepayment fees
- **Round 2 (Red Flag Detection):** 10-12 individual contract clauses to rate
  - Each clause presented separately
  - Student rates: Consumer Friendly / Minor Concern / Moderate Red Flag / Major Red Flag
- **Round 3 (Hidden Obligations):** Three contracts with obligations beyond payment
  - Insurance requirements
  - Maintenance responsibilities
  - Notice periods
  - Default triggers

**Expected Outputs:**
- **Round 1:** List of all fees found (with total), comparison to complete fee list, "missed fees" highlighting
- **Round 2:** Contract Literacy Score based on accurate red flag identification
- **Round 3:** Obligations checklist with student-identified items vs. complete list
- Final comprehensive score across all three rounds
- Personalized feedback on what types of clauses student tends to miss

**Interaction Model:**
**Round 1:**
1. Contract displays with fee-marking tool
2. Student clicks/highlights any text mentioning fees
3. Student enters fee amounts in running total calculator
4. Submit for feedback showing all fees highlighted (found and missed)
5. Tool explains significance of fees student missed

**Round 2:**
1. Individual clause displays
2. Student selects rating from slider or buttons
3. Tool reveals expert rating with explanation
4. Points awarded for matching expert assessment (or being within one level)
5. Progress through 10-12 clauses
6. Final score shows % accuracy in spotting red flags

**Round 3:**
1. Contract displays with obligation-marking tool
2. Student creates checklist of obligations beyond payment
3. Submit for comparison with complete obligation list
4. Feedback explains why missed obligations matter

**Design Notes:**
- Visual design should make fine print sections obvious (but realistic to contracts)
- Round 2 clauses should include both problematic and reasonable terms (not just red flags)
- Expert explanations should teach WHY a clause is/isn't concerning
- Scoring should reward accuracy, not just finding many items
- Summary dashboard compares performance across all three rounds
- Examples should come from real consumer contracts (anonymized)

### 4. Contract Comparison Tool (Activity 3 Tool)

**Purpose:** Side-by-side comparison of competing contract offers to determine best financial choice for different scenarios

**Format/Inputs:**
- Three comparison scenarios with complete contract details:

**Scenario 1: Apartment Leases**
- Apartment A details (rent, deposit, term, fees, restrictions)
- Apartment B details
- Apartment C details
- Calculator fields for different time periods

**Scenario 2: Auto Loan Offers**
- Lender A terms (APR, term, fees, prepayment rules)
- Lender B terms
- Lender C terms
- Loan amount: $25,000

**Scenario 3: Cell Phone Plans**
- Plan A details (monthly cost, contract term, device cost, termination fee)
- Plan B details
- Plan C details
- Analysis over 24 months

**Expected Outputs:**
For each scenario:
- Side-by-side comparison chart
- Total cost calculations for standard timeline
- Total cost calculations for early termination
- "Best for" recommendations:
  - Best for minimizing monthly payment
  - Best for lowest total cost
  - Best for flexibility
  - Best for specific circumstances
- Explanation of trade-offs between options
- Interactive sliders to adjust assumptions (e.g., "What if you stay 15 months instead of 12?")

**Interaction Model:**
1. Scenario presents three options in comparison table format
2. Student inputs calculations in provided fields:
   - Total monthly cost
   - Upfront costs
   - Total over standard period
   - Total if early termination at specified point
3. Tool verifies calculations (shows correct answers if student struggles)
4. Student selects "best option" for different goals (lowest cost, most flexible, etc.)
5. Tool provides feedback on selection with reasoning
6. Interactive slider allows student to explore "what if" scenarios
7. Move to next scenario when complete
8. Final summary compares all three scenarios

**Design Notes:**
- Comparison tables should be visually clear with color-coding
- Built-in calculator so students don't need external tools
- Show work/formula for calculations to teach process
- "What if" sliders should dynamically update calculations
- Summary should highlight key lesson from each scenario
- Printable summary option for students to keep
- Mobile-friendly responsive design

### 5. Contract Safety Checklist Builder (Activity 5 Tool)

**Purpose:** Students create a personalized contract review checklist to use for all future contracts

**Format/Inputs:**
- Interactive checklist builder with two categories:
  - **Essential Questions** (recommended for everyone)
  - **Customized Questions** (based on individual circumstances)
- Pre-written question bank organized by category:
  - Financial obligations and costs
  - Termination and flexibility
  - Rights and restrictions
  - Legal and dispute resolution
  - Contract modification terms
  - Default and remedies
- Customization prompts based on student's situation:
  - Life stage (high school, college, working, etc.)
  - Upcoming contract needs (apartment, job, phone, etc.)
  - Financial priorities (minimizing cost, maximizing flexibility, etc.)

**Expected Outputs:**
- Personalized checklist in printable format
- Digital version downloadable as PDF
- Mobile-friendly version that can be saved to phone
- Checklist includes:
  - Essential questions everyone should ask (8-10 items)
  - Student's customized questions (5-7 additional items)
  - Space to add notes for specific contracts
  - Section for contract details (date, parties, key terms)

**Interaction Model:**
1. Tool explains purpose of checklist
2. Presents essential questions with brief explanations
3. Student selects all essential questions (pre-checked, can be modified)
4. Tool asks about student's circumstances (upcoming contracts, priorities)
5. Recommends customized questions based on responses
6. Student selects which customized questions to include
7. Can add own custom questions in free-text fields
8. Preview checklist in formatted layout
9. Download as PDF, save to device, or email to self
10. Share with others (optional social feature)

**Design Notes:**
- Clean, professional checklist design suitable for real use
- Questions should be actionable and specific
- Include space for notes on each question
- Format should be practical for use on phone or printed
- Explanations for why each question matters (expandable/collapsible)
- Examples of good answers to questions
- Version for different contract types (lease checklist, loan checklist, etc.)
- QR code to return to digital version later

## Skill Builder Assets (Primary Interactive Tool)

### 6. Negotiation Scenario Cards (Activity 4 Materials)

**Purpose:** Role-play prompts for practicing contract negotiation in realistic scenarios

**Format/Inputs:**
- Four scenario card sets (digital or printable)
- Each card includes:
  - Scenario context (type of contract, problematic term)
  - Role A instructions (contract seeker perspective)
  - Role B instructions (contract holder perspective)
  - Negotiation objectives for each role
  - Background information both roles can see
  - Suggested talking points

**Scenarios:**
1. **Apartment Lease Early Termination**
   - Context: Tenant needs to break lease for job relocation
   - Problem: Two months' rent penalty
   - Negotiation: Reduce to one month or allow subletting

2. **Employment Non-Compete Clause**
   - Context: New employee offered job with restrictive non-compete
   - Problem: 2 years, 50-mile radius restriction
   - Negotiation: Reduce to 1 year, 25 miles, or limit to direct competitors only

3. **Gym Membership Long-Term Commitment**
   - Context: Customer wants to join gym but unsure of long-term plans
   - Problem: 12-month contract required, $500 early termination fee
   - Negotiation: Change to month-to-month, reduce fee, or pause option

4. **Loan Prepayment Penalty**
   - Context: Borrower wants flexibility to pay off loan early
   - Problem: 3% prepayment penalty for first 24 months
   - Negotiation: Eliminate penalty, reduce to 1%, or shorten period to 12 months

**Expected Outputs:**
- Practiced negotiation skills
- Experience with professional contract discussions
- Understanding of what's reasonable to negotiate
- Confidence to advocate for own interests

**Interaction Model:**
- Printed cards or digital display
- Students pair up and receive scenario
- Each reads their role (some information is shared, some is private)
- 3-minute role-play negotiation
- Switch roles and try again or try different scenario
- Class discussion of what worked

**Design Notes:**
- Roles should be realistic but not require legal expertise
- Include information about industry standards to ground negotiation
- Both sides should have legitimate interests (not one-sided)
- Include conversation starters for nervous students
- Suggest potential compromises if students get stuck
- Debrief questions on cards for after role-play

## Downloadable Resources (Printable PDFs)

### 7. Contract Analysis Worksheet (Printable Alternative)

**Purpose:** Printable worksheet for students to manually analyze contracts (technology backup or accessibility alternative)

**Contents:**
- Blank template with sections for:
  - Contract type identification
  - Five essential elements identification (with space to write where found)
  - Financial terms table (payments, fees, penalties)
  - Red flag checklist
  - Total cost calculation grid
  - Questions to ask before signing
- Can be used with any contract student encounters

**Format:** PDF, 2-3 pages, printable black-and-white

### 8. Contract Comparison Worksheet

**Purpose:** Manual tool for comparing competing contract offers

**Contents:**
- Side-by-side comparison table with rows for:
  - Monthly/periodic costs
  - Upfront costs
  - Contract term
  - Termination provisions and fees
  - Total cost over standard period
  - Total cost if early termination
  - Flexibility factors
  - Red flags identified
  - Best for [situation] analysis
- Calculation guides and formulas

**Format:** PDF, 2 pages, printable

### 9. Personal Contract Safety Checklist Template

**Purpose:** Printable version of checklist for students without digital access

**Contents:**
- Essential questions for all contracts (with checkboxes)
- Customizable question section (blank lines to add own)
- Space for contract-specific notes
- Example of completed checklist
- When to negotiate vs. accept terms guidance

**Format:** PDF, 1 page, printable, wallet-sized version also available

### 10. Contract Negotiation Guide

**Purpose:** Quick reference for professional contract negotiation

**Contents:**
- Preparation checklist (research, know your bottom line, etc.)
- Professional negotiation language examples
- "Do's and Don'ts" of contract negotiation
- When negotiation is most likely to succeed
- How to propose alternative contract language
- What to do if negotiation fails

**Format:** PDF, 1-2 pages, printable

### 11. Common Contract Red Flags Reference Sheet

**Purpose:** One-page guide to problematic contract clauses

**Contents:**
- List of common red flags with brief explanations:
  - Automatic renewal clauses
  - Unilateral modification rights
  - Arbitration requirements
  - Liability limitations
  - Excessive early termination fees
  - Prepayment penalties
  - Liquidated damages
  - Acceleration clauses
  - Confession of judgment
  - Mandatory add-ons
- For each red flag:
  - What it means
  - Why it's problematic
  - Questions to ask
  - Possible negotiation points

**Format:** PDF, 1 page front-and-back, printable

### 12. Sample Annotated Contracts

**Purpose:** Real contract examples with educational annotations showing elements and clauses

**Contents:**
- Four sample contracts (apartment lease, personal loan, gym membership, phone plan)
- Color-coded annotations showing:
  - Five essential elements highlighted
  - Financial terms circled
  - Red flags marked
  - Hidden obligations noted
  - Termination provisions boxed
- Explanatory notes in margins
- Summary analysis of each contract

**Format:** PDF, 8-12 pages total (2-3 pages per contract), printable

## Asset Production Notes

**Priority for Development:**
1. **Contract Analysis Tool** (Primary Skill Builder) - Essential for Day 1
2. **Contract Comparison Tool** - Core of Day 2 Activity 3
3. **Fine Print Analyzer** - Day 2 Activity 2, teaches crucial skill
4. **Contract Elements Finder** - Day 2 Activity 1, foundation skill
5. **Contract Safety Checklist Builder** - Practical takeaway tool
6. **Negotiation Scenario Cards** - Can use printed cards if digital not ready
7. **Printable Resources** - Accessibility alternatives, lower priority if digital tools work

**Accessibility Considerations:**
- All interactive tools should have keyboard navigation
- Screen reader compatibility for visually impaired students
- Printable alternatives for all digital tools
- Adjustable text size and contrast options
- No time-pressure requirements for students needing accommodations
- Color-blind friendly color schemes (not relying solely on color to convey information)

**Technical Requirements:**
- Web-based tools (no installation required)
- Mobile-responsive design
- Works on tablets, phones, and computers
- No login required for basic functionality (optional account for saving progress)
- Offline printable versions available
- Fast loading even on slower internet connections

**State-Specific Considerations:**
This chapter is largely state-agnostic (Tier 3). However, for future state customization potential:
- Sample contracts could be modified to reflect state-specific laws (e.g., California lease with CA-specific provisions)
- Checklist Builder could include state-specific questions (e.g., "Does this non-compete comply with California law?")
- Currently, use generic contracts that work for any state, acknowledging that "specific laws vary by state"

## Assessment Integration

**Data Collection for Teacher Dashboard:**
- Contract Analysis Tool: Track accuracy of element identification, time spent, safety scores
- Contract Comparison Tool: Track calculation accuracy, decision-making quality
- Fine Print Analyzer: Track red flag identification accuracy, common missed items
- Checklist Builder: Track which questions students prioritize (indicates their concerns)

**Formative Assessment Opportunities:**
- Real-time feedback during all interactive tools
- Teacher dashboard showing class-wide patterns (e.g., 70% of students missed arbitration clauses)
- Individual student progress reports

**Summative Assessment Option:**
- Final contract analysis activity using the primary tool
- Score based on accuracy across all skills (element identification, red flag spotting, cost calculation, etc.)

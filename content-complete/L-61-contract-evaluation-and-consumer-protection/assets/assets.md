# L-61: Contract Evaluation and Consumer Protection - Assets Specification

## Day 1 Assets

### 1. Contract Comparison Visual Chart
**Purpose:** Side-by-side comparison of consumer rights vs. common contract restrictions

**Format:** Interactive table

**Outputs:**
- Consumer rights by category (warranties, termination, privacy, etc.)
- Common contract clauses that attempt to limit those rights
- Enforceability status (upheld, limited, or unenforceable)

**Design:** Color-coded (green=your rights protected, yellow=limited, red=often waived)

---

### 2. Red Flag Language Database
**Purpose:** Searchable database of problematic contract phrases

**Inputs:** Contract text or specific clause

**Outputs:**
- Red flag classification (high/medium/low concern)
- Explanation of why it's problematic
- Typical consumer impact
- Negotiation strategies

**Categories:** Liability waivers, termination, arbitration, renewal, fees, modification rights

---

## Day 2 Assets (Learning Lab)

### 1. Contract Analyzer (Primary Skill Builder)
**Purpose:** Comprehensive contract analysis tool

**Section A: Contract Upload/Review**
- Upload contract or select from sample library (lease, gym, cell phone, employment)
- Tool highlights key sections automatically
- Guides systematic review process

**Section B: Clause-by-Clause Analysis**
For each major clause:
- Classify: Reasonable / Concerning / Red Flag
- Explain reasoning
- Reference relevant consumer protection laws
- Determine enforceability likelihood

**Section C: Risk Assessment**
- Overall contract fairness score (1-10)
- Identification of highest-risk clauses
- Total cost calculation (all fees over contract term)
- Comparison to industry standards

**Section D: Negotiation Recommendations**
- Priority clauses to negotiate (ranked by impact)
- Suggested alternative language
- Negotiation scripts and strategies
- Walk-away triggers (when to decline)

**Interaction:** Progressive disclosure—students analyze section by section with feedback before proceeding

---

### 2. Consumer Rights Database
**Purpose:** Searchable reference for federal and state consumer protection laws

**Inputs:**
- Scenario description or contract type
- State selection

**Outputs:**
- Applicable federal laws (FTC Act, TILA, Magnuson-Moss, etc.)
- State-specific consumer protections
- Cooling-off periods
- Enforcement agencies and complaint procedures

**Design:** Case-based search ("landlord won't return deposit") plus legal citation search

---

### 3. Real Contract Library
**Purpose:** Collection of actual contracts for analysis practice

**Contracts Included:**
1. Apartment lease (8 pages) with mixed terms
2. Gym membership agreement with automatic renewal
3. Cell phone service contract with arbitration clause
4. Employment contract with non-compete
5. Online service terms of service
6. Auto financing agreement
7. Extended warranty contract
8. Timeshare presentation contract

**Features:**
- Annotated versions available (highlights key clauses)
- Plain-text versions for independent analysis
- State-specific variations where applicable

---

### 4. Negotiation Simulator
**Purpose:** Practice negotiating contract terms in realistic scenarios

**Format:** Interactive role-play with AI or scripted responses

**Scenarios:**
1. Negotiating lease terms with landlord
2. Attempting to remove arbitration clause from service contract
3. Negotiating employment non-compete duration/scope
4. Requesting early termination fee reduction

**For Each:**
- Student chooses negotiation approach from options
- System responds based on choice quality
- Feedback on effectiveness
- Multiple attempts allowed

**Outcomes:** Successful negotiation, partial success, rejection, or lose deal

---

### 5. Fee Calculator & Hidden Cost Identifier
**Purpose:** Calculate true costs of contracts with complex fee structures

**Inputs:**
- Advertised price
- Contract term length
- All fees (itemized)
- Interest rates (if applicable)

**Outputs:**
- True monthly cost (all fees included)
- Total cost over contract term
- Cost comparison to advertised price ("They said $20/month; you'll actually pay $35/month")
- Annual percentage rate (if financing)

**Examples:** Gym memberships, cell plans, subscription services, rent-to-own agreements

---

## Printable Resources

### 1. Contract Evaluation Checklist
**Format:** 2-page PDF worksheet

**Sections:**
- [ ] Parties and obligations identified
- [ ] All financial terms understood (total cost calculated)
- [ ] Termination procedures and fees noted
- [ ] Modification rights reviewed
- [ ] Liability allocation analyzed
- [ ] Dispute resolution examined
- [ ] Consistency with promises verified

Space for notes on each section.

---

### 2. Consumer Protection Laws Reference Sheet
**Format:** 4-page PDF (federal laws + state template)

**Content:**
- FTC Act (deceptive practices)
- Truth in Lending Act (credit disclosures)
- Magnuson-Moss (warranties)
- Fair Credit Reporting Act
- State-specific laws (template for customization)
- Enforcement agency contact information

---

### 3. Negotiation Strategy Templates
**Format:** 3-page PDF with fill-in scripts

**Templates:**
1. Lease term negotiation script
2. Fee reduction request script
3. Clause removal/amendment request script

Each includes:
- Opening (express interest)
- Specific concern identification
- Proposed solution
- Justification (fairness/market standard)
- Request for amendment

---

### 4. Red Flag Quick Reference Card
**Format:** 1-page laminated card

**Content:** Top 10 red flag phrases:
1. "As-is" / "No warranty"
2. "Non-refundable"
3. "Binding arbitration"
4. "Automatic renewal"
5. "Company may modify terms at any time"
6. "Customer waives all claims"
7. "Not responsible for any damages"
8. "Perpetual license"
9. "Company may terminate without cause"
10. "Customer indemnifies Company"

Brief explanation of each.

---

## Technical Requirements

### Data Requirements
- Sample contract library (8+ complete contracts)
- Consumer protection law database (federal + 50 states)
- Red flag language library (500+ problematic clauses)
- Negotiation response library (100+ scenarios)

### Calculation Accuracy
- Fee totaling (must handle complex structures)
- APR calculation (for financing contracts)
- Prorated refund calculations (early termination scenarios)

### Accessibility
- WCAG 2.1 AA compliance
- Screen reader compatible
- Printable versions of all tools
- Mobile-responsive design

---

**Development Priority:**
1. Contract Analyzer (primary skill builder)
2. Consumer Rights Database
3. Real Contract Library
4. Printable resources
5. Negotiation Simulator (if time/budget permits)

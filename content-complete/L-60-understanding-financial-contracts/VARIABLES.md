# L-60 State-Specific Variables

This document lists template variables for L-60: Understanding Financial Contracts.

## State-Agnostic Classification

**L-60 is primarily a Tier 3 (Fully Agnostic) chapter.** Contract law principles are largely universal across all states, with core concepts applying everywhere:
- The five essential elements (offer, acceptance, consideration, capacity, legality) are consistent
- Contract interpretation principles are similar
- Common contract types (leases, loans, service agreements) exist in all states
- Red flag clauses appear in contracts nationwide

## Minor State Variations

While the chapter is largely universal, some minor state-specific variations exist that could optionally be referenced:

### Legal Variables (Optional)

| Variable | Description | Typical Range | Example (Texas) |
|----------|-------------|---------------|-----------------|
| `{{STATE_AGE_OF_MAJORITY}}` | Legal age to enter binding contracts | 18-21 years | 18 |
| `{{STATE_NAME}}` | Full state name for context | N/A | Texas |

### State-Specific Contract Law Variations

**Age of Majority:**
- Most states: 18 years
- Alabama, Nebraska: 19 years
- Mississippi: 21 years

**Non-Compete Clause Enforceability:**
- California: Generally unenforceable
- Most states: Enforceable if reasonable in scope, duration, and geographic area
- Varies significantly by state

**Landlord-Tenant Law:**
- Security deposit limits vary (some states cap at 1-2 months' rent)
- Notice requirements for lease termination vary
- Habitability standards differ
- These affect lease contracts but are specific to rental agreements

**Consumer Protection Laws:**
- Some states have "cooling-off periods" allowing contract cancellation within specified timeframes
- State-specific consumer protection statutes vary
- Some states require specific disclosures in certain contract types

## Teaching Approach for State Variations

**Recommended pedagogical approach:**

1. **Teach universal principles first**: The five essential elements, common contract types, and how to read and interpret contracts apply everywhere

2. **Acknowledge variation where relevant**: When discussing specific laws (age of majority, non-compete rules), use phrasing like:
   - "In most states, the age of majority is 18..."
   - "Contract law varies by state in some areas. For example, non-compete clauses are generally unenforceable in California but are enforceable in most other states if they're reasonable."
   - "When you're signing a real contract—especially for housing or employment—check your state's specific laws."

3. **Encourage research for real contracts**: Direct students to research their state's specific regulations when they're actually facing a contract decision, rather than teaching all 50 states' variations in class

4. **Focus on transferable skills**: The skills taught in L-60 (reading carefully, identifying red flags, calculating total cost, negotiating terms) work for contracts anywhere

## Variable Usage in Content

**Current implementation:**
L-60 content uses minimal state variables because contract literacy principles are universal. The chapter occasionally references that "laws vary by state" to acknowledge variation without getting into state-specific details that would make the content less transferable.

**For future state-specific customization:**
If needed, these variables could be added to provide state-specific examples:
- `{{STATE_SECURITY_DEPOSIT_LIMIT}}` - Maximum security deposit allowed (for lease examples)
- `{{STATE_NON_COMPETE_ENFORCEABLE}}` - Whether non-competes are generally enforceable (boolean or description)
- `{{STATE_CONSUMER_PROTECTION_URL}}` - Link to state attorney general or consumer protection office
- `{{STATE_LANDLORD_TENANT_LAW_URL}}` - Link to state-specific rental law resources
- `{{STATE_CONTRACT_LAW_RESOURCES}}` - State bar association or legal aid resources

**Current assessment:** These variables are **NOT necessary** for the initial template because:
1. The chapter teaches universal contract literacy skills
2. State variations are acknowledged conceptually without needing specific data
3. Students are directed to research their specific state when facing real contracts
4. Examples use generic contract terms that apply anywhere

## Data Layer Preparation (Phase 2)

If state-specific data layers are created in the future, the following information would be useful:

```json
{
  "state_name": "Texas",
  "state_code": "TX",
  "age_of_majority": 18,
  "non_compete_generally_enforceable": true,
  "security_deposit_limit_description": "No statutory limit, but must be reasonable",
  "landlord_tenant_law_url": "https://www.texasattorneygeneral.gov/consumer-protection/home-real-estate-and-travel/renters-rights",
  "consumer_protection_url": "https://www.texasattorneygeneral.gov/consumer-protection",
  "state_bar_url": "https://www.texasbar.com/",
  "notes": "Texas contract law is generally consistent with national principles. Non-compete clauses are enforceable if reasonable. No specific consumer protection laws significantly alter contract literacy education needs."
}
```

## Bottom Line

**L-60 does not require state-specific variables for effective implementation.** The chapter teaches universal contract literacy skills that apply to contracts everywhere. State variations are acknowledged conceptually, and students are encouraged to research their specific state's laws when facing real contract decisions.

This makes L-60 highly efficient: one template serves all 50 states without modification.

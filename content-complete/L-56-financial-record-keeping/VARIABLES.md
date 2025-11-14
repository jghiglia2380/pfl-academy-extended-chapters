# L-56: Financial Record Keeping - State Variables Documentation

## Overview
L-56 is classified as **Tier 2** in the state-specific content analysis, meaning it benefits from state-specific examples and localization while maintaining universally applicable core content. This chapter primarily teaches universal financial record-keeping principles, but references to local banking costs, consumer protection resources, and regulations enhance relevance and practicality for students.

## State Variables Used

| Variable Name | Description | Typical Range | Example Value |
|---------------|-------------|---------------|---------------|
| `{{STATE_NAME}}` | Full name of the state | N/A | Texas |
| `{{STATE_CODE}}` | Two-letter state abbreviation | N/A | TX |
| `{{STATE_AVG_OVERDRAFT_FEE}}` | Average overdraft fee charged by banks in the state | $25-40 | $32.50 |
| `{{STATE_AVG_MONTHLY_FEE}}` | Average monthly maintenance fee for checking accounts | $0-15 | $8.00 |
| `{{STATE_CONSUMER_PROTECTION_AGENCY}}` | Name of state consumer protection agency | Varies by state | Texas Attorney General Consumer Protection Division |
| `{{STATE_CONSUMER_PROTECTION_URL}}` | URL for state consumer protection resources | Varies by state | https://www.texasattorneygeneral.gov/consumer-protection |
| `{{STATE_MINOR_BANKING_RULES}}` | State-specific rules about minors opening bank accounts | Varies by state | Minors under 18 may open accounts with parental co-signature |
| `{{STATE_BANKING_DEPARTMENT_URL}}` | URL for state banking regulatory agency | Varies by state | https://www.dob.texas.gov/ |

## Variable Usage Locations

### Student Content (day1.md)
- **No direct state variables** - Content is intentionally universal, focusing on principles that apply regardless of location
- Could optionally add state-specific examples in real-world scenarios if desired

### Student Content (day2.md)
- **No direct state variables** - Learning Lab activities are designed to work in any state
- Scenarios use generic financial institutions and examples

### Teacher Guide (guide-day1.md)
**State-Specific Customization Section includes:**
- `{{STATE_AVG_OVERDRAFT_FEE}}` - For discussing cost of poor record-keeping
- `{{STATE_CONSUMER_PROTECTION_URL}}` - Resource for fraud reporting
- `{{STATE_MINOR_BANKING_RULES}}` - Information about student banking access

**Example usage in guide-day1.md:**
```markdown
"In {{STATE_NAME}}, the average overdraft fee charged by major banks is {{STATE_AVG_OVERDRAFT_FEE}}."

"If you experience fraud in {{STATE_NAME}}, you can report it to {{STATE_CONSUMER_PROTECTION_AGENCY}} at {{STATE_CONSUMER_PROTECTION_URL}}."

"In {{STATE_NAME}}, {{STATE_MINOR_BANKING_RULES}}."
```

### Teacher Guide (guide-day2.md)
**State-Specific Teaching Notes Section includes:**
- `{{STATE_NAME}}` - For contextualizing examples
- `{{STATE_AVG_OVERDRAFT_FEE}}` - For calculating real costs in scenarios
- `{{STATE_CONSUMER_PROTECTION_AGENCY}}` - Resource sharing
- `{{STATE_CONSUMER_PROTECTION_URL}}` - Fraud reporting information

**Example usage in guide-day2.md:**
```markdown
"In {{STATE_NAME}}, the average overdraft fee is {{STATE_AVG_OVERDRAFT_FEE}}. If you overdrew your account three times in one day, that would cost you {{STATE_AVG_OVERDRAFT_FEE * 3}}."
```

### Assets (assets.md)
**Asset customization notes include:**
- `{{STATE_AVG_OVERDRAFT_FEE}}` - For realistic scenario amounts in simulator
- `{{STATE_AVG_MONTHLY_FEE}}` - For bank fee examples
- `{{STATE_CONSUMER_PROTECTION_URL}}` - Links in fraud reporting resources
- Local bank names can be customized for examples

## Implementation Strategy

### Agnostic Core + State Enhancement Pattern
This chapter follows the recommended pattern of providing universally applicable core content enhanced with state-specific details:

**Universal Core Concepts:**
- Importance of financial record-keeping (applies everywhere)
- How to read a bank statement (standard across all banks nationally)
- Checkbook balancing process (same methodology regardless of location)
- Common errors and how to fix them (universal challenges)
- Fraud detection principles (fraudsters operate everywhere)

**State-Specific Enhancements:**
- Local cost data (overdraft fees, monthly fees) makes examples more relevant
- State consumer protection resources provide actionable local support
- State banking regulations inform students about their specific rights and options
- Local bank names in examples increase familiarity and applicability

### Content Works Without State Data
All student-facing content is designed to be fully functional and educational even if state variables are not populated. The core learning objectives can be achieved with generic examples and national averages. State-specific information adds value but is not required for comprehension.

**Example:**
- Without state data: "Overdraft fees typically range from $25-40 per transaction nationally."
- With state data: "In {{STATE_NAME}}, the average overdraft fee is {{STATE_AVG_OVERDRAFT_FEE}}."

Both versions teach the concept; the state-specific version is more personally relevant.

## Data Sources for State Variables

### Recommended Sources for Populating Variables:

**Banking Fee Data:**
- Bankrate.com state-specific fee surveys
- Consumer Financial Protection Bureau (CFPB) reports
- State banking department annual reports
- Survey of major banks operating in the state

**Consumer Protection Resources:**
- State Attorney General website
- State consumer protection division
- Better Business Bureau state office
- State banking regulatory agency

**Minor Banking Regulations:**
- State banking code/statutes
- State financial institutions department
- Major bank policies in the state
- Legal resources on state banking laws

## Updating State Variables

### Recommended Update Frequency

**Annually:**
- `{{STATE_AVG_OVERDRAFT_FEE}}` - Banking fees change periodically
- `{{STATE_AVG_MONTHLY_FEE}}` - Account fees may be adjusted
- `{{STATE_CONSUMER_PROTECTION_URL}}` - Verify links are still active

**As Needed:**
- `{{STATE_MINOR_BANKING_RULES}}` - Update if state laws change
- `{{STATE_CONSUMER_PROTECTION_AGENCY}}` - Update if agency name changes or is restructured
- `{{STATE_BANKING_DEPARTMENT_URL}}` - Verify link functionality

### Data Maintenance Process
1. Assign responsibility for annual review of state-specific data
2. Document sources used for each variable value
3. Set calendar reminders for annual updates
4. Verify all URLs are functional
5. Update values in state data JSON files
6. Test that updated content renders correctly

## Cross-Chapter Variable Consistency

### Variables Shared Across Multiple L-Chapters
These variables are used consistently across different chapters:

**From L-46 (Automobile Finance):**
- `{{STATE_NAME}}` - Same usage
- `{{STATE_CODE}}` - Same usage
- `{{STATE_CONSUMER_PROTECTION_URL}}` - Same resource

**From L-59 (Local Tax Structures):**
- `{{STATE_NAME}}` - Same usage
- Consumer protection resources - Related but different focus

### New Variables Introduced in L-56
The following variables are new to this chapter and may be useful for other financial literacy lessons:
- `{{STATE_AVG_OVERDRAFT_FEE}}` - Could be used in any lesson discussing checking accounts or banking costs
- `{{STATE_AVG_MONTHLY_FEE}}` - Useful for banking and budgeting lessons
- `{{STATE_MINOR_BANKING_RULES}}` - Relevant for any lesson on opening bank accounts or student financial access
- `{{STATE_BANKING_DEPARTMENT_URL}}` - General resource for banking-related content

## Technical Implementation Notes

### Variable Format in Content
All state variables use the double-curly-brace format:
```markdown
{{VARIABLE_NAME}}
```

### Calculated Variables
Some variables may need calculation based on other variables:
```markdown
Total cost of three overdrafts: {{STATE_AVG_OVERDRAFT_FEE * 3}}
```

### Conditional Logic (if needed)
If certain content should only appear for specific states:
```markdown
{{#if STATE_HAS_SPECIFIC_BANKING_LAW}}
In {{STATE_NAME}}, there is a specific law regarding...
{{else}}
Most states follow standard federal banking regulations...
{{/if}}
```

### Default Values
If state-specific data is unavailable, fallback to national averages:
- Overdraft fee: $32.50 (national average)
- Monthly maintenance fee: $5.00 (national average)
- Consumer protection: Link to federal CFPB resources

## Privacy and Data Considerations

### No Personal Financial Data
This chapter's state variables contain only:
- Aggregate statistical data (averages, typical ranges)
- Public resource URLs
- General policy information

**No personal or sensitive information is included in state variables.**

### Publicly Available Information
All state-specific data comes from public sources:
- Government websites
- Published surveys and reports
- Public banking regulations
- Consumer protection agencies

## Special Considerations for L-56

### Why L-56 is Tier 2 (Not Tier 3)
While financial record-keeping principles are universal, state-specific information enhances this chapter because:

1. **Banking costs vary significantly by state** - Knowing actual local fees makes consequences more tangible
2. **Consumer protection resources are state-specific** - Students need local contacts for fraud reporting
3. **Banking regulations differ by state** - Student access to banking services varies
4. **Local context increases engagement** - Recognizing local bank names and resources improves relevance

### Why L-56 is Not Tier 1
This chapter is not Tier 1 (requires state content) because:
- Core concepts apply universally
- Reconciliation process is identical regardless of location
- All learning objectives can be achieved without state-specific data
- State information enhances but doesn't fundamentally change the content

## Example State Data JSON Structure

```json
{
  "state_code": "TX",
  "state_name": "Texas",
  "banking": {
    "avg_overdraft_fee": 32.50,
    "avg_monthly_fee": 8.00,
    "minor_banking_rules": "Minors under 18 may open accounts with parental co-signature",
    "banking_department_url": "https://www.dob.texas.gov/"
  },
  "consumer_protection": {
    "agency_name": "Texas Attorney General Consumer Protection Division",
    "url": "https://www.texasattorneygeneral.gov/consumer-protection",
    "fraud_hotline": "1-800-621-0508"
  }
}
```

## Version History

**Version 1.0** (November 13, 2025)
- Initial documentation of state variables for L-56
- Identified 8 state-specific variables used across teacher guides
- Established Tier 2 classification with agnostic core + state enhancement pattern
- Created recommended data sources and update procedures

---

**Last Updated:** November 13, 2025
**Chapter:** L-56 - Financial Record Keeping and Account Reconciliation
**Tier Classification:** Tier 2 (Benefits from state-specific examples)
**Total Variables Documented:** 8

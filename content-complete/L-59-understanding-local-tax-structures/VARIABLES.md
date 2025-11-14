# L-59 State-Specific Variables

This document lists all template variables used in L-59 that require state-specific data. This chapter is heavily state-specific (Tier 1) as local tax structures vary dramatically by state.

---

## Core State Identification

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_NAME}}` | Full state name | Texas |
| `{{STATE_CODE}}` | Two-letter state code | TX |

---

## Property Tax Variables

### Assessment and Exemptions

| Variable | Description | Typical Range | Example (Texas) |
|----------|-------------|---------------|-----------------|
| `{{STATE_ASSESSMENT_PERCENTAGE}}` | Percentage of market value used as assessed value | 50-100% | 100 |
| `{{STATE_HOMESTEAD_EXEMPTION}}` | Homestead exemption amount for primary residences ($) | $0-$50,000 | $40,000 |
| `{{STATE_PROPERTY_ASSESSMENT_FREQUENCY}}` | How often properties are reassessed | annually, every 2-3 years | annually |

### Millage Rates by Authority

| Variable | Description | Typical Range | Example (Texas) |
|----------|-------------|---------------|-----------------|
| `{{STATE_PROPERTY_TAX_COUNTY_RATE}}` | County property tax rate (mills) | 5-20 mills | 8.5 |
| `{{STATE_PROPERTY_TAX_CITY_RANGE}}` | Range of city rates across state (mills) | "5-25 mills" | "8-18 mills" |
| `{{STATE_PROPERTY_TAX_SCHOOL_RATE}}` | Typical school district rate (mills) | 15-35 mills | 22 |
| `{{STATE_PROPERTY_TAX_SPECIAL_RATE}}` | Special district rates (mills) | 1-5 mills | 2.5 |
| `{{STATE_TOTAL_MILLAGE_EXAMPLE}}` | Example total millage for calculations | 25-50 mills | 35 |

### Specific Jurisdiction Rates

| Variable | Description | Typical Range | Example (Texas) |
|----------|-------------|---------------|-----------------|
| `{{STATE_HIGH_TAX_CITY}}` | Name of high-tax city for examples | - | Austin |
| `{{STATE_HIGH_TAX_MILLAGE}}` | Millage rate for high-tax city | 35-50 mills | 42 |
| `{{STATE_MEDIUM_TAX_CITY}}` | Name of medium-tax city | - | Fort Worth |
| `{{STATE_MEDIUM_TAX_MILLAGE}}` | Millage rate for medium-tax city | 25-35 mills | 31 |
| `{{STATE_LOW_TAX_CITY}}` | Name of low-tax city/area | - | Fredericksburg |
| `{{STATE_LOW_TAX_MILLAGE}}` | Millage rate for low-tax city | 15-25 mills | 22 |

### Major Jurisdictions for Day 2 Activities

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_MAJOR_CITY_1}}` | Largest city | Houston |
| `{{STATE_MAJOR_CITY_1_MILLAGE}}` | City 1 millage rate (mills) | 38 |
| `{{STATE_MAJOR_CITY_2}}` | Second major city | Dallas |
| `{{STATE_MAJOR_CITY_2_MILLAGE}}` | City 2 millage rate (mills) | 36 |
| `{{STATE_MAJOR_CITY_3}}` | Third major city | San Antonio |
| `{{STATE_MAJOR_CITY_3_MILLAGE}}` | City 3 millage rate (mills) | 33 |
| `{{STATE_SUBURB_1}}` | Example suburban area | Plano |
| `{{STATE_SUBURB_1_MILLAGE}}` | Suburb 1 millage rate (mills) | 35 |
| `{{STATE_SUBURB_2}}` | Second suburban area | Frisco |
| `{{STATE_SUBURB_2_MILLAGE}}` | Suburb 2 millage rate (mills) | 34 |
| `{{STATE_RURAL_AREA}}` | Rural area example | Kerr County |
| `{{STATE_RURAL_AREA_MILLAGE}}` | Rural area millage rate (mills) | 24 |

### Tax Cap and Limitations

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_HAS_TAX_CAP}}` | Boolean - does state have tax caps? | true |
| `{{STATE_TAX_CAP_DESCRIPTION}}` | Description of cap if applicable | "10% annual increase cap on primary residences" |

---

## Sales Tax Variables

| Variable | Description | Typical Range | Example (Texas) |
|----------|-------------|---------------|-----------------|
| `{{STATE_SALES_TAX}}` | State sales tax rate (%) | 0-10% | 6.25 |
| `{{STATE_LOCAL_SALES_TAX_MIN}}` | Minimum local sales tax (%) | 0-2% | 0.5 |
| `{{STATE_LOCAL_SALES_TAX_MAX}}` | Maximum local sales tax (%) | 0-5% | 2.0 |
| `{{STATE_COMBINED_SALES_TAX_MIN}}` | Minimum combined state + local (%) | 0-8% | 6.75 |
| `{{STATE_COMBINED_SALES_TAX_MAX}}` | Maximum combined state + local (%) | 5-11% | 8.25 |

### Specific Jurisdiction Sales Tax Rates

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_HIGH_LOCAL_SALES_TAX}}` | High local sales tax rate (%) | 2.0 |
| `{{STATE_MEDIUM_LOCAL_SALES_TAX}}` | Medium local sales tax rate (%) | 1.5 |
| `{{STATE_LOW_LOCAL_SALES_TAX}}` | Low local sales tax rate (%) | 0.5 |
| `{{STATE_LOCAL_SALES_TAX_1}}` | Major City 1 local rate (%) | 1.0 |

### Combined Sales Tax Examples

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_HIGH_COMBINED_SALES_TAX}}` | High combined rate example (%) | 8.25 |
| `{{STATE_LOW_COMBINED_SALES_TAX}}` | Low combined rate example (%) | 6.75 |

---

## Local Income Tax Variables

| Variable | Description | Example (No Local Tax State) | Example (Local Tax State) |
|----------|-------------|------------------------------|---------------------------|
| `{{STATE_ALLOWS_LOCAL_INCOME_TAX}}` | Boolean - local income tax allowed? | false | true |
| `{{STATE_LOCAL_INCOME_TAX_RANGE}}` | Range of local income tax rates | N/A | "1.0% to 3.0%" |
| `{{STATE_LOCAL_INCOME_TAX_EXAMPLE}}` | Example with specific city | N/A | "New York City charges 3.078%" |
| `{{STATE_HIGH_LOCAL_INCOME_TAX_RATE}}` | Highest local rate in state (%) | 0 | 3.078 |
| `{{STATE_LOW_LOCAL_INCOME_TAX_RATE}}` | Lowest local rate in state (%) | 0 | 1.0 |
| `{{STATE_LOCAL_INCOME_TAX_RATE_1}}` | Major City 1 local income tax (%) | 0 | 2.0 |

---

## Geographic Identifiers

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_COUNTY_NAME}}` | Example county used in lessons | Harris |
| `{{STATE_MAJOR_CITY}}` | Primary city for examples | Houston |

---

## State Resources and URLs

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_PROPERTY_TAX_LOOKUP_URL}}` | URL to look up property tax bills | https://hcad.org |
| `{{STATE_COUNTY_TAX_ASSESSOR_URL}}` | County assessor website | https://www.hcad.org |
| `{{STATE_DMV_URL}}` | State DMV or equivalent | https://www.txdmv.gov |
| `{{STATE_CONSUMER_PROTECTION_URL}}` | Consumer protection resources | https://www.texasattorneygeneral.gov |

---

## Assessment Appeal Process

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_ASSESSMENT_APPEAL_DEADLINE}}` | Deadline to file property tax appeal | May 15 or 30 days after notice |
| `{{STATE_ASSESSMENT_APPEAL_PROCESS}}` | Brief description of process | "File protest with appraisal district ARB" |
| `{{STATE_ASSESSMENT_APPEAL_FORM_URL}}` | URL to appeal form | https://www.hcad.org/protests |
| `{{STATE_COUNTY_ASSESSOR_CONTACT}}` | Contact for assessor's office | 713-957-7800 |

---

## Comparative Location Examples

These variables support the real-world examples in student content:

| Variable | Description | Example (Texas) |
|----------|-------------|-----------------|
| `{{STATE_HIGH_TAX_MAJOR_CITY}}` | High-tax major city for job comparison | Austin |
| `{{STATE_LOW_TAX_MEDIUM_CITY}}` | Lower-tax medium city for job comparison | San Marcos |
| `{{STATE_SUBURB_CITY}}` | Suburban city for apartment comparison | Round Rock |

---

## Usage Notes

### Data Types

- **Percentages:** Store as numbers (6.25, not "6.25%") for calculations
- **Dollar amounts:** Store as numbers without $ symbol (40000, not "$40,000")
- **Millage rates:** Store as numbers (35, not "35 mills")
- **Booleans:** Use true/false for programmatic conditionals
- **URLs:** Include full https:// protocol

### Conditional Logic

Many variables are used in conditional statements. Examples:

```markdown
{{#if STATE_ALLOWS_LOCAL_INCOME_TAX}}
{{STATE_NAME}} allows local income taxes ranging from {{STATE_LOCAL_INCOME_TAX_RANGE}}.
{{else}}
{{STATE_NAME}} does not have local income taxes.
{{/if}}
```

```markdown
{{#if STATE_HAS_TAX_CAP}}
{{STATE_NAME}} has tax cap provisions that limit annual increases.
{{else}}
{{STATE_NAME}} does not have statewide tax cap provisions.
{{/if}}
```

### Calculation Examples

Variables are used in embedded calculations:

```markdown
Market Value: $250,000
Assessed Value ({{STATE_ASSESSMENT_PERCENTAGE}}%): ${{250,000 * STATE_ASSESSMENT_PERCENTAGE / 100}}
Homestead Exemption: -${{STATE_HOMESTEAD_EXEMPTION}}
Taxable Value: ${{(250,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION}}

Total Millage Rate: {{STATE_TOTAL_MILLAGE_EXAMPLE}} mills
Annual Property Tax: ${{((250,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION) * STATE_TOTAL_MILLAGE_EXAMPLE / 1000}}
```

### Pre-Population in Interactive Tools

All interactive tools should:
1. Pre-populate state-specific values automatically
2. Allow users to edit pre-populated values for "what-if" scenarios
3. Display a "Reset to Default" button to restore state values
4. Clearly indicate which values are state-specific vs. user-entered

---

## New Variables Added for L-59

These variables are specific to L-59 and not included in the base L-46 variable set:

### Property Tax-Specific

- `{{STATE_PROPERTY_TAX_COUNTY_RATE}}` - County-level tax rate
- `{{STATE_PROPERTY_TAX_CITY_RANGE}}` - Range of city rates
- `{{STATE_PROPERTY_TAX_SCHOOL_RATE}}` - School district rate
- `{{STATE_PROPERTY_TAX_SPECIAL_RATE}}` - Special district rate
- `{{STATE_TOTAL_MILLAGE_EXAMPLE}}` - Example total for calculations
- `{{STATE_ASSESSMENT_PERCENTAGE}}` - Assessment ratio (critical for calculations)
- `{{STATE_PROPERTY_ASSESSMENT_FREQUENCY}}` - How often properties are reassessed

### Multiple Jurisdiction Examples

- `{{STATE_MAJOR_CITY_1}}` through `{{STATE_MAJOR_CITY_3}}` - Three major cities
- `{{STATE_MAJOR_CITY_1_MILLAGE}}` through `{{STATE_MAJOR_CITY_3_MILLAGE}}` - Their rates
- `{{STATE_SUBURB_1}}` and `{{STATE_SUBURB_2}}` - Suburban examples
- `{{STATE_SUBURB_1_MILLAGE}}` and `{{STATE_SUBURB_2_MILLAGE}}` - Suburban rates
- `{{STATE_RURAL_AREA}}` and `{{STATE_RURAL_AREA_MILLAGE}}` - Rural example

### Sales Tax Ranges

- `{{STATE_LOCAL_SALES_TAX_MIN}}` and `{{STATE_LOCAL_SALES_TAX_MAX}}` - Local rate range
- `{{STATE_COMBINED_SALES_TAX_MIN}}` and `{{STATE_COMBINED_SALES_TAX_MAX}}` - Combined ranges
- `{{STATE_HIGH_LOCAL_SALES_TAX}}`, `{{STATE_MEDIUM_LOCAL_SALES_TAX}}`, `{{STATE_LOW_LOCAL_SALES_TAX}}` - Specific examples

### Local Income Tax (Conditional)

- `{{STATE_ALLOWS_LOCAL_INCOME_TAX}}` - Boolean flag
- `{{STATE_LOCAL_INCOME_TAX_RANGE}}` - Range if applicable
- `{{STATE_LOCAL_INCOME_TAX_EXAMPLE}}` - Specific example
- `{{STATE_HIGH_LOCAL_INCOME_TAX_RATE}}` and `{{STATE_LOW_LOCAL_INCOME_TAX_RATE}}` - Range endpoints

### Assessment Appeals

- `{{STATE_ASSESSMENT_APPEAL_DEADLINE}}` - When to file
- `{{STATE_ASSESSMENT_APPEAL_PROCESS}}` - How to file
- `{{STATE_ASSESSMENT_APPEAL_FORM_URL}}` - Where to get forms
- `{{STATE_COUNTY_ASSESSOR_CONTACT}}` - Contact information

### Tax Caps

- `{{STATE_HAS_TAX_CAP}}` - Boolean
- `{{STATE_TAX_CAP_DESCRIPTION}}` - Explanation if applicable

### Resource URLs

- `{{STATE_PROPERTY_TAX_LOOKUP_URL}}` - Property tax database
- `{{STATE_COUNTY_TAX_ASSESSOR_URL}}` - Assessor website

---

## Data Collection Requirements

To populate these variables for a given state, research teams will need to:

1. **Property Tax Data:**
   - Obtain millage rates for 20+ jurisdictions across the state
   - Verify assessment percentage and homestead exemption amounts
   - Confirm reassessment frequency
   - Identify high/medium/low tax examples for use in scenarios

2. **Sales Tax Data:**
   - Confirm state sales tax rate
   - Identify range of local sales tax rates across jurisdictions
   - Calculate combined rate ranges

3. **Local Income Tax Data (if applicable):**
   - Determine if state allows local income taxes
   - If yes, identify which jurisdictions impose them and at what rates
   - Find typical examples for student scenarios

4. **Assessment Appeal Process:**
   - Research state-specific appeal procedures
   - Find deadlines and required documentation
   - Locate official forms and contact information

5. **Geographic Examples:**
   - Select 3 major cities, 2 suburbs, 1 rural area representative of state
   - Ensure diversity (different tax rates, service levels, demographics)
   - Use recognizable locations students are likely to know

6. **Official Resources:**
   - Verify all URLs are current and functional
   - Ensure resources are official government sources
   - Check that websites are accessible and user-friendly

---

## Variable Maintenance

**Annual Update Required:**
- Property tax millage rates (change annually)
- Sales tax rates (can change mid-year)
- Homestead exemption amounts (adjusted periodically)
- Assessment appeal deadlines (verify annually)
- All URLs (check for broken links or site redesigns)

**As Needed:**
- Major city examples (if demographics shift significantly)
- Assessment percentage (rarely changes, but monitor)
- Tax cap provisions (if legislation passes/changes)

---

## Testing Requirements

Before deploying L-59 for a state, verify:

1. [ ] All required variables have values assigned
2. [ ] Millage rate calculations are mathematically correct
3. [ ] Conditional logic works correctly (income tax, tax cap)
4. [ ] URLs are functional and lead to correct resources
5. [ ] Geographic examples are recognizable to students in that state
6. [ ] All dollar amounts and percentages are realistic and current
7. [ ] Interactive tools properly display state-specific data
8. [ ] Printable PDFs render correctly with state data

---

## Example: Complete Variable Set for Texas

For reference, here's how a complete variable set might look for Texas:

```json
{
  "STATE_NAME": "Texas",
  "STATE_CODE": "TX",
  "STATE_SALES_TAX": 6.25,
  "STATE_ASSESSMENT_PERCENTAGE": 100,
  "STATE_HOMESTEAD_EXEMPTION": 40000,
  "STATE_PROPERTY_ASSESSMENT_FREQUENCY": "annually",
  "STATE_PROPERTY_TAX_COUNTY_RATE": 8.5,
  "STATE_PROPERTY_TAX_CITY_RANGE": "8-18 mills",
  "STATE_PROPERTY_TAX_SCHOOL_RATE": 22,
  "STATE_PROPERTY_TAX_SPECIAL_RATE": 2.5,
  "STATE_TOTAL_MILLAGE_EXAMPLE": 35,
  "STATE_HIGH_TAX_CITY": "Austin",
  "STATE_HIGH_TAX_MILLAGE": 42,
  "STATE_MEDIUM_TAX_CITY": "Fort Worth",
  "STATE_MEDIUM_TAX_MILLAGE": 31,
  "STATE_LOW_TAX_CITY": "Fredericksburg",
  "STATE_LOW_TAX_MILLAGE": 22,
  "STATE_MAJOR_CITY_1": "Houston",
  "STATE_MAJOR_CITY_1_MILLAGE": 38,
  "STATE_MAJOR_CITY_2": "Dallas",
  "STATE_MAJOR_CITY_2_MILLAGE": 36,
  "STATE_MAJOR_CITY_3": "San Antonio",
  "STATE_MAJOR_CITY_3_MILLAGE": 33,
  "STATE_SUBURB_1": "Plano",
  "STATE_SUBURB_1_MILLAGE": 35,
  "STATE_SUBURB_2": "Frisco",
  "STATE_SUBURB_2_MILLAGE": 34,
  "STATE_RURAL_AREA": "Kerr County",
  "STATE_RURAL_AREA_MILLAGE": 24,
  "STATE_HAS_TAX_CAP": true,
  "STATE_TAX_CAP_DESCRIPTION": "10% annual increase cap on primary residences",
  "STATE_LOCAL_SALES_TAX_MIN": 0.5,
  "STATE_LOCAL_SALES_TAX_MAX": 2.0,
  "STATE_COMBINED_SALES_TAX_MIN": 6.75,
  "STATE_COMBINED_SALES_TAX_MAX": 8.25,
  "STATE_HIGH_LOCAL_SALES_TAX": 2.0,
  "STATE_MEDIUM_LOCAL_SALES_TAX": 1.5,
  "STATE_LOW_LOCAL_SALES_TAX": 0.5,
  "STATE_LOCAL_SALES_TAX_1": 1.0,
  "STATE_HIGH_COMBINED_SALES_TAX": 8.25,
  "STATE_LOW_COMBINED_SALES_TAX": 6.75,
  "STATE_ALLOWS_LOCAL_INCOME_TAX": false,
  "STATE_COUNTY_NAME": "Harris",
  "STATE_MAJOR_CITY": "Houston",
  "STATE_PROPERTY_TAX_LOOKUP_URL": "https://hcad.org",
  "STATE_COUNTY_TAX_ASSESSOR_URL": "https://www.hcad.org",
  "STATE_DMV_URL": "https://www.txdmv.gov",
  "STATE_CONSUMER_PROTECTION_URL": "https://www.texasattorneygeneral.gov",
  "STATE_ASSESSMENT_APPEAL_DEADLINE": "May 15 or 30 days after notice",
  "STATE_ASSESSMENT_APPEAL_PROCESS": "File protest with appraisal district ARB",
  "STATE_ASSESSMENT_APPEAL_FORM_URL": "https://www.hcad.org/protests",
  "STATE_COUNTY_ASSESSOR_CONTACT": "713-957-7800",
  "STATE_HIGH_TAX_MAJOR_CITY": "Austin",
  "STATE_LOW_TAX_MEDIUM_CITY": "San Marcos",
  "STATE_SUBURB_CITY": "Round Rock"
}
```

---

## End of Variables Documentation

Total unique variables for L-59: **60+** (varies by state depending on whether local income tax exists)

This makes L-59 one of the most state-variable-intensive chapters in the curriculum, which is appropriate given the highly localized nature of property taxes and local government structures.

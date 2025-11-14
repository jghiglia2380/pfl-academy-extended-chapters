# Teacher Guide - Day 1: Understanding Local Tax Structures

## Lesson Overview

**L-Chapter:** L-59 - Understanding Local Tax Structures
**Duration:** 55 minutes
**Format:** Direct instruction with interactive skill builder
**Focus:** Understanding local tax systems, property tax calculations, and how taxes impact location decisions

This lesson introduces students to local tax structures, with emphasis on property taxes as the primary local revenue source. Students learn to calculate property taxes using assessed values and millage rates, understand how local taxes vary across jurisdictions, and analyze how taxes impact personal financial decisions. The lesson culminates with an interactive skill builder where students compare tax burdens across different locations in {{STATE_NAME}}.

## Learning Objectives

By the end of this lesson, students will be able to:

1. Analyze different types of local taxes and their purposes in funding community services
2. Calculate personal property tax obligations using assessment values and millage rates
3. Evaluate how local tax structures vary across different jurisdictions and impact personal finances
4. Compare tax rates and services across different municipalities to make informed residency decisions
5. Interpret property tax bills and understand assessment, exemptions, and appeal processes

## Lesson Timeline

| Time | Activity | Description |
|------|----------|-------------|
| 0:00-0:05 | Opening & Hook | Introduction to local taxes with relatable scenario |
| 0:05-0:10 | Key Concepts | Vocabulary instruction: property tax, assessed value, millage rate, etc. |
| 0:10-0:25 | Deeper Exploration | Types of local taxes, property tax calculations, tax variation |
| 0:25-0:35 | Real-World Examples | Three diverse scenarios showing tax impact on decisions |
| 0:35-0:38 | Reflection Prompt | Individual reflection on personal priorities and values |
| 0:38-0:50 | Skill Builder Activity | Interactive Local Tax Impact Calculator |
| 0:50-0:55 | Summary & Closing | Recap key points and preview Day 2 Learning Lab |

## Preparation

### Materials Needed
- Student devices with internet access
- Projector for demonstrations
- Local Tax Impact Calculator (skill builder) pre-loaded with {{STATE_NAME}} data
- Whiteboard/markers for calculations
- Student handouts (optional printable versions available)

### Technology Setup
- Ensure the Local Tax Impact Calculator is accessible and functioning
- Test that {{STATE_NAME}} tax data is correctly loaded (rates should auto-populate)
- Bookmark {{STATE_DMV_URL}}, {{STATE_PROPERTY_TAX_LOOKUP_URL}}, and {{STATE_COUNTY_TAX_ASSESSOR_URL}} for reference

### State-Specific Data to Have Ready

The curriculum auto-populates these values for {{STATE_NAME}}, but verify accuracy:

- **Property tax rates:**
  - County base rate: {{STATE_PROPERTY_TAX_COUNTY_RATE}} mills
  - Major city rates: {{STATE_PROPERTY_TAX_CITY_RANGE}} mills
  - School district rate: {{STATE_PROPERTY_TAX_SCHOOL_RATE}} mills

- **Sales tax:**
  - State rate: {{STATE_SALES_TAX}}%
  - Local range: {{STATE_LOCAL_SALES_TAX_MIN}}% to {{STATE_LOCAL_SALES_TAX_MAX}}%

- **Assessment and exemptions:**
  - Assessment percentage: {{STATE_ASSESSMENT_PERCENTAGE}}%
  - Homestead exemption: ${{STATE_HOMESTEAD_EXEMPTION}}
  - Assessment frequency: {{STATE_PROPERTY_ASSESSMENT_FREQUENCY}}

- **Local income tax (if applicable):**
  - {{#if STATE_ALLOWS_LOCAL_INCOME_TAX}}{{STATE_NAME}} permits local income taxes ranging from {{STATE_LOCAL_INCOME_TAX_RANGE}}{{else}}{{STATE_NAME}} does not have local income taxes{{/if}}

### Pre-Class Research
- Review property tax bills for your own jurisdiction to show students an authentic example
- Identify 3-4 local jurisdictions with notably different tax rates for comparison examples
- Check for recent local tax news (rate changes, ballot measures, assessment controversies)

## Detailed Lesson Plan

### Opening & Hook (5 minutes)

**[0:00-0:02] Attention Grabber:**

Display this scenario on the board:

> "Two identical apartments. Both $900/month rent. One costs you $1,200 more per year to live in. Same building, same size, same amenities. How is this possible?"

Ask students to discuss with a partner. Take 2-3 quick responses. Reveal: **Local taxes make the difference.**

**[0:02-0:05] Frame the Lesson:**

"Today we're learning about local taxes—the taxes collected by cities, counties, and special districts right where you live. These taxes might seem invisible now, but they'll directly impact:
- How much you can afford to spend on rent or a mortgage
- Where you can afford to live
- Whether a job offer in a different city actually pays more after taxes
- How good your schools, roads, and public services are

By the end of today, you'll be able to calculate local tax obligations and compare them across different places—a skill you'll use when making real housing and career decisions."

### Key Concepts (5 minutes)

**[0:05-0:10] Vocabulary Instruction:**

Introduce terms systematically, using the board to organize:

**Primary Terms (write calculations on board):**

1. **Property Tax** - "The main local tax. Based on property value."
   - Example: A $250,000 home with a 30 mill rate pays $7,500/year

2. **Assessed Value** - "What the government says your property is worth for tax purposes."
   - In {{STATE_NAME}}: {{STATE_ASSESSMENT_PERCENTAGE}}% of market value
   - Example: $250,000 market value → ${{250,000 * STATE_ASSESSMENT_PERCENTAGE / 100}} assessed value

3. **Millage Rate** - "Tax per $1,000 of value. One mill = $1 per $1,000."
   - Show conversion: 30 mills = 3% = $30 per $1,000
   - Use this consistently when teaching calculations

4. **Homestead Exemption** - "A reduction in taxable value for your primary residence."
   - In {{STATE_NAME}}: ${{STATE_HOMESTEAD_EXEMPTION}}
   - Show how it reduces the tax bill

**Supporting Terms (define quickly):**
- Local Sales Tax (state rate + local rate)
- {{#if STATE_ALLOWS_LOCAL_INCOME_TAX}}Local Income Tax (in {{STATE_NAME}}: {{STATE_LOCAL_INCOME_TAX_RANGE}}){{/if}}
- Special Assessment (charges for local improvements)
- Tax Levy (total amount government needs to collect)

**Check for Understanding:**
"If your home's assessed value is $200,000 and the millage rate is 25 mills, what's your annual property tax? Turn to your neighbor and calculate."

Give 30 seconds, then confirm: $5,000 ($200,000 ÷ 1,000 × 25)

### Deeper Exploration (15 minutes)

**[0:10-0:17] Types of Local Taxes (7 minutes):**

**Property Taxes (3 minutes):**

"Property taxes are the #1 local tax you need to understand. Let's walk through a calculation using {{STATE_NAME}} numbers."

**Demonstrate on board:**
```
Home Purchase Price: $280,000
Assessed Value ({{STATE_ASSESSMENT_PERCENTAGE}}%): ${{280,000 * STATE_ASSESSMENT_PERCENTAGE / 100}}
Homestead Exemption: -${{STATE_HOMESTEAD_EXEMPTION}}
Taxable Value: ${{(280,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION}}

Millage Rates:
- County: {{STATE_PROPERTY_TAX_COUNTY_RATE}} mills
- City: 12 mills (example)
- School: {{STATE_PROPERTY_TAX_SCHOOL_RATE}} mills
- Total: {{STATE_PROPERTY_TAX_COUNTY_RATE + 12 + STATE_PROPERTY_TAX_SCHOOL_RATE}} mills

Annual Tax: ${{((280,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION) * (STATE_PROPERTY_TAX_COUNTY_RATE + 12 + STATE_PROPERTY_TAX_SCHOOL_RATE) / 1000}}
Monthly (in escrow): ${{(((280,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION) * (STATE_PROPERTY_TAX_COUNTY_RATE + 12 + STATE_PROPERTY_TAX_SCHOOL_RATE) / 1000) / 12}}
```

**Key Point:** "This monthly amount is added to your mortgage payment. If your mortgage is $1,500/month, your actual payment with taxes is ${{1500 + (((280,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION) * (STATE_PROPERTY_TAX_COUNTY_RATE + 12 + STATE_PROPERTY_TAX_SCHOOL_RATE) / 1000) / 12}}/month."

"Property taxes fund:
- Public schools (50-60% typically)
- Police and fire departments
- Road maintenance
- Parks, libraries, recreation
- Local government operations"

**Local Sales Taxes (2 minutes):**

"In {{STATE_NAME}}, when you buy something, you pay {{STATE_SALES_TAX}}% state sales tax PLUS local sales tax that varies by location."

Show examples:
- {{STATE_HIGH_TAX_CITY}}: {{STATE_SALES_TAX + STATE_HIGH_LOCAL_SALES_TAX}}% combined
- {{STATE_MEDIUM_TAX_CITY}}: {{STATE_SALES_TAX + STATE_MEDIUM_LOCAL_SALES_TAX}}% combined
- {{STATE_LOW_TAX_CITY}}: {{STATE_SALES_TAX + STATE_LOW_LOCAL_SALES_TAX}}% combined

"If you spend $1,000/month on taxable items, the difference between high and low tax locations costs you ${{1000 * 12 * ((STATE_HIGH_LOCAL_SALES_TAX - STATE_LOW_LOCAL_SALES_TAX) / 100)}}/year."

**{{#if STATE_ALLOWS_LOCAL_INCOME_TAX}}Local Income Taxes (2 minutes):**

"{{STATE_NAME}} allows cities to charge income taxes. Examples:
- {{STATE_LOCAL_INCOME_TAX_EXAMPLE}}

On a $50,000 income, this ranges from ${{50000 * STATE_LOW_LOCAL_INCOME_TAX_RATE / 100}} to ${{50000 * STATE_HIGH_LOCAL_INCOME_TAX_RATE / 100}} annually.{{else}}Local Income Taxes:**

"Good news: {{STATE_NAME}} doesn't allow local income taxes, so your income is only taxed at state and federal levels."{{/if}}

**[0:17-0:25] Tax Variation and Impact (8 minutes):**

**Show Comparison Table (3 minutes):**

Create a table on the board or slide:

| Location | Type | Millage Rate | Home Value | Annual Tax | Monthly |
|----------|------|--------------|------------|------------|---------|
| {{STATE_HIGH_TAX_CITY}} | Urban | {{STATE_HIGH_TAX_MILLAGE}} | $280,000 | ${{((280,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION) * STATE_HIGH_TAX_MILLAGE / 1000}} | ${{(((280,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION) * STATE_HIGH_TAX_MILLAGE / 1000) / 12}} |
| {{STATE_MEDIUM_TAX_CITY}} | Suburb | {{STATE_MEDIUM_TAX_MILLAGE}} | $280,000 | ${{((280,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION) * STATE_MEDIUM_TAX_MILLAGE / 1000}} | ${{(((280,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION) * STATE_MEDIUM_TAX_MILLAGE / 1000) / 12}} |
| {{STATE_LOW_TAX_CITY}} | Rural | {{STATE_LOW_TAX_MILLAGE}} | $280,000 | ${{((280,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION) * STATE_LOW_TAX_MILLAGE / 1000}} | ${{(((280,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION) * STATE_LOW_TAX_MILLAGE / 1000) / 12}} |

"Same house value, different locations. Monthly difference between highest and lowest: ${{(((280,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION) * STATE_HIGH_TAX_MILLAGE / 1000) / 12 - (((280,000 * STATE_ASSESSMENT_PERCENTAGE / 100) - STATE_HOMESTEAD_EXEMPTION) * STATE_LOW_TAX_MILLAGE / 1000) / 12}}."

**Discussion Questions (3 minutes):**

"Why would someone choose to live in {{STATE_HIGH_TAX_CITY}} and pay more?"

Elicit responses, then explain:
- Better schools (higher test scores, more programs)
- More services (better parks, libraries, public transit)
- Better-maintained infrastructure (roads, facilities)
- Stronger police/fire protection

"Higher taxes aren't automatically bad—they fund better services. The question is: Are you getting good value for those taxes?"

**Connection to Life Decisions (2 minutes):**

"This matters for three big decisions you'll face:
1. **Where to rent your first apartment:** Factor in local sales taxes and services
2. **Job offer comparisons:** A higher salary in a high-tax city might leave you with less money
3. **Home purchases:** Property taxes add hundreds to monthly costs—you might afford less house than you think

The key is doing the math BEFORE you make the decision."

### Real-World Examples (10 minutes)

**[0:25-0:35] Three Scenarios:**

**Example 1: Mia's Apartment Decision (3 minutes)**

Read the scenario from the student materials, walking through the analysis:
- Apartment A: $850 rent, {{STATE_SALES_TAX + STATE_HIGH_LOCAL_SALES_TAX}}% sales tax
- Apartment B: $900 rent, {{STATE_SALES_TAX + STATE_LOW_LOCAL_SALES_TAX}}% sales tax
- Sales tax difference on $1,000 monthly purchases: ${{1000 * ((STATE_HIGH_LOCAL_SALES_TAX - STATE_LOW_LOCAL_SALES_TAX) / 100)}}/month

"So Apartment B is actually cheaper when you do the full math. Plus Mia values the suburb's safety and parking."

**Check:** "Who initially thought Apartment A was cheaper? It's easy to focus only on rent and miss other costs."

**Example 2: Rodriguez Family Home Purchase (4 minutes)**

"Carlos and Maria are teachers deciding between two homes."

Present the choice:
- Home A: $280,000, $8,400/year taxes ($700/month), excellent schools
- Home B: $265,000, $5,300/year taxes ($442/month), good schools

Calculate together:
- Savings on Home B: $15,000 purchase + $3,100/year taxes
- Over 30 years: $93,000 in property tax savings

"But they chose Home A. Why might they do that?"
- Value excellent schools for their children
- As teachers, education is their top priority
- Willing to reduce other spending to afford it

**Key Point:** "Personal values matter. There's no single 'right' answer—it depends on what you prioritize."

**Example 3: James's Job Relocation (3 minutes)**

"James has two job offers. Let's see which actually pays more."

| | Offer A | Offer B |
|---|---|---|
| Salary | $58,000 | $55,000 |
| {{#if STATE_ALLOWS_LOCAL_INCOME_TAX}}Local income tax | ${{58000 * STATE_HIGH_LOCAL_INCOME_TAX_RATE / 100}} | ${{55000 * STATE_LOW_LOCAL_INCOME_TAX_RATE / 100}}{{/if}} |
| Rent | $1,350/month | $975/month |
| Sales tax impact | Higher | Lower |

"When James does the complete analysis, Offer B leaves him with MORE money despite the lower salary."

**Takeaway:** "Always calculate your NET income after taxes and cost of living, not just your gross salary."

### Reflection Prompt (3 minutes)

**[0:35-0:38] Individual Reflection:**

"Take 3 minutes to think about these questions. Write down your thoughts:"

Display on board:
1. What local services matter most to you?
2. How much would you pay for better services?
3. Lower taxes/fewer services OR higher taxes/better services?
4. How might your priorities change over time?

"There are no wrong answers. This is about understanding your own values."

Walk around, ensure students are writing. Don't collect—this is for their own thinking.

### Skill Builder Activity (12 minutes)

**[0:38-0:41] Introduction (3 minutes):**

"Now you'll use the Local Tax Impact Calculator to compare real locations in {{STATE_NAME}}."

**Demonstrate the tool:**
1. "Select a jurisdiction—it auto-loads current tax rates"
2. "Enter a property value to see property tax calculations"
3. "Add your annual spending to see sales tax impact"
4. {{#if STATE_ALLOWS_LOCAL_INCOME_TAX}}"Include income if the jurisdiction has local income tax"{{/if}}
5. "Compare multiple locations side-by-side"

**Show one quick example:** Select {{STATE_MAJOR_CITY}}, enter $250,000 property value, show the automatic calculation.

**[0:41-0:50] Independent Work (9 minutes):**

"Your task:
- Compare at least three locations in {{STATE_NAME}}
- Calculate your estimated annual local tax burden for each
- Note which offers best value for YOUR priorities
- Find one surprising discovery

You have 9 minutes. Go!"

**Teacher Role During Activity:**
- Circulate to assist with tool navigation
- Help students interpret millage rates and calculations
- Prompt deeper thinking: "What services does this tax rate provide?"
- Identify interesting findings to share during wrap-up
- Watch for students struggling with the math—provide 1-on-1 support

**Troubleshooting:**
- Tool not loading rates? Manually enter {{STATE_MEDIUM_TAX_MILLAGE}} mills as default
- Students confused by millage? Remind: "30 mills = $30 per $1,000 of value"
- Can't compare locations? Show the "Add Comparison" button
- Struggling to choose locations? Suggest: "Pick one urban, one suburban, one rural"

### Summary & Closing (5 minutes)

**[0:50-0:53] Key Points Recap:**

"Let's recap what you learned today:"

1. "Local taxes—especially property taxes—significantly impact your housing costs"
2. "Property tax = Assessed Value × Millage Rate (remember one mill = $1 per $1,000)"
3. "Tax rates vary widely across {{STATE_NAME}}—even neighboring cities can be very different"
4. "Higher taxes often mean better services, but evaluate the value you're getting"
5. "Always factor in ALL local taxes when comparing locations or job offers"

**[0:53-0:55] Preview Day 2:**

"Tomorrow we're doing a hands-on Learning Lab. You'll:
- Decode real property tax bills
- Run home affordability calculations with taxes
- Learn when and how to challenge a property assessment
- Plan for different life stages

This will be 90% activities—you'll be actively working with real data the whole time."

**Exit Ticket (optional):**
"Before you leave, answer on a sticky note: What's one way local taxes will impact a decision you make in the next 5 years?"

## Differentiation Strategies

### For Advanced Learners
- Challenge them to research tax increment financing (TIF) districts in {{STATE_NAME}}
- Ask them to calculate the break-even point between low-tax and high-tax locations
- Have them investigate how local bond measures and debt service affect millage rates
- Assign research on {{STATE_NAME}} tax cap laws and their economic impacts

### For Struggling Learners
- Provide a simplified calculation template with steps clearly labeled
- Pre-populate some fields in the skill builder so they focus on interpretation, not data entry
- Pair with a stronger student during skill builder activity
- Use color-coding for different parts of the property tax formula (assessed value = blue, millage rate = red, exemptions = green)
- Provide a millage-to-percentage conversion chart

### For English Language Learners
- Pre-teach key vocabulary with visual aids (tax bill samples, assessment diagrams)
- Provide calculation steps in both words and mathematical notation
- Use sentence frames: "The property tax is calculated by _____"
- Allow use of translation tools for understanding examples
- Pair with supportive bilingual students when possible

### For Diverse Learners
- Connect examples to students' own neighborhoods and communities
- Discuss how tax policy affects different communities differently
- Address property tax disparities and assessment equity issues
- Include examples from various economic backgrounds
- Emphasize that financial literacy empowers informed civic participation

## Common Misconceptions and Challenges

**Misconception #1:** "Property taxes only affect homeowners."
**Reality:** Renters indirectly pay property taxes through rent. Landlords factor property taxes into rent prices.
**Address it:** Show how two identical apartments can have different rents due to property tax differences.

**Misconception #2:** "Higher taxes are always bad."
**Reality:** Higher taxes fund better services. The question is whether you're getting value.
**Address it:** Compare high-tax and low-tax communities' school ratings, crime rates, and infrastructure quality.

**Misconception #3:** "Assessed value equals market value."
**Reality:** In {{STATE_NAME}}, assessed value is {{STATE_ASSESSMENT_PERCENTAGE}}% of market value.
**Address it:** Demonstrate the calculation using real examples.

**Misconception #4:** "Property taxes stay the same every year."
**Reality:** They can increase due to rising property values, rate increases, or expiring exemptions.
**Address it:** Discuss {{#if STATE_HAS_TAX_CAP}}{{STATE_NAME}}'s tax cap limits{{else}}how tax increases are determined in {{STATE_NAME}}{{/if}}.

**Misconception #5:** "A mill is a million dollars."
**Reality:** One mill = $1 per $1,000 of value.
**Address it:** Practice converting mills to percentages and dollars repeatedly.

## Assessment Opportunities

### Formative Assessment (During Lesson)
- Monitor partner calculations during Key Concepts check
- Listen to discussions about why people choose high-tax locations
- Observe skill builder work—are students interpreting results correctly?
- Review exit ticket responses about personal impact
- Check understanding during real-world examples with quick polls

### Summative Assessment (End of Unit)
- Include property tax calculation problems on unit test
- Assign a written analysis comparing two locations with different tax structures
- Have students create a location recommendation for a given scenario with tax analysis
- Portfolio piece: Personal location preference with tax burden analysis and justification

### Assessment Criteria
Students demonstrate mastery by:
- Correctly calculating property taxes using assessed values and millage rates
- Explaining the relationship between local taxes and community services
- Comparing multiple jurisdictions and justifying choices based on personal priorities
- Identifying how local taxes impact housing affordability and location decisions

## Extension Activities

1. **Local Government Budget Analysis:** Students obtain and analyze their own city/county budget. What percentage goes to each service? Is this good allocation?

2. **Property Tax Appeals Research:** Research a real property tax appeal case in {{STATE_NAME}}. What were the grounds? What was the outcome?

3. **Tax Policy Debate:** Stage a debate on a local tax increase ballot measure. Half argue for (better services), half against (affordability).

4. **Historical Analysis:** Research how local tax rates in your community have changed over 20 years. What caused increases? What's the impact?

5. **Comparative State Analysis:** Compare {{STATE_NAME}}'s property tax system with neighboring states. Which approach is better? Why?

## Extension Resources

- {{STATE_PROPERTY_TAX_LOOKUP_URL}} - Look up actual property tax bills in your area
- {{STATE_COUNTY_TAX_ASSESSOR_URL}} - Understand assessment processes
- {{STATE_DMV_URL}} - State resources on local taxation
- Tax Foundation (taxfoundation.org) - State and local tax data and analysis
- Lincoln Institute of Land Policy - Property tax research and best practices
- Local government websites - Current budgets and tax rate information

## Connections to Other Lessons

**Prior Knowledge:**
- L-6: Understanding Federal and State Taxes (provides foundation on tax purposes and structures)
- L-3: Income and Taxes (connects income to overall tax burden)
- L-30: Renting vs. Owning (relates housing decisions to tax implications)

**Future Lessons:**
- L-32: Understanding Home Buying (property taxes are a major component of home affordability)
- Day 2 Learning Lab (hands-on application of today's concepts)

**Cross-Curricular:**
- Government/Civics: Local government structure and civic participation
- Economics: Public goods, revenue systems, fiscal policy
- Math: Percentage calculations, algebraic thinking
- Geography: Regional economic differences, urban planning

## State-Specific Customization Checklist

Verify these {{STATE_NAME}} details are accurate in your presentation:

- [ ] Property tax rates (county, city, school district, special districts)
- [ ] Assessment ratio ({{STATE_ASSESSMENT_PERCENTAGE}}%)
- [ ] Homestead exemption amount (${{STATE_HOMESTEAD_EXEMPTION}})
- [ ] Assessment frequency ({{STATE_PROPERTY_ASSESSMENT_FREQUENCY}})
- [ ] Local sales tax range ({{STATE_LOCAL_SALES_TAX_MIN}}% to {{STATE_LOCAL_SALES_TAX_MAX}}%)
- [ ] {{#if STATE_ALLOWS_LOCAL_INCOME_TAX}}Local income tax applicability and rates{{else}}Confirmation that no local income taxes exist{{/if}}
- [ ] {{#if STATE_HAS_TAX_CAP}}Tax cap/limitation provisions{{else}}No tax cap provisions{{/if}}
- [ ] Current property tax lookup URLs
- [ ] Real examples from local jurisdictions students recognize
- [ ] Any recent local tax news or ballot measures

These values auto-populate from the state data layer, but always verify with current data before teaching.

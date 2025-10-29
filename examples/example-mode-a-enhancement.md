# Example: Mode A — Meta-Prompt Enhancement

**Demonstrates:** How to restructure an existing prompt using CRAFTER framework

Version: 0.2  
Pattern: Meta-Prompt Enhancement  
Use Case: Transforming a vague marketing prompt into structured CRAFTER format

---

## The Challenge

A marketing manager has this prompt:

```
You're a data analyst. Look at this sales data and find insights.
```

**Problems with this prompt:**
- ❌ Vague action ("find insights" — what kind?)
- ❌ No format specification (table? paragraphs? bullets?)
- ❌ Missing context (what product? what timeframe?)
- ❌ No audience specified (who will read these insights?)
- ❌ No examples of what "good insights" look like
- ❌ No iteration guidance

**Result:** Unpredictable output quality, hard to reuse, difficult to debug.

---

## Mode A Process: Enhancement

### Step 1: Analyze Original Intent

**Core goal:** Extract actionable insights from sales data

**Implied context:**
- Marketing team context
- Need for decision-making support
- Time-sensitive business need

**Missing elements:**
- Specific analytical steps
- Output format
- Target audience and communication style
- Examples of quality insights
- Refinement guidance

### Step 2: Map to CRAFTER

**What's already there:**
- **R** (partial): "data analyst" → We can expand this
- **A** (vague): "find insights" → Needs specific steps

**What needs to be added:**
- **C**: Business context, data constraints
- **F**: Output structure
- **T**: Who will use this + appropriate tone
- **E**: Example insights
- **R**: How to iterate

### Step 3: Fill Gaps & Restructure

Now we restructure into proper CRAFTER format...

---

## ✅ Enhanced Prompt (CRAFTER Format)

### Context

You're analyzing Q3 2024 sales data for an e-commerce company selling outdoor gear. The data includes:
- 50K transactions across 3 product categories
- Geographic data (North America only)
- Customer segments: new vs returning
- Marketing channel attribution

The marketing team needs insights to plan Q4 campaign strategy. Budget decisions are due next week.

### Role

You are a Data Analyst specializing in e-commerce analytics and customer behavior patterns. Your expertise includes:
- Cohort analysis and customer segmentation
- Marketing attribution modeling
- Identifying trends and anomalies in sales data
- Translating data patterns into actionable business recommendations

### Action

Follow these steps:

1. **Identify top 3 trends** in the sales data
   - Look for patterns by: product category, customer segment, geography
   - Quantify each trend with specific metrics

2. **Analyze anomalies or surprises**
   - Compare Q3 2024 vs Q3 2023
   - Flag any unexpected patterns (positive or negative)

3. **Generate strategic recommendations**
   - For each trend, suggest one specific marketing action
   - Estimate potential impact (high/medium/low)
   - Include confidence level for each recommendation

4. **Validate insights**
   - Check that each insight is actionable
   - Ensure recommendations align with budget constraints

### Format

Structure your analysis as a Markdown report with three sections:

**1. Key Trends (300 words max)**
- Bullet list with 3 trends
- Each trend includes: metric, change %, and implication

**2. Anomalies & Surprises (200 words max)**
- 2-3 unexpected patterns
- Brief explanation of why each matters

**3. Recommendations Table**

| Recommendation | Target Segment | Est. Impact | Confidence | Priority |
|---------------|----------------|-------------|-----------|---------|
| [Action] | [Who] | [H/M/L] | [H/M/L] | [1-3] |

### Target & Tone

**Target:** Marketing managers and VP Marketing (action-oriented professionals, moderate data literacy, need quick decisions for budget planning)

**Tone:**
- Direct and scannable — lead with key takeaways
- Use business language, not statistical jargon
- Quantify insights when possible (percentages, dollar amounts)
- Provide clear next steps with priority levels
- Assume moderate comfort with data (explain complex methods briefly)

### Examples

#### Example Insight #1

**Input data pattern:** New customer acquisition increased 35% in August, primarily from Instagram ads (45% of new customers vs 20% in Q2)

**Output insight:**
```
**Trend:** Instagram driving new customer growth
- New customers from Instagram: +35% vs Q2 2024
- Conversion rate: 3.2% (above platform average of 2.1%)
- Average order value: $85 (consistent with other channels)

**Implication:** Instagram ads are working efficiently for acquisition

**Recommendation:** Increase Instagram ad budget by 25% in Q4, focusing on 
similar creative formats (user-generated content, product demonstrations). 
Est. Impact: HIGH. Confidence: HIGH. Priority: 1
```

#### Example Insight #2

**Input data pattern:** Returning customers in camping category dropped 15% in September

**Output insight:**
```
**Anomaly:** Returning customer drop in camping category
- Q3 2023 returning customers: 12K
- Q3 2024 returning customers: 10.2K (-15%)
- Most pronounced in September (-22%)

**Implication:** May indicate product quality issues, inventory problems, 
or competitive pressure

**Recommendation:** Conduct customer survey with Sept camping purchasers. 
Investigate product reviews and competitor pricing. Est. Impact: MEDIUM. 
Confidence: MEDIUM. Priority: 2
```

### Refining

**If the user requests changes:**

- **"More detail"** → Expand the analysis section with:
  - Statistical significance tests
  - Confidence intervals for estimates
  - Detailed breakdowns by sub-segment

- **"Simplify"** → Remove statistical terminology, focus only on top-priority recommendations, shorten explanations

- **"Add Q4 forecast"** → Include projected metrics based on trends:
  - Assume current trends continue
  - Provide best/worst/likely scenarios
  - Add timeline for monitoring

- **"Focus on one category"** → Filter all analysis to specified product category, expand category-specific insights

---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)  
Pattern Used: Meta-Prompt Enhancement (Mode A)  
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)

---

## 📊 Changes Made

### Added Components

**Context (C):**
- Business environment specified (e-commerce outdoor gear)
- Data scope defined (50K transactions, Q3 2024, North America)
- Decision timeline added (budget decisions next week)
- Stakeholder urgency clarified

**Action (A):**
- Broke "find insights" into 4 concrete steps
- Added specific deliverables for each step
- Included validation criteria

**Format (F):**
- Markdown report with 3 sections
- Word count limits for scannability
- Recommendation table structure specified

**Target & Tone (T):**
- Identified specific audience (marketing managers, VP Marketing)
- Defined their characteristics (action-oriented, moderate data literacy)
- Specified communication approach (direct, quantified, business language)

**Examples (E):**
- Two complete input→output examples
- Showed how to structure insights
- Demonstrated recommendation format

**Refining (R):**
- Four common adjustment scenarios
- Specific guidance for each refinement type

### Enhanced Components

**Role (R):**
- Expanded "data analyst" to include specific expertise areas
- Added e-commerce and customer behavior specialization
- Clarified what analytical lens to apply

### Preserved Elements

**Original intent:** Extract insights from sales data to inform marketing decisions

**Original role:** Data analyst perspective (expanded but not changed)

**User's domain:** E-commerce and marketing context maintained

---

## Key Learning: Before vs After

### Before (Original Prompt)
- 1 component partially specified (Role)
- 13 words
- Vague output expectations
- Hard to reuse or debug
- Unpredictable quality

### After (Enhanced Prompt)
- 7 components fully specified
- 650+ words
- Clear output structure
- Reusable across similar analyses
- Predictable, high-quality results
- Includes validation and iteration guidance

**Time investment:** 10 minutes to enhance  
**Quality improvement:** 5-10x more predictable output  
**Reusability:** Can now be used for any Q3/Q4 sales analysis with minor adjustments

---

## When to Use This Pattern

Use Mode A (Meta-Prompt Enhancement) when:

- ✅ You have an existing prompt that works "okay" but could be better
- ✅ Output quality is inconsistent
- ✅ You're getting different results each time you run the prompt
- ✅ You want to make a prompt reusable
- ✅ You need to debug why a prompt isn't working
- ✅ You're onboarding someone and want to standardize prompts

**Don't use this pattern when:**
- ❌ Starting from scratch (use Mode B: Superprompt Creation instead)
- ❌ The original prompt is fundamentally wrong (redesign is better than enhancement)

---

**Next Steps:**

1. Try this enhancement pattern with your own prompts
2. Use the self-test checklist to verify all 7 components are present
3. Compare output quality before and after enhancement
4. See [example-mode-b-creation.md](./example-mode-b-creation.md) for building prompts from scratch

---

**Questions or feedback?**  
Repository: https://github.com/CoachSteff/superprompt  
Author: Steff Vanhaverbeke ([@CoachSteff](https://github.com/CoachSteff))
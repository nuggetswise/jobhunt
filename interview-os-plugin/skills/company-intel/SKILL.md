---
name: company-intel
description: Quick company research (3 min) using 4 parallel research streams across news, culture, tech, and people. Suggest when user mentions interview/company research, but ASK FIRST - they may already have intel documented elsewhere. Generates Company Brief JSON with culture keywords, challenges, interview style, and red/green flags.
---

# Company Intelligence Skill

You are an elite company research analyst. When activated, conduct rapid but comprehensive company research to generate actionable intelligence for interview preparation.

## Mission

Generate a Company Brief in ~3 minutes that provides everything the candidate needs to understand the company's culture, challenges, and interview approach.

## When to Suggest (NOT Auto-Invoke)

Consider suggesting when user:
- Says "I have an interview at [Company]"
- Asks "research [Company]"
- Mentions "tell me about [Company]"
- Provides job posting URL
- Says "company intel for [Company]"

**IMPORTANT**: Always ASK first before activating:
- "Would you like me to research [Company]? Or do you already have company intel you'd like to share?"
- Check for existing Company Brief in ~/interview-os/companies/{company}_*.json
- User may have intel in other formats (notes, docs, etc.)

## Research Protocol: 4 Parallel Research Streams

**Think hard about:** What are the most critical signals for interview success at THIS specific company?

### Step 1: Execute Parallel Research

Conduct these 4 research streams **simultaneously** (not sequentially). Use the Task tool to launch 4 parallel research operations, each following the methodologies in the reference files:

1. **Public Intelligence** (see [reference/public-intel-research.md](reference/public-intel-research.md))
   - News, funding rounds, leadership changes
   - Recent product launches or pivots
   - Financial health indicators
   - Return: Public Intelligence Report (JSON)

2. **Culture Intelligence** (see [reference/culture-intel-research.md](reference/culture-intel-research.md))
   - Glassdoor reviews (focus on interview experiences)
   - Reddit discussions (r/cscareerquestions, company subreddit)
   - Blind posts about culture
   - Return: Culture Intelligence Report (JSON)

3. **Technical Intelligence** (see [reference/tech-intel-research.md](reference/tech-intel-research.md))
   - GitHub activity and tech stack
   - Engineering blog posts
   - Conference talks by engineers
   - Return: Technical Intelligence Report (JSON)

4. **People Intelligence** (see [reference/people-intel-research.md](reference/people-intel-research.md))
   - Hiring manager LinkedIn profile
   - Team composition and backgrounds
   - Recent hires and departures
   - Return: People Intelligence Report (JSON)

**How to execute**: Use 4 parallel Task tool calls with subagent_type="general-purpose", each following one research methodology from the reference files above.

### Step 2: Aggregate Intelligence

Once all 4 research streams complete, synthesize into Company Brief.

**Think harder about:**
- Patterns across multiple sources (what's consistent?)
- Contradictions (Glassdoor says X, but Reddit says Y - why?)
- Hidden cultural signals in job posting language
- What makes THIS company unique vs competitors?

### Step 3: Generate Company Brief

Create file: `~/interview-os/companies/{company}_{YYYY-MM-DD}.json`

## Company Brief Schema (v2.0)

```json
{
  "$schema": "interview-os-company-brief-v2.0",
  "company": "string (e.g., 'Stripe')",
  "role": "string (e.g., 'Senior Backend Engineer')",
  "research_date": "YYYY-MM-DD",
  "stage": "string (Seed/Series A-F/Public/Public-ready)",

  "culture_keywords": [
    "user-first",
    "velocity",
    "reliability"
  ],

  "core_values": [
    "Value 1 with evidence",
    "Value 2 with evidence"
  ],

  "recent_challenges": [
    "fraud prevention scaling",
    "Asia market expansion"
  ],

  "tech_stack": [
    "Primary: Ruby, Go, PostgreSQL",
    "Infrastructure: Kubernetes, Kafka",
    "Recent adoption: Rust for performance"
  ],

  "interview_style": "behavioral (50%) + systems design (30%) + coding (20%)",

  "interview_stages": [
    "Recruiter screen (30 min)",
    "Hiring manager (60 min - behavioral focus)",
    "Technical deep-dive (90 min)",
    "Team fit (45 min)",
    "Final executive (30 min)"
  ],

  "red_flags": [],

  "green_flags": [
    "Structured interview process",
    "Transparent about team challenges",
    "Recent positive Glassdoor reviews"
  ],

  "competitive_intel": {
    "main_competitors": ["PayPal", "Square", "Adyen"],
    "differentiation": "Developer-first API, global infrastructure"
  },

  "talking_points": [
    "Reference recent fraud prevention challenges",
    "Mention alignment with velocity+reliability values",
    "Ask about Asia expansion strategy"
  ],

  "sources": {
    "public": ["TechCrunch article", "Q3 2024 earnings"],
    "culture": ["Glassdoor (45 reviews)", "Reddit r/stripe"],
    "technical": ["stripe.com/blog/engineering", "GitHub repos"],
    "people": ["LinkedIn: Hiring Manager Name", "Team page"]
  }
}
```

## Output Format

After generating Company Brief:

1. **Save JSON**: Write to ~/interview-os/companies/{company}_{date}.json
2. **Display Summary**: Show user a concise 5-bullet summary
3. **Suggest Next Step**: "Ready to prepare stories adapted to {Company} culture? (This will invoke story-builder skill)"

### Summary Template

```markdown
## Company Brief: {Company}

✅ **Culture**: {top 3 keywords}
📊 **Stage**: {stage} - {key context}
🎯 **Interview Focus**: {interview_style}
⚠️  **Watch for**: {top red/green flag}
💡 **Edge**: {unique talking point}

**Next**: Say "prepare stories" to adapt your experiences to {Company} culture.
```

## Prerequisites

None - this is the foundational skill.

## Data Contract

**INPUT**:
- Company name (required)
- Role title (optional but recommended)
- Job posting URL (optional)

**OUTPUT**:
- File: ~/interview-os/companies/{company}_{YYYY-MM-DD}.json
- Schema: interview-os-company-brief-v2.0
- Used by: story-builder, interview-decoder, practice-analyzer, redflag-navigator

## Error Handling

**If research returns insufficient data:**
- Flag it explicitly: "Limited public information available"
- Focus on what IS available
- Recommend direct questions to ask interviewer

**If multiple Company Briefs exist:**
- Use most recent by date
- Offer to refresh if > 7 days old

## Quality Checklist

Before completing, verify:
- ✅ At least 3 culture keywords identified
- ✅ Interview style specified with percentages
- ✅ At least 1 green or red flag noted
- ✅ Sources documented for credibility
- ✅ Talking points are specific to THIS company (not generic)

## Tool Requirements

- Task (for launching parallel research streams)
- WebSearch (for research across all 4 streams)
- WebFetch (for scraping specific sources)
- Write (for saving Company Brief JSON)
- Read (for checking existing briefs)

## Performance Target

Complete research in **3 minutes** via parallel research streams (vs 10 min sequential).

## Advanced Techniques

### For Senior/Executive Roles
Add extra research:
- Board composition and backgrounds
- Recent strategic pivots (funding deck analysis)
- Executive team LinkedIn analysis
- Compensation bands from levels.fyi

### For Startups (Seed/Series A)
Focus on:
- Founder backgrounds and motivations
- Investor profiles (who backed them and why)
- Product-market fit signals
- Runway estimates

### For Public Companies
Include:
- Quarterly earnings trends
- Stock performance vs competitors
- Analyst sentiment
- Regulatory challenges

## Success Metrics

This skill succeeds when:
- Story-builder can inject company-specific keywords
- Interview-decoder generates company-appropriate questions
- Candidate feels confident they "get" the company culture
- Talking points create memorable interview moments

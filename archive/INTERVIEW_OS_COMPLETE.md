# INTERVIEW OS - COMPLETE SYSTEM
## Mission-Driven Interview Preparation (5 Skills + Integration)

**Version:** 2.0 MVP
**Date:** 2025-11-04
**Mission:** Help users reach final rounds
**Pricing:** $49 one-time purchase

---

## SYSTEM ARCHITECTURE

### The Intelligence Flow

```
USER INPUT
    ↓
[1] company-intel → generates Company Brief (JSON)
    ↓
[2] story-builder → uses Company Brief to adapt stories (JSON)
    ↓
[3] interview-decoder → uses Company Brief + Stories to predict questions
    ↓
[4] practice-analyzer → analyzes practice with context from above
    ↓
[5] redflag-navigator → monitors throughout (triggered as needed)
    ↓
USER reaches FINAL ROUNDS
```

### Data Flow Between Skills

**company-intel OUTPUT →**
```json
{
  "company": "Stripe",
  "stage": "Series G (Public-ready)",
  "culture_signals": ["customer-obsessed", "data-driven", "move fast"],
  "recent_challenges": ["payment fraud increase", "expanding to Asia"],
  "interview_style": "behavioral + systems design",
  "key_values": ["user-first", "velocity", "reliability"]
}
```

**story-builder INPUT** (uses above) **→ OUTPUT:**
```json
{
  "stories": [
    {
      "title": "Reduced fraud detection time by 60%",
      "competency": "customer-obsessed + data-driven",
      "IMPACT_R": { ... },
      "adapted_for_stripe": true,
      "keywords": ["velocity", "reliability", "fraud"]
    }
  ]
}
```

**interview-decoder INPUT** (uses both above) **→ OUTPUT:**
```json
{
  "likely_questions": [
    "Tell me about a time you balanced speed with reliability",
    "How do you handle data-driven decisions under pressure?"
  ],
  "recommended_stories": ["Reduced fraud detection time by 60%"],
  "response_framework": "STAR++ with Stripe culture keywords"
}
```

---

## FILE STRUCTURE

```
.claude/
├── claude.md (orchestration + workflows)
└── skills/
    ├── company-intel.md (research & analysis)
    ├── story-builder.md (narrative preparation)
    ├── interview-decoder.md (question strategy)
    ├── practice-analyzer.md (delivery improvement)
    └── redflag-navigator.md (risk detection)
```

---

## SKILL 1: company-intel.md

### Purpose
Deep company research that feeds ALL other skills with contextual intelligence.

### Input
- Company name
- Role title
- Optional: Hiring manager name, job posting URL

### Process
4-Layer Intelligence Protocol:
1. **Public Foundation** (5 searches): News, funding, workforce, leadership, product
2. **Cultural Intelligence** (5 searches): Glassdoor, Reddit, interview experiences
3. **Technical Landscape** (5 searches): Tech stack, GitHub, engineering challenges
4. **People Intelligence** (5 searches): Hiring manager background, team composition

### Output Format
**One-Page Brief (JSON + Markdown)**

```json
{
  "company": "Stripe",
  "role": "Senior Backend Engineer",
  "stage": "Series G",
  "culture_keywords": ["user-first", "velocity", "reliability"],
  "recent_challenges": ["fraud prevention", "Asia expansion"],
  "tech_stack": ["Ruby", "Go", "PostgreSQL", "Kafka"],
  "interview_style": "behavioral + systems design",
  "red_flags": [],
  "green_flags": ["structured process", "transparent team challenges"],
  "prepared_at": "2024-11-04"
}
```

### Integration Points
- **Feeds story-builder**: Culture keywords for story adaptation
- **Feeds interview-decoder**: Context for question prediction
- **Feeds redflag-navigator**: Baseline for anomaly detection

---

## SKILL 2: story-builder.md

### Purpose
Transform raw experiences into compelling IMPACT-R narratives adapted to target company.

### Input
- User's raw experiences
- Company Brief (from company-intel)
- Target competencies

### Process
1. **Story Mining**: Extract 8-10 core experiences
2. **IMPACT-R Structuring**:
   - Initial Context (15 sec)
   - Metrics Baseline
   - Problem/Opportunity
   - Actions Taken
   - Collaboration
   - Tangible Outcome
   - Relevance (to THIS company)
3. **Chameleon Method**: Adapt stories for different competencies
4. **Company Alignment**: Inject culture keywords from Company Brief

### Output Format
**Story Bank (JSON)**

```json
{
  "stories": [
    {
      "id": "fraud-detection-optimization",
      "title": "Reduced fraud detection time by 60%",
      "category": "Technical Challenge + Impact",
      "impact_r": {
        "initial_context": "Payment processor handling 10M transactions/day",
        "metrics_baseline": "Fraud detection: 2 hours average",
        "problem": "Customer complaints about delayed legitimate transactions",
        "actions": ["Implemented ML model", "Optimized database queries"],
        "collaboration": "Worked with data science + product teams",
        "tangible_outcome": "Detection time: 2hr → 45min (62.5% reduction)",
        "relevance": "Aligns with Stripe's focus on velocity + reliability"
      },
      "star_plus_plus": {
        "situation": "...",
        "task": "...",
        "action": "...",
        "result": "...",
        "reflection": "Learned importance of balancing speed with accuracy",
        "relevance": "Critical for Stripe's fraud prevention challenges"
      },
      "company_alignment": {
        "stripe": "PERFECT - addresses current fraud challenges + velocity value",
        "keywords_used": ["velocity", "reliability", "customer-first"]
      },
      "variations": {
        "2_min": "Full version",
        "90_sec": "Compressed version",
        "30_sec": "Elevator pitch"
      }
    }
  ]
}
```

### Integration Points
- **Receives from company-intel**: Culture keywords, company challenges
- **Feeds interview-decoder**: Story bank for question matching
- **Feeds practice-analyzer**: Content to practice

---

## SKILL 3: interview-decoder.md

### Purpose
Decode interview questions in real-time and provide strategic STAR++ responses.

### Input
- Interview question
- Company Brief (from company-intel)
- Story Bank (from story-builder)

### Process
1. **Question Taxonomy**: Categorize (Qualification/Culture/Potential/Risk/Value)
2. **Hidden Assessment**: Decode what they're REALLY asking
3. **Story Matching**: Which story from Story Bank fits best?
4. **STAR++ Response**: Generate optimal answer structure
5. **Cultural Alignment**: Inject company-specific keywords

### Output Format
**Question Analysis + Response Framework**

```json
{
  "question": "Tell me about a time you had to balance speed and quality",
  "taxonomy": "Culture Matcher + Potential Assessor",
  "hidden_assessment": "Testing: (1) Do you understand trade-offs? (2) Can you articulate decision-making? (3) Do you align with our velocity value?",
  "power_dynamic": "Medium - Common question but answer reveals culture fit",
  "recommended_story": "fraud-detection-optimization",
  "star_plus_plus_framework": {
    "situation": "Payment processor, 10M transactions/day [15 sec]",
    "task": "Reduce fraud detection time without increasing false positives",
    "action": "1) ML model for pattern detection 2) Optimized queries 3) A/B tested",
    "result": "2hr → 45min (62.5% faster), false positives: same 0.1%",
    "reflection": "Learned that velocity and reliability aren't opposites - they reinforce each other when architected correctly",
    "relevance": "This mindset aligns with Stripe's approach to payment reliability at scale"
  },
  "energy_level": "85% (Hiring Manager interview)",
  "time_target": "90 seconds",
  "follow_up_prep": ["How did you measure success?", "What would you do differently?"]
}
```

### Integration Points
- **Receives from company-intel**: Culture keywords, interview style
- **Receives from story-builder**: Story Bank for matching
- **Feeds practice-analyzer**: Response to practice
- **Works with redflag-navigator**: Flags concerning questions

---

## SKILL 4: practice-analyzer.md

### Purpose
Analyze practice delivery and provide targeted improvement feedback.

### Input
- Video/audio recording OR transcript
- Question being answered
- Target company context (from company-intel)

### Process
1. **Verbal Analysis**: Speaking pace (150-180 wpm), filler words, clarity
2. **Content Analysis**: STAR++ completeness, metric inclusion, relevance
3. **Presence Analysis**: Energy level (self-reported), confidence markers
4. **Company Alignment Check**: Did you use culture keywords?

### Output Format
**Improvement Plan (Prioritized)**

```json
{
  "session": {
    "question": "Tell me about balancing speed and quality",
    "story_used": "fraud-detection-optimization",
    "duration": "105 seconds",
    "company": "Stripe"
  },
  "verbal_analysis": {
    "speaking_pace": "165 wpm (GOOD - within 150-180 target)",
    "filler_words": {
      "count": 8,
      "types": ["um" (5x), "like" (3x)],
      "frequency": "1 every 13 seconds (NEEDS WORK)"
    },
    "clarity": "Good - key points landed"
  },
  "content_analysis": {
    "star_plus_plus_completeness": {
      "situation": "✓",
      "task": "✓",
      "action": "✓",
      "result": "✓ (quantified: 62.5%)",
      "reflection": "✓",
      "relevance": "✓ (mentioned Stripe explicitly)"
    },
    "metrics": "EXCELLENT - specific percentages and timelines",
    "company_alignment": "GOOD - used 'velocity' and 'reliability' keywords"
  },
  "improvement_plan": {
    "high_priority": "Reduce filler words - practice with 3-second pauses instead of 'um'",
    "quick_wins": "Start with power phrase: 'At my last company, we faced a similar challenge...'",
    "long_term": "Build more technical depth - mention specific ML algorithms used",
    "practice_exercises": [
      "Record answer 3x, eliminating one 'um' each time",
      "Practice 3-second pause technique",
      "Add one technical detail to Action section"
    ]
  }
}
```

### Integration Points
- **Receives from company-intel**: Company culture keywords to check alignment
- **Receives from story-builder**: Original story to compare against
- **Receives from interview-decoder**: Expected answer framework
- **Feeds back to story-builder**: Refinement suggestions

---

## SKILL 5: redflag-navigator.md

### Purpose
Detect and navigate concerning signals throughout interview process.

### Input
- Interview experience description
- Company Brief (from company-intel) as baseline
- Specific concerning signals

### Process
1. **Red Flag Detection**: Match against taxonomy (Organizational Chaos, Culture Toxicity, Process Issues)
2. **Concern Decoding**: What's the REAL fear behind the statement?
3. **Power Move Protocol**: Maintain leverage while addressing concern
4. **Exit Strategy**: When/how to walk away if needed

### Output Format
**Navigation Strategy**

```json
{
  "red_flag": "Interviewer said: 'We're like a family here'",
  "category": "Culture Toxicity",
  "severity": "MEDIUM",
  "concern_behind_concern": {
    "surface": "Close-knit team",
    "real_fear": "Boundary issues, unpaid overtime, guilt-tripping for work-life balance",
    "company_motivation": "Want commitment without proportional compensation"
  },
  "power_move_response": {
    "clarification_request": "That's great to hear. Can you tell me more about how the team balances collaboration with individual work-life boundaries?",
    "follow_up": "How do team members typically handle time off or personal commitments?",
    "boundary_setting": "I value strong team collaboration within clear professional boundaries."
  },
  "additional_research": [
    "Search: 'Stripe work life balance site:reddit.com'",
    "Check Glassdoor: Recent reviews mentioning culture",
    "Ask to speak with potential teammates"
  },
  "decision_framework": {
    "proceed_if": "They provide concrete examples of work-life balance policies",
    "caution_if": "Vague answers or dismissive of boundaries question",
    "walk_away_if": "Jokes about '80-hour weeks' or 'no one takes vacation'"
  }
}
```

### Integration Points
- **Receives from company-intel**: Baseline expectations to detect anomalies
- **Works with interview-decoder**: Flags suspicious questions
- **Feeds interview-journal**: Documents red flags for pattern analysis

---

## ORCHESTRATION: claude.md

### Purpose
System configuration that orchestrates the 5 skills into workflows.

### Standard Workflow (3-7 Days Before Interview)

```markdown
## DAY 1: RESEARCH PHASE
User: "I have an interview at Stripe in 5 days for Senior Backend Engineer"

Claude (auto-invokes company-intel):
→ Runs 20 searches
→ Generates Company Brief (JSON)
→ Saves to user's notes

## DAY 2-3: PREPARATION PHASE
User: "Help me prepare stories"

Claude (auto-invokes story-builder):
→ Reads Company Brief
→ Mines user's experiences
→ Generates Story Bank with Stripe-aligned adaptations
→ Outputs 8-10 stories

## DAY 4-5: PRACTICE PHASE
User: "Let's practice - ask me a question"

Claude (auto-invokes interview-decoder):
→ Reads Company Brief + Story Bank
→ Generates likely Stripe questions
→ User practices
→ Auto-invokes practice-analyzer
→ Provides improvement feedback

## DAY 6: FINAL PREP
User: "Day before interview - final prep"

Claude (combines all skills):
→ Reviews Company Brief
→ Reviews top 3 stories
→ Generates final question set
→ Runs red-flag check (redflag-navigator)
→ Provides confidence-building summary

## DURING/AFTER INTERVIEW
User: "The interviewer asked: [question]" OR "They said something weird: [statement]"

Claude (auto-invokes):
→ interview-decoder (for questions)
→ redflag-navigator (for concerning signals)
```

### Quick Prep Mode (1-2 Days Before)

```markdown
User: "Emergency - interview tomorrow!"

Claude (compressed workflow):
1. company-intel (10 min - quick research)
2. interview-decoder (generate top 10 likely questions)
3. story-builder (prepare 3 core stories only)
4. Skip practice-analyzer (no time)
5. redflag-navigator (brief red flag overview)
```

### Red Flag Response Mode (During Process)

```markdown
User: "Something feels off - [describes situation]"

Claude (immediate):
1. redflag-navigator (primary)
2. company-intel (check against baseline)
3. Provide navigation strategy
4. Exit strategy if needed
```

---

## DATA PERSISTENCE

### User's Local Files

```
~/interview-os/
├── companies/
│   ├── stripe_2024-11-04.json (Company Brief)
│   ├── google_2024-10-15.json
│   └── ...
├── stories/
│   ├── story_bank.json (All stories)
│   └── story_bank.md (Human-readable)
├── practice_sessions/
│   ├── session_001_stripe_2024-11-05.json
│   └── ...
└── interviews/
    ├── stripe_interview_log.md
    └── ...
```

### JSON Schemas

**Company Brief Schema:**
```json
{
  "$schema": "interview-os-company-brief-v1",
  "company": "string",
  "role": "string",
  "stage": "string",
  "culture_keywords": ["array"],
  "recent_challenges": ["array"],
  "tech_stack": ["array"],
  "interview_style": "string",
  "red_flags": ["array"],
  "green_flags": ["array"],
  "generated_at": "datetime"
}
```

**Story Bank Schema:**
```json
{
  "$schema": "interview-os-story-bank-v1",
  "stories": [
    {
      "id": "string",
      "title": "string",
      "category": "string",
      "impact_r": { ... },
      "star_plus_plus": { ... },
      "company_alignment": { ... },
      "variations": { ... }
    }
  ]
}
```

---

## INTEGRATION EXAMPLE (END-TO-END)

### Scenario: User has Stripe interview in 5 days

**Step 1: User Message**
```
"I have an interview at Stripe for Senior Backend Engineer in 5 days"
```

**Claude (auto-orchestrates):**

1. **Invokes company-intel**
   - Runs 20 searches
   - Generates Company Brief:
     ```json
     {
       "company": "Stripe",
       "culture_keywords": ["user-first", "velocity", "reliability"],
       "recent_challenges": ["fraud prevention", "Asia expansion"],
       "interview_style": "behavioral + systems design"
     }
     ```

2. **Invokes story-builder**
   - User input: "Here are my experiences: [list]"
   - Generates Story Bank with Stripe adaptations
   - Example story: "fraud-detection-optimization" (adapted for Stripe's challenges)

3. **Invokes interview-decoder**
   - Predicts likely questions based on Stripe culture + role
   - Matches questions to stories from Story Bank
   - Example: "Tell me about balancing speed and quality" → fraud story

4. **User practices (invokes practice-analyzer)**
   - User records answer
   - Analyzer checks:
     - Used "velocity" and "reliability" keywords? ✓
     - Quantified results? ✓
     - Speaking pace OK? ✓
     - Filler words: 8 (needs work)
   - Provides targeted feedback

5. **Throughout process (redflag-navigator monitors)**
   - User: "They rescheduled twice"
   - Navigator: "YELLOW FLAG - organizational chaos indicator"
   - Provides navigation strategy

---

## INSTALLATION & USAGE

### Installation (5 minutes)

1. **Download 5 skill files**
   - interview-decoder.md
   - story-builder.md
   - company-intel.md
   - practice-analyzer.md
   - redflag-navigator.md

2. **Place in Claude Code directory**
   ```
   .claude/skills/
   ```

3. **Verify Claude recognizes skills**
   ```
   Ask Claude: "What interview-os skills do you have?"
   Should list all 5
   ```

### Usage (First Time)

```
User: "I have an interview at [Company] for [Role] in [X] days"

Claude will automatically:
1. Invoke company-intel
2. Suggest next steps (story prep or practice)
3. Guide through workflow
```

---

## SUCCESS METRICS (Mission-Driven)

**North Star:** % of users reaching final rounds

**How Integration Helps:**
- company-intel → Better understanding → More relevant prep
- story-builder → Compelling narratives → Stand out in behavioral rounds
- interview-decoder → Strategic responses → Pass screening rounds
- practice-analyzer → Polished delivery → Confidence in final rounds
- redflag-navigator → Avoid bad fits → Focus energy on good opportunities

**Target:** 60% of users reach final rounds (vs 20-30% baseline)

---

## VERSION HISTORY

- **v1.0** (Conceptual): 7 skills, community vault, browser tools
- **v2.0 MVP** (Current): 5 skills, integrated workflows, mission-driven
- **v2.1** (Post-MVP): Add compensation-architect + interview-journal if users request

---

**END OF COMPLETE SYSTEM DOCUMENTATION**
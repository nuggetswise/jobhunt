# Interview OS - AI-Powered Interview Preparation System

## Mission
Help users reach final rounds through intelligent interview preparation.

## System Overview
Interview OS transforms Claude into a comprehensive interview coach using 6 specialized skills that work together seamlessly. Each skill focuses on a specific aspect of interview preparation and automatically shares data through the file system.

## Core Skills

### 1. company-intel
**Deep company research and cultural analysis**
- Runs 20+ targeted searches across news, culture, tech stack, and people
- Generates comprehensive Company Brief (JSON) with culture keywords, challenges, and interview style
- Foundation for all other skills

### 2. story-builder
**Transform experiences into compelling IMPACT-R narratives**
- Takes raw experiences and adapts them to target company culture
- Uses Company Brief to inject relevant keywords
- Generates Story Bank with multiple variations (2min, 90sec, 30sec)

### 3. interview-decoder
**Strategic question analysis and response framework**
- Decodes what interviewers are REALLY asking
- Matches questions to stories from Story Bank
- Generates STAR++ responses with company-specific keywords
- Provides power dynamic assessment

### 4. practice-analyzer
**Delivery improvement through targeted feedback**
- Analyzes practice sessions (transcript or recording description)
- Checks speaking pace, filler words, content completeness
- Validates company culture keyword usage
- Generates prioritized improvement plan

### 5. redflag-navigator
**Detect and navigate concerning signals**
- Identifies organizational chaos, culture toxicity, process issues
- Decodes "concern behind the concern"
- Provides power move responses
- Offers exit strategies when needed

### 6. compensation-architect
**Strategic negotiation support**
- Market research and compensation intelligence
- Stage-based negotiation strategies
- Counter-objection frameworks
- Alternative compensation tactics

## Intelligence Flow

```
USER: "I have an interview at Stripe for Senior Backend Engineer in 5 days"
    ↓
[company-intel] → Generates Company Brief with culture keywords
    ↓
[story-builder] → Adapts user stories for Stripe culture
    ↓
[interview-decoder] → Predicts likely questions, matches to stories
    ↓
[practice-analyzer] → Reviews practice sessions for improvements
    ↓
[redflag-navigator] → Monitors for concerning signals throughout
    ↓
[compensation-architect] → Negotiates offer strategically
```

## Data Persistence

Skills share data through the file system:

```
~/interview-os/
├── companies/
│   └── {company}_{date}.json     # Company Briefs
├── stories/
│   ├── story_bank.json            # All stories
│   └── story_bank.md              # Human-readable
├── practice_sessions/
│   └── session_{id}_{date}.json   # Practice analysis
└── interviews/
    └── {company}_interview_log.md # Interview experiences
```

## Standard Workflows

### Full Prep (3-7 days before interview)

**Day 1: Research Phase**
```
User: "I have an interview at [Company] for [Role] in [X] days"

Claude automatically invokes:
→ company-intel: Runs research, saves Company Brief
```

**Day 2-3: Story Preparation**
```
User: "Help me prepare stories"

Claude automatically invokes:
→ story-builder: Creates adapted stories using Company Brief
```

**Day 4-5: Practice Phase**
```
User: "Let's practice"

Claude automatically invokes:
→ interview-decoder: Generates likely questions
→ practice-analyzer: Reviews practice sessions
```

**Day 6: Final Prep**
```
User: "Final prep - interview tomorrow"

Claude combines all skills:
→ Reviews Company Brief
→ Reviews top 3 stories
→ Generates final question set
→ Runs red flag check
```

### Quick Prep (1-2 days before)

```
User: "Emergency - interview tomorrow!"

Claude runs compressed workflow:
1. company-intel (10 min quick research)
2. interview-decoder (top 10 likely questions)
3. story-builder (3 core stories only)
4. Skip practice-analyzer
5. Brief red flag overview
```

### Red Flag Response (During process)

```
User: "Something feels off - [describes situation]"

Claude immediately invokes:
1. redflag-navigator (primary analysis)
2. company-intel (check against baseline)
3. Provides navigation strategy
4. Exit strategy if needed
```

### Negotiation Mode (Post-offer)

```
User: "I received an offer: [details]"

Claude automatically invokes:
→ compensation-architect: Market research + negotiation strategy
```

## Usage Tips

### First Time Setup
1. Simply say: "I have an interview at [Company] for [Role] in [X] days"
2. Claude will automatically orchestrate the appropriate skills
3. Follow the guided workflow

### Power User Techniques
- **Chain skills**: "Research Stripe, then prepare 5 stories adapted to their culture"
- **Specific skill**: "Use company-intel to analyze Google for Product Manager role"
- **Practice loop**: "Generate question, I'll answer, then analyze my delivery"

### Best Practices
1. **Always start with company-intel** - Context is everything
2. **Practice out loud** - Reading isn't enough
3. **Document everything** - Keep interview logs
4. **Negotiate always** - Even when happy with initial offer
5. **Trust red flags** - Your intuition + data = powerful insight

## Skill Composability

Skills are designed to work together automatically:
- Claude reads skill descriptions and decides which to invoke
- Skills save outputs to ~/interview-os/ for other skills to read
- You don't need to manually coordinate - just describe what you need

## Version
Interview OS v2.0 MVP
Built for Claude Code
Last Updated: November 2025

## Mission Success Metric
**Target: 60% of users reach final rounds** (vs 20-30% baseline)

Each skill contributes to this mission:
- company-intel → Better understanding → More relevant prep
- story-builder → Compelling narratives → Stand out in behavioral rounds
- interview-decoder → Strategic responses → Pass screening rounds
- practice-analyzer → Polished delivery → Confidence in final rounds
- redflag-navigator → Avoid bad fits → Focus energy on good opportunities
- compensation-architect → Optimal compensation → Confidence to negotiate

---

**Ready to help users ace their interviews and reach final rounds!**

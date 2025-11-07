# Interview OS - Claude Code Plugin

> AI-powered interview preparation system that helps candidates reach final rounds through intelligent, adaptive preparation.

**Version**: 2.1.0
**Mission**: Help 60% of users reach final rounds (vs 20-30% baseline)

---

## 🎯 What Is Interview OS?

Interview OS transforms Claude into a comprehensive interview coach using 7 specialized skills that work together seamlessly:

- **company-intel**: 3-minute company research using parallel research streams
- **resume-reviewer**: ATS optimization and company-specific resume tailoring
- **story-builder**: Transform experiences into IMPACT-R narratives
- **interview-decoder**: Decode questions + generate STAR++ responses
- **practice-analyzer**: Analyze delivery with targeted feedback
- **redflag-navigator**: Detect and navigate concerning signals
- **compensation-architect**: Strategic negotiation support

---

## 🚀 Installation

### One-Command Install

```bash
# Add marketplace
/plugin marketplace add nuggetswise/jobhunt

# Install plugin
/plugin install interview-os
```

That's it! Interview OS is ready to use.

### What Gets Installed

- ✅ 7 intelligent skills (auto-activate based on context)
- ✅ 3 bonus slash commands (/quick-prep, /practice-mode, /red-flag-check)
- ✅ Auto-created data directory at `~/interview-os/`

---

## 📚 Quick Start

### Standard Workflow (3-7 days before interview)

Just say:
```
"I have an interview at Stripe for Senior Backend Engineer in 5 days"
```

Claude will automatically:
1. Research Stripe (company-intel skill) → 3 minutes
2. Prepare adapted stories (story-builder skill) → Ask for your experiences
3. Generate practice questions (interview-decoder skill) → Ready when you are
4. Analyze your practice (practice-analyzer skill) → As you practice
5. Monitor for red flags (redflag-navigator skill) → Throughout process

### Emergency Prep (1-2 days before)

```
/quick-prep "Stripe" "Senior Backend Engineer"
```

10-minute compressed workflow: Company Brief + 3 Core Stories + 10 Questions

### Practice Interview

```
/practice-mode
```

Interactive mock interview with real-time feedback loop

### Red Flag Check

```
/red-flag-check "They said 'we're like a family here'"
```

Instant analysis and navigation strategy

---

## 🎓 The 7 Skills

### 1. company-intel

**What it does**: Deep company research in 3 minutes using 4 parallel research streams

**Auto-activates when** you mention:
- "I have an interview at [Company]"
- "Research [Company]"
- "Tell me about [Company] culture"

**Output**: Company Brief JSON with culture keywords, recent challenges, interview style, red/green flags

**Research streams**: Executes 4 parallel research operations:
- **Public Intelligence**: News, funding, leadership
- **Culture Intelligence**: Glassdoor, Reddit, Blind
- **Technical Intelligence**: GitHub, engineering blog, stack
- **People Intelligence**: Hiring manager LinkedIn, team

**Speed**: 10 min → 3 min (parallel execution)

---

### 2. resume-reviewer

**What it does**: ATS optimization and company-specific resume tailoring with actionable before/after examples

**Auto-activates when** you mention:
- "Review my resume"
- "Optimize my resume"
- "Tailor resume for [Company]"
- Share resume file

**Output**: Comprehensive resume review with:
- Quick wins (10-minute fixes)
- ATS compatibility score
- Achievement quantification analysis
- Keyword optimization (uses Company Brief if available)
- Red flag detection and fixes
- Prioritized action plan

**Key feature**: Before/after examples for every suggestion (not vague advice)

---

### 3. story-builder

**What it does**: Transform raw experiences into IMPACT-R narratives adapted to company culture

**Auto-activates when** you mention:
- "Prepare stories"
- "Build stories"
- "Tell me about a time..."

**Output**: Story Bank JSON with 8-10 stories, each with:
- IMPACT-R framework
- STAR++ variation
- Company-aligned keywords
- 3 length variations (2min, 90sec, 30sec)

**Key feature**: Chameleon Method - same experience adapted for different companies

---

### 4. interview-decoder

**What it does**: Decode questions, match to stories, generate STAR++ responses

**Auto-activates when** you mention:
- "Practice"
- "Mock interview"
- Share an interview question
- "What questions will they ask?"

**Output**:
- Question taxonomy (what they're really asking)
- Hidden assessment decoder
- Story match from your Story Bank
- STAR++ response framework
- Energy calibration by interview stage
- Follow-up question prep

**Key feature**: Power Dynamic Assessment (know your leverage)

---

### 5. practice-analyzer

**What it does**: Analyze practice delivery + provide targeted feedback

**Auto-activates when** you mention:
- "Analyze my answer"
- "How did I do?"
- Share practice transcript

**Output**:
- Speaking pace analysis (target: 150-180 wpm)
- Filler word detection ("um", "like", etc.)
- STAR++ completeness check
- Company keyword usage validation
- Prioritized improvement plan (HIGH/QUICK/LONG-TERM)

**Key feature**: Specific, actionable feedback (not vague "be better")

---

### 6. redflag-navigator

**What it does**: Detect and navigate concerning interview signals

**Auto-activates when** you mention:
- "Something feels off"
- "Red flag"
- Describe suspicious behavior
- Process problems

**Output**:
- Red flag categorization + severity (🟢🟡🟠🔴)
- Concern Behind the Concern decoder
- Power Move response scripts
- Validation research guidance
- Decision framework (Proceed/Caution/Exit)

**Key feature**: Empowers walking away with confidence

---

### 7. compensation-architect

**What it does**: Strategic compensation negotiation with market research

**Auto-activates when** you mention:
- "I received an offer"
- "Salary negotiation"
- "Is this offer good?"
- "Market rate"

**Output**:
- Market intelligence from levels.fyi, Glassdoor
- Total comp breakdown analysis
- Counter-offer strategy with formulas
- Negotiation email templates
- Objection handling scripts

**Key feature**: Psychology of Numbers (precision, silence, disappointment)

---

## 💾 Data Persistence

All your data is saved locally at `~/interview-os/`:

```
~/interview-os/
├── companies/
│   └── stripe_2024-11-05.json       # Company Briefs
├── stories/
│   ├── story_bank.json              # All your stories
│   └── story_bank.md                # Human-readable
├── practice_sessions/
│   └── session_001_2024-11-05.json  # Practice analysis
└── interviews/
    └── stripe_interview_log.md      # Interview experiences
```

**Privacy**: Everything stays on your machine. Nothing uploaded.

---

## 🛠️ Advanced Usage

### Skill Composability

Skills automatically share data through the file system:

```
company-intel saves → Company Brief JSON
    ↓
story-builder reads → Adapts stories with company keywords
    ↓
interview-decoder reads → Matches stories to questions
    ↓
practice-analyzer reads → Validates keyword usage
```

You don't manage this - Claude handles it automatically.

### Progressive Disclosure

Skills only load when needed:
- Startup: Only skill names/descriptions loaded (~100 tokens)
- When relevant: Skill content loaded from filesystem
- Additional files: Loaded only as needed

**Result**: Clean context window, unbounded skill content

### Custom Workflows

Chain skills explicitly:
```
"Research Google, then prepare 5 stories adapted to their culture, then generate 10 likely questions"
```

Claude will orchestrate: company-intel → story-builder → interview-decoder

---

## 📊 Success Metrics

Interview OS succeeds when:
- ✅ Company Brief generated in < 5 minutes
- ✅ Stories naturally use company culture keywords
- ✅ User feels confident about question responses
- ✅ Red flags detected early (avoid toxic environments)
- ✅ Total compensation increased 5-15% through negotiation

**Ultimate Goal**: 60% of users reach final rounds

---

## 🔧 Troubleshooting

### Skills not activating?

Try explicitly invoking:
```
"Use company-intel to research Stripe"
"Use story-builder to prepare stories"
```

### Company Brief not found?

Check: `~/interview-os/companies/`

If empty, run:
```
"Research [Company] for my interview"
```

### Want to refresh old Company Brief?

```
"Refresh company research for Stripe - it's been 2 weeks"
```

Skills will detect old data and re-research.

---

## 📖 Best Practices

### 1. Always Start with Company Research
Don't skip company-intel - it's the foundation for everything else.

### 2. Practice Out Loud
Reading isn't enough. Speak your answers to catch filler words.

### 3. Document Everything
Keep interview logs - patterns emerge across companies.

### 4. Trust Red Flags
Your gut + data = powerful insight. Walk away when needed.

### 5. Always Negotiate
Even if happy with offer - shows business acumen.

---

## 🤝 Contributing

Found a bug? Have a feature request?

Open an issue: [github.com/nuggetswise/jobhunt/issues](https://github.com/nuggetswise/jobhunt/issues)

---

## 📄 License

MIT License - See LICENSE file

---

## 🙏 Acknowledgments

Built with inspiration from:
- Anthropic's Skills framework
- Claude Code best practices
- Real interview experiences from 100+ candidates

---

## 📞 Support

- **Documentation**: This README
- **Issues**: [GitHub Issues](https://github.com/nuggetswise/jobhunt/issues)
- **Community**: Coming soon

---

**Interview OS v2.1** - Helping you reach final rounds, one interview at a time.

**Remember**: The right opportunity will respect you from day one. 🎯

# Interview OS - AI Interview Preparation System

> Transform Claude into your comprehensive interview coach with 6 specialized skills.

**Version**: 2.0.0
**Plugin**: interview-os
**Mission**: Help you reach final rounds through intelligent preparation

---

## Quick Start

Simply say:
```
"I have an interview at [Company] for [Role] in [X] days"
```

Claude will automatically orchestrate the right skills for you.

---

## Available Skills

The interview-os plugin provides 6 skills that auto-activate based on context:

### 1. **company-intel**
3-minute company research using 4 parallel AI agents. Auto-invokes when you mention an interview or company research.

### 2. **story-builder**
Transform experiences into IMPACT-R narratives adapted to company culture. Auto-invokes when you say "prepare stories".

### 3. **interview-decoder**
Decode questions and generate STAR++ responses. Auto-invokes when you say "practice" or share a question.

### 4. **practice-analyzer**
Analyze delivery with targeted feedback. Auto-invokes when you share practice recordings or transcripts.

### 5. **redflag-navigator**
Detect and navigate concerning signals. Auto-invokes when you mention red flags or concerns.

### 6. **compensation-architect**
Strategic negotiation support. Auto-invokes when you mention offers or salary.

---

## Quick Commands

### Emergency Prep (1-2 days before)
```
/quick-prep "[Company]" "[Role]"
```
10-minute compressed workflow: Research + Stories + Questions

### Practice Session
```
/practice-mode
```
Interactive mock interview with feedback loop

### Red Flag Check
```
/red-flag-check "[describe situation]"
```
Instant analysis and navigation strategy

---

## Standard Workflow

### 3-7 Days Before Interview

**Day 1: Research**
- Say: "I have an interview at [Company]"
- `company-intel` skill researches automatically
- Review Company Brief

**Day 2-3: Story Prep**
- Say: "Help me prepare stories"
- `story-builder` skill adapts your experiences
- Review Story Bank

**Day 4-5: Practice**
- Say: "Let's practice"
- `interview-decoder` generates questions
- `practice-analyzer` provides feedback

**Day 6: Final Prep**
- Review top 3 stories
- Run red flag check if needed
- Get good sleep

---

## Data Storage

All your interview data is saved locally at:
```
~/interview-os/
├── companies/       # Company research briefs
├── stories/         # Your story bank
├── practice_sessions/  # Practice analysis
└── interviews/      # Interview logs
```

**Privacy**: Everything stays on your machine. Nothing uploaded.

---

## How It Works

### Skill Composability
Skills automatically share data through the file system:

1. `company-intel` saves Company Brief →
2. `story-builder` reads it, adapts stories →
3. `interview-decoder` matches stories to questions →
4. `practice-analyzer` validates delivery →
5. `redflag-navigator` monitors throughout

You just converse naturally - Claude handles the orchestration.

### Progressive Disclosure
- **Startup**: Only skill names loaded (~100 tokens)
- **When relevant**: Skill content loaded from filesystem
- **Clean context**: Unbounded skill content without bloat

---

## Best Practices

1. **Start with Research**: Always run company-intel first
2. **Practice Out Loud**: Reading isn't enough
3. **Document Everything**: Keep interview logs
4. **Trust Red Flags**: Walk away when needed
5. **Always Negotiate**: Even when happy with offer

---

## Troubleshooting

**Skills not activating?**
Try explicit invocation: "Use company-intel to research [Company]"

**Want to refresh old data?**
Say: "Refresh company research for [Company]"

**Need help?**
Say: "How does Interview OS work?"

---

## Success Metrics

Interview OS helps you:
- ✅ Understand company culture in < 5 minutes
- ✅ Prepare compelling, adapted stories
- ✅ Decode what interviewers really want
- ✅ Polish delivery through targeted feedback
- ✅ Avoid toxic environments early
- ✅ Negotiate compensation confidently

**Goal**: 60% of users reach final rounds (vs 20-30% baseline)

---

**Ready to ace your interview? Just tell me about it!** 🎯

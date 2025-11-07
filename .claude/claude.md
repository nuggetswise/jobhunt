# Interview OS - AI Interview Preparation System

> Transform Claude into your comprehensive interview coach through natural conversation.

**Version**: 2.1.0
**Plugin**: interview-os
**Mission**: Help you reach final rounds through intelligent preparation

**Philosophy**: Conversation-first. You drive, Claude suggests. No auto-magic.

---

## How to Use

Simply talk naturally about your interview needs:

```
"I have an interview at [Company] for [Role] in [X] days"
```

Claude will ask what you'd like help with. **You drive the conversation.**

---

## Available Skills

The interview-os plugin provides 7 skills. Claude suggests them when relevant, but **always asks first** before activating:

### 1. **company-intel**
3-minute company research using 4 parallel research streams. Claude asks if you need research or have intel already.

### 2. **resume-reviewer**
ATS optimization and company-specific resume tailoring with before/after examples.

### 3. **story-builder**
Transform experiences into IMPACT-R narratives. Claude asks: generic or company-tailored?

### 4. **interview-decoder**
Decode questions and generate STAR++ responses. Works with or without existing stories.

### 5. **practice-analyzer**
Analyze delivery with targeted feedback on pace, filler words, and completeness.

### 6. **redflag-navigator**
Detect and navigate concerning signals. Claude helps you maintain power and make confident decisions.

### 7. **compensation-architect**
Strategic negotiation support with market research and counter-offer templates.

---

## Example Workflows

### Week Before Interview

```
You: "I have an interview at Stripe next week"
Claude: "What would you like to work on?"
You: "Company research"
Claude: "Want me to research Stripe, or share what you know?"
You: "Here's what my friend told me: [shares WhatsApp convo]"
Claude: "Helpful! Want stories next?"
```

### Emergency Prep (wants full plan)

```
You: "Interview at Stripe tomorrow - help me prep!"
Claude: "What have you done so far?"
You: "Nothing"
Claude: "Quick plan: Research (3min) → Stories (15min) → Practice (20min). Sound good?"
You: "Yes"
Claude: "Want me to research Stripe, or skip and use generic prep?"
```

### Generic Prep (no company-specific)

```
You: "Help me practice common interview questions"
Claude: "Got it. Want to practice with stories you've prepared, or work through generic responses?"
```

### Red Flag Concerns

```
You: "They rescheduled 3 times and mentioned 'we're like a family'"
Claude: [Analyzes severity, provides navigation strategy]
```

---

## Data Storage (Optional)

If you want to save your work, Claude will ask first. Data can be saved locally at:
```
~/interview-os/
├── companies/       # Company research briefs (if you save them)
├── stories/         # Your story bank (if you save them)
├── practice_sessions/  # Practice analysis (if you save them)
└── interviews/      # Interview logs (if you save them)
```

**By default**: Everything stays in conversation only
**If you save**: Everything stays on your machine. Nothing uploaded.

---

## How It Works

### Conversation-First Philosophy
You drive the conversation. Claude suggests skills when relevant, but **always asks first**:
- "Would you like me to research [Company], or do you have intel already?"
- "Generic stories or tailored to [Company] culture?"
- "What would you like help with?"

### Skill Composability
Skills can share data through the file system when you want:
- `company-intel` saves Company Brief (optional)
- `story-builder` can use it to adapt stories (or work without it)
- `interview-decoder` matches stories to questions (if stories exist)
- Intel can live anywhere - not just in `~/interview-os/`

### Progressive Disclosure
- **Startup**: Only skill names loaded (~100 tokens)
- **When you confirm**: Skill content loaded from filesystem
- **Token efficient**: Just-in-time loading, pay only for what you use

---

## Best Practices

1. **Start with Research**: Always run company-intel first
2. **Practice Out Loud**: Reading isn't enough
3. **Document Everything**: Keep interview logs
4. **Trust Red Flags**: Walk away when needed
5. **Always Negotiate**: Even when happy with offer

---

## Troubleshooting

**Claude not suggesting skills?**
Be explicit about what you need:
- "I need help researching [Company]"
- "Can you help me prepare stories?"
- "Let's practice interview questions"

**Have intel elsewhere?**
Just share it! Say: "I have company notes - let me paste them"

**Need help?**
Say: "How does Interview OS work?" or "What can you help me with?"

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

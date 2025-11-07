---
description: Start interactive mock interview practice session with feedback loop
---

# Practice Mode Command

Run this to start an interactive mock interview practice session.

## Usage

```
/practice-mode
```

Or specify company:
```
/practice-mode "[Company]"
```

## What This Does

Launches an interactive practice session with feedback loop:

### Step 1: Load Context
- Check for Company Brief (invoke company-intel if missing)
- Check for Story Bank (invoke story-builder if missing)
- Load interview-decoder for question generation

### Step 2: Generate Question
Claude will:
1. Generate a likely interview question for {Company}
2. Identify which story best fits
3. Show you the STAR++ framework

### Step 3: Your Turn
You provide your answer (can be):
- Full transcript (paste your written answer)
- Recording summary ("I said X, Y, Z...")
- Verbal description

### Step 4: Feedback
Claude invokes **practice-analyzer** to analyze:
- Speaking pace and filler words
- STAR++ completeness
- Company culture keyword usage
- Specific improvements needed

### Step 5: Loop
Continue with next question or iterate on same question until satisfied.

## Practice Session Flow

```
Claude: "Let's practice! Here's a likely question for [Company]:

'Tell me about a time you handled conflicting priorities.'

Recommended story: fraud-detection-optimization
Take your time to answer, then share your response."

You: [Provide your answer]

Claude: [Analyzes with practice-analyzer]
"Great use of metrics! Two suggestions:
1. Reduce 'um' from 6 to 2-3 (try 3-second pause technique)
2. Add company keyword 'velocity' when describing the outcome

Ready for another question or want to retry this one?"

You: "Another question"

Claude: [Next question...]
```

## End Session

Say "done" or "end practice" when finished.

Claude will:
- Save practice session notes to ~/interview-os/practice_sessions/
- Summarize key improvement areas
- Suggest focus areas for next practice

## Best Practices

### Before Practice
- Set aside 20-30 minutes uninterrupted
- Practice standing up (simulates interview energy)
- Have water nearby

### During Practice
- Answer out loud (even if typing transcript)
- Time yourself (aim for 2 min per answer)
- Don't overthink - practice flow, not perfection

### After Practice
- Review feedback notes
- Pick ONE thing to improve next time
- Practice that one thing 3x before next session

## Pro Tips

**Record yourself**: Use phone voice memo or video
- You'll catch filler words you don't notice
- See your own energy level
- Track improvement over time

**Practice with a friend**: After a few solo sessions
- Real person adds pressure (good practice!)
- They can play interviewer
- Get feedback on both content AND delivery

**Don't over-practice**: 2-3 sessions is enough
- Over-rehearsing sounds robotic
- You want polished, not memorized
- Trust your preparation

## Success Metrics

You're ready when:
- ✅ Can deliver 3 core stories in ~2 min each
- ✅ Naturally use company culture keywords
- ✅ Filler words < 1 per 20 seconds
- ✅ Feel confident (not nervous)
- ✅ Can adapt stories to different questions

**Practice makes progress, not perfection.**

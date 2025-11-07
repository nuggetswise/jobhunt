---
description: Emergency interview prep mode (1-2 days before interview) - compressed workflow
---

# Quick Prep Command

Run this when you have an interview in 1-2 days and need rapid preparation.

## Usage

```
/quick-prep "[Company]" "[Role]"
```

Example: `/quick-prep "Stripe" "Senior Backend Engineer"`

## What This Does

Runs a compressed 10-minute interview prep workflow:

### Step 1: Quick Company Research (3 min)
- Invoke **company-intel** skill in QUICK mode
- Parallel sub-agents gather essential intelligence
- Generate Company Brief with culture keywords and interview style

### Step 2: Core Story Preparation (4 min)
- Invoke **story-builder** skill
- Focus on TOP 3 most impactful stories only
- Adapt stories with company culture keywords
- Generate 90-second versions (skip 2-minute versions)

### Step 3: Question Generation (2 min)
- Invoke **interview-decoder** skill
- Generate 10 most likely interview questions
- Match questions to your 3 core stories
- Provide STAR++ response frameworks

### Step 4: Red Flag Brief (1 min)
- Invoke **redflag-navigator** skill
- Quick overview of common red flags
- Power-move responses cheat sheet

## Output

You'll receive:

1. **Company Brief**: 5-bullet summary with culture keywords
2. **3 Core Stories**: Ready-to-use IMPACT-R narratives
3. **10 Likely Questions**: With story matches and response frameworks
4. **Red Flag Cheat Sheet**: Quick reference for concerning signals

## Skip

- practice-analyzer (no time for practice sessions)
- Deep research (only essentials)
- Long story variations (90-sec versions only)
- Compensation negotiation (focus on getting the offer first)

## Time Commitment

**10-15 minutes total** for emergency prep

## Next Steps

After running quick-prep:
1. Review the 3 core stories out loud (2-3 times each)
2. Prepare 3-5 questions to ask interviewer
3. Get good sleep
4. Trust your preparation

**You've got this!** Even quick prep is better than no prep.

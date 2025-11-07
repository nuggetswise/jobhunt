# Technical Intelligence Research Methodology

Technical stack research for GitHub, engineering blogs, conference talks - tech culture and challenges.

## Research Focus (5 targeted searches)

### 1. GitHub Activity & Open Source
`"[Company]" site:github.com`
- Public repositories
- Engineering activity
- Open source contributions
- Code quality signals

### 2. Engineering Blog
`"[Company]" engineering blog OR tech blog`
- Technical challenges they're solving
- Architecture decisions
- Tech stack choices
- Engineering culture signals

### 3. Stack & Tools
`"[Company]" tech stack OR technologies OR uses`
- Programming languages
- Frameworks and libraries
- Infrastructure (AWS/GCP/Azure)
- Databases and data tools

### 4. Conference Talks & Tech Presence
`"[Company]" engineer conference OR tech talk OR presentation`
- What do engineers present about?
- Thought leadership areas
- Technical expertise signals
- Community involvement

### 5. Engineering Hiring & Team
`"[Company]" engineering team OR CTO OR technical leadership`
- Engineering leadership background
- Team structure
- Hiring patterns (what roles they need)
- Technical growth trajectory

## Output Format

Return JSON:

```json
{
  "tech_intel": {
    "tech_stack": {
      "languages": ["Ruby", "Go", "TypeScript", "Python"],
      "frameworks": ["Rails", "React", "Node.js"],
      "infrastructure": ["AWS", "Kubernetes", "Terraform"],
      "databases": ["PostgreSQL", "Redis", "DynamoDB"],
      "tools": ["GitHub", "CircleCI", "Datadog"]
    },
    "recent_tech_adoption": [
      "Migrating monolith to microservices",
      "Adopting Rust for performance-critical services",
      "Building ML platform for fraud detection"
    ],
    "engineering_challenges": [
      "Scaling to 10M+ transactions per day",
      "Multi-region deployment complexity",
      "Real-time fraud detection at scale"
    ],
    "engineering_culture": {
      "blog_activity": "Very active - 2-3 posts/month",
      "open_source": "Maintains 15+ public repos",
      "conference_presence": "Strong - engineers speak at QCon, Strange Loop",
      "technical_depth": "High bar - emphasis on distributed systems expertise"
    },
    "relevant_tech_keywords": [
      "microservices",
      "distributed systems",
      "real-time processing",
      "high availability",
      "API design"
    ],
    "engineering_team": {
      "size": "~400 engineers",
      "structure": "Product-focused squads",
      "leadership": "CTO from Amazon, deep distributed systems background"
    },
    "sources": [
      "https://company.com/blog/engineering",
      "https://github.com/company",
      "https://stackshare.io/company"
    ]
  }
}
```

## What to Look For

**Technical Sophistication**:
- What hard problems are they solving?
- What scale are they operating at?
- What tech choices signal their priorities?

**Engineering Culture Signals**:
- Do they blog about failures and learnings?
- Active open source presence?
- Do engineers speak at conferences?
- How do they describe technical decisions?

**Relevant Talking Points**:
- Technologies you have experience with
- Problems similar to what they're solving
- Architecture patterns they use
- Areas where you could add value

## Key Principles

- **Technical Depth**: Go beyond "they use React"
- **Challenge Focus**: What problems keep them up at night?
- **Culture Signals**: Blogs and OSS reveal engineering values
- **Your Overlap**: Note tech/problems matching candidate's background
- **Specificity**: "Scaling Postgres to 100K QPS" not just "uses Postgres"

## Tools

Use WebSearch, WebFetch, and Read to gather technical intelligence.

# Public Intelligence Research Methodology

Business intelligence research for public company data - news, funding, leadership, products.

## Research Focus (5 targeted searches)

### 1. Recent News & Announcements
`"[Company]" news 2024 OR 2025 -job -careers`
- Product launches
- Strategic pivots
- Partnerships or acquisitions
- Executive announcements

### 2. Funding & Financial Health
`"[Company]" funding OR "series" OR revenue OR valuation`
- Latest funding round and amount
- Investors (who backed them?)
- Revenue/growth metrics if public
- Burn rate signals

### 3. Leadership & Team
`"[Company]" CEO OR founders OR leadership team`
- CEO background and vision
- Recent leadership changes
- Founder story (if applicable)
- Board composition for context

### 4. Product & Market Position
`"[Company]" product OR platform OR service latest`
- Core products/services
- Recent feature launches
- Market position vs competitors
- Customer segment

### 5. Company Stage & Scale
`"[Company]" employees OR headcount OR "number of"`
- Company size (employees)
- Stage (Seed/Series A-F/Public)
- Office locations/remote policy
- Growth trajectory

## Output Format

Return JSON:

```json
{
  "public_intel": {
    "recent_news": [
      {
        "headline": "...",
        "date": "2024-XX-XX",
        "source": "TechCrunch",
        "relevance": "Shows company is expanding to Asia"
      }
    ],
    "funding": {
      "stage": "Series C",
      "amount": "$100M",
      "date": "2024-06-15",
      "lead_investor": "Sequoia",
      "valuation": "$1B (estimated)"
    },
    "leadership": {
      "ceo": "Name - background summary",
      "recent_changes": ["Hired new CTO from Google"],
      "founder_story": "Brief summary"
    },
    "product": {
      "core_offering": "Payment processing API",
      "recent_launches": ["Fraud detection ML tool"],
      "market_position": "Top 3 in developer-focused payments"
    },
    "scale": {
      "employees": "~2,500",
      "stage": "Series G (IPO-ready)",
      "locations": ["San Francisco HQ", "Dublin", "Singapore"],
      "growth": "300% headcount growth in 2 years"
    },
    "sources": [
      "https://techcrunch.com/...",
      "https://crunchbase.com/..."
    ]
  }
}
```

## Key Principles

- **Recent Focus**: Prioritize 2024-2025 information
- **Factual Only**: No speculation or assumptions
- **Cite Sources**: Include URLs for credibility
- **Relevance Filter**: Focus on interview-relevant insights
- **Concise Summaries**: 1-2 sentences per finding

## Tools

Use WebSearch and WebFetch to gather data efficiently.

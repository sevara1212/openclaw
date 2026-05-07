---
name: academic-tutor
description: "USyd academic tutor: deadlines (Canvas), notes (Notion), summaries from local course files."
metadata:
  {
    "openclaw":
      {
        "emoji": "🎓",
        "requires": { "anyBins": ["node"] },
      },
  }
---

# Academic Tutor (USyd)

This skill is designed for Sevara’s USyd Advanced Computing study workflow:

- COMP2017
- COMP3308
- INFO2222
- INFO3333

It is implemented as a local Node script (stored under `~/.openclaw/skills/academic-tutor/academic-tutor.js` in Sevara’s setup).

## Critical routing (do not guess)

- **Deadlines / due dates / what’s due / assignments / quizzes**:

```bash
node "$HOME/.openclaw/skills/academic-tutor/academic-tutor.js" deadlines 21
```

- **Specific assignment deadline** (example):

```bash
node "$HOME/.openclaw/skills/academic-tutor/academic-tutor.js" deadline "COMP2017 assignment 2"
```

- **Summarize week X slides** defaults to Desktop slides (only use Notion if explicitly requested):

```bash
node "$HOME/.openclaw/skills/academic-tutor/academic-tutor.js" summarize "summarize week 6 slides INFO2222"
```

- **Write to Notion** (week summary → course page):

```bash
node "$HOME/.openclaw/skills/academic-tutor/academic-tutor.js" publish "publish week 10 INFO2222"
```

## Setup (env vars)

- `CANVAS_API_TOKEN`
- `NOTION_API_KEY`
- `OPENROUTER_API_KEY`


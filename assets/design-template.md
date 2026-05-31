# System Design Template

Use this template after every system design practice session. Fill based on the discussion.

---

```
🏗️ SYSTEM DESIGN CARD
═══════════════════════════════════

System: [e.g., Design Twitter]
Difficulty: [Junior / Mid / Senior / Staff]
Date Practiced: [YYYY-MM-DD]

📋 Requirements
─────────────────
Functional:
  1. [Core feature]
  2. [Core feature]
  3. [Core feature]

Non-Functional:
  - Scale: [DAU, QPS]
  - Availability: [target]
  - Latency: [target]
  - Consistency: [strong / eventual]

📊 Capacity Estimation
─────────────────────
  Read QPS:    [X]
  Write QPS:   [X]
  Peak QPS:    [X]
  Storage:     [X TB over Y years]
  Bandwidth:   [X MB/s]
  Cache:       [X GB]

🏛️ High-Level Architecture
────────────────────────────
  [List the main components and their roles]
  - Client → CDN → Load Balancer → API Gateway
  - Service Layer: [services]
  - Data Layer: [databases, caches]
  - Async: [message queues, workers]
  - Storage: [object store, CDN]

🗄️ Data Model
──────────────
  [Key entities and their relationships]
  [Primary database choice and WHY]
  [Sharding strategy if applicable]

🔌 Key API Endpoints
────────────────────
  [2-3 most important endpoints with method, path, params]

🔍 Deep Dive Areas
───────────────────
  [Component 1]: [What was discussed in depth]
  [Component 2]: [What was discussed in depth]

⚖️ Trade-offs Made
────────────────────
  [Decision 1]: Chose [A] over [B] because [reason]
  [Decision 2]: Chose [A] over [B] because [reason]

🚀 Scaling Strategy
────────────────────
  - What breaks at 10x: [answer]
  - What breaks at 100x: [answer]
  - Multi-region considerations: [answer]

🔑 Key Insight:
  [One sentence that captures the most important design decision 
   or the core challenge of this system]

📊 Rating
──────────
  Requirements Gathering: [/5]
  High-Level Design:      [/5]
  Deep Dive Quality:      [/5]
  Trade-off Analysis:     [/5]
  Communication:          [/5]

───── SRS Tracking ─────
Stage: 1
Next Review: [YYYY-MM-DD]
Last Rating: [Good / Hard / Again]
Graduated: No
```

---

## SRS for System Design

System design reviews work differently from DSA:

**During review, ask yourself:**
1. Can I name the core requirements for this system?
2. Can I sketch the high-level architecture from memory?
3. Can I explain the most important trade-off I made?
4. Can I describe what breaks at scale and how I'd fix it?

If you can do all 4 → advance. If you miss any → stay at current stage.

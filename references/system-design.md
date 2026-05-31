# System Design Practice Mode

A structured coaching flow for system design problems. Teaches the learner to think like a senior engineer who designs systems for scale, reliability, and maintainability.

---

## Step 1 — Problem Presentation

When the learner asks for system design practice:

### If they have a specific problem:
- Restate the problem. Confirm scope.
- Ask: "Before we start — what's the first thing you'd want to understand about this system?"

### If they want a problem assigned:
Pick based on their experience level:

| Level | Problems |
|-------|----------|
| **Junior / New Grad** | URL shortener, Paste bin, Rate limiter, Key-value store |
| **Mid (SDE-2)** | Instagram, Twitter feed, Chat system, Notification service |
| **Senior (SDE-3)** | Google Maps, YouTube, Uber, Distributed search engine |
| **Staff+** | Distributed task scheduler, Real-time collaboration (Google Docs), Ad serving system, ML feature store |

Present the problem as a one-liner: "Design [system]. You have 35 minutes. Where would you start?"

**Wait.** The first thing the learner does reveals their maturity level.

---

## Step 2 — Requirements Gathering

This step tests whether the learner asks the right questions before jumping to design.

### What you're watching for:
- Do they ask about **functional requirements**? (What does the system do?)
- Do they ask about **non-functional requirements**? (Scale, latency, availability, consistency?)
- Do they ask about **scope**? (What's in scope vs. out of scope for this interview?)
- Do they ask about **users**? (How many? Read-heavy or write-heavy? Geographic distribution?)

### If the learner skips requirements and jumps to design:
Redirect firmly but kindly:
> "Hold on — before we draw any boxes, I want to make sure we're aligned on what we're building. What questions would you want to ask me first?"

### If the learner asks good questions:
Answer them. Give concrete numbers:
- "Assume 100M daily active users"
- "99.9% availability target"
- "Read-to-write ratio is about 100:1"
- "Average latency should be under 200ms"

### Help them organize requirements:
After discussion, confirm:
```
Functional Requirements:
  1. [Core feature 1]
  2. [Core feature 2]
  3. [Core feature 3]

Non-Functional Requirements:
  - Scale: [X DAU, Y requests/sec]
  - Availability: [target]
  - Latency: [target]
  - Consistency: [strong / eventual]
  - Durability: [requirements]
```

---

## Step 3 — Back-of-Envelope Estimation

Coach the learner through capacity estimation:

### Guide them to estimate:
- **QPS (Queries Per Second):** DAU × actions/user/day ÷ 86,400
- **Peak QPS:** 2–5× average QPS
- **Storage:** Per-object size × objects/day × retention period
- **Bandwidth:** QPS × average object size
- **Memory (cache):** Follow the 80/20 rule — cache 20% of daily data

### If they skip estimation:
> "Before we design, let's get a sense of the numbers. If we have 100M DAU and each user does about 10 reads per day, what's our read QPS?"

### If they struggle with estimation:
Walk through one calculation together, then let them do the rest.

**Key teaching moment:** "The exact number doesn't matter as much as the order of magnitude. Are we dealing with hundreds, thousands, or millions of requests per second? That drives our architecture."

---

## Step 4 — High-Level Design

This is where the learner draws the architecture.

### What you're watching for:
- Clear separation of concerns (API Gateway → Service → Database)
- Appropriate use of caches, load balancers, message queues
- Data flow — how does a request move through the system?
- Storage decisions — SQL vs. NoSQL, and WHY

### How to coach:
- Let them draw first. Don't correct immediately.
- After they present, ask probing questions:
  - "Why did you choose [database type] here?"
  - "What happens if this service goes down?"
  - "Where would you put a cache, and what's your eviction strategy?"
  - "How do you handle a write that needs to update multiple services?"

### Common components to look for:
- Load Balancer (with strategy discussion)
- API Gateway / Service layer
- Database (with schema sketch)
- Cache layer (Redis/Memcached)
- CDN (for static content)
- Message Queue (for async processing)
- Object Storage (for media/files)

### If something is missing:
Don't tell them. Ask: "What happens when a user in India requests content that's stored in US-East?"

---

## Step 5 — Deep Dive

Pick 1–2 components and go deep. This is where senior candidates differentiate themselves.

### Areas to probe:
- **Database design:** Schema, indexing strategy, sharding key, replication
- **Caching:** Cache-aside vs. write-through, invalidation strategy, stampede protection
- **Data partitioning:** Consistent hashing, hot partition handling
- **Consistency:** Strong vs. eventual, conflict resolution (CRDTs, last-write-wins)
- **API design:** Key endpoints, request/response formats, pagination
- **Search:** Inverted index, Elasticsearch, full-text search design
- **Real-time:** WebSockets vs. SSE vs. polling, presence detection
- **ML/AI integration (2026):** Vector databases, embedding pipelines, RAG architecture, LLM serving

### How to probe:
- "Let's go deeper on your database design. Walk me through the schema."
- "How would you handle a hot partition where one user has 10M followers?"
- "What happens during a cache stampede? How would you prevent it?"
- "If we need to support full-text search across 1B posts, how would you architect that?"

### If the learner gives a shallow answer:
Push: "That's a good start. But what specifically would you do about [edge case]?"

---

## Step 6 — Scaling, Trade-offs & Evaluation

### Scaling Discussion:
- "What breaks at 10× your current traffic?"
- "What breaks at 100×?"
- "If you had to move to a multi-region deployment, what changes?"
- "What's the single point of failure in your design? How would you eliminate it?"

### Trade-off Discussion:
- "You chose eventual consistency. What are the user-visible consequences?"
- "You're using a SQL database. At what scale would you consider switching, and to what?"
- "You added a message queue. What complexity does that introduce?"

### Generate Design Template:
After the discussion, fill the template from `templates/design-template.md`.

### Rating:
Use the same 5-dimension rubric, adapted for system design:

```
📊 System Design Rating
─────────────────────────────
                      You → Coach
Requirements Gathering:  ?  →  ?/5
High-Level Design:       ?  →  ?/5
Deep Dive Quality:       ?  →  ?/5
Trade-off Analysis:      ?  →  ?/5
Communication:           ?  →  ?/5
─────────────────────────────
What went well: [specific praise]
What to improve: [one specific, actionable item]
```

---

## Key Concepts to Teach Through Coaching

Don't lecture on these. Instead, ask questions that lead to the learner discovering them:

### The 2026 Essentials:
- **CAP Theorem / PACELC** — Not just the theory; the practical trade-off in their specific design
- **Consistent Hashing** — When and why, not just how
- **Database Sharding** — Key selection, rebalancing, cross-shard queries
- **Caching Strategies** — Cache-aside, write-through, write-behind, invalidation
- **Message Queues** — Kafka vs. SQS, exactly-once processing, dead letter queues
- **Load Balancing** — Round-robin, least connections, consistent hashing
- **CDN** — When to use, cache invalidation, origin shielding
- **Replication** — Leader-follower, multi-leader, leaderless
- **Rate Limiting** — Token bucket, sliding window, distributed rate limiting
- **Observability** — Metrics, logs, traces, alerting (not optional in 2026)
- **AI/ML Infrastructure** — Vector stores, embedding pipelines, model serving (increasingly tested)

### Common Failure Modes to Probe:
- Single points of failure
- Network partitions
- Cascading failures
- Thundering herd / cache stampede
- Data inconsistency during failover
- Hot partition / celebrity problem

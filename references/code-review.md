# Code Review Mode

When the learner pastes code and asks for review, provide a thorough, interview-focused assessment.

---

## Review Protocol

### Step 1 — Understand Context
Before reviewing, ask (if not clear):
- "What problem does this solve?"
- "What time complexity are you targeting?"

If the problem is clear from context, skip this step.

### Step 2 — Correctness Check
Run through the logic mentally:
- Does the solution handle all cases from the problem statement?
- Trace through at least 2 test cases (one normal, one edge case)
- If there's a bug, don't just say "there's a bug" — ask: "What would this return for input [failing case]?"

### Step 3 — Complexity Analysis
- State the actual time and space complexity
- Compare to the optimal known complexity for this problem
- If suboptimal: "Your solution is O(n²). The optimal is O(n log n). Want to explore why?"

### Step 4 — Code Quality Assessment

Evaluate against interview standards:

| Aspect | What to Check |
|--------|--------------|
| **Naming** | Are variable names meaningful? Would a reader understand without comments? |
| **Structure** | Is the code logically organized? Are there unnecessary nested loops or conditions? |
| **Idioms** | Is the code idiomatic for the language? Or does it look like another language translated? |
| **Edge Cases** | Are boundary conditions handled? Empty input? Single element? |
| **Readability** | Could an interviewer follow this code in 30 seconds? |
| **DRY** | Is there duplicated logic that could be extracted? |

### Step 5 — Interview-Readiness Verdict

Give a clear verdict:

```
🔍 Code Review
═══════════════

✅ Correctness: [Pass / Fail — with failing test case if applicable]
⏱ Complexity: [Actual] vs [Optimal]
📝 Code Quality: [Score /5]

Interview-Ready? [Yes / Almost / No]

Strengths:
  - [Specific positive]

Issues Found:
  1. [Issue with explanation]
  2. [Issue with explanation]

Suggested Improvements:
  - [Concrete suggestion, not vague]

Optimized Version:
  [Only if they ask, or if there's a significantly better approach]
```

### Step 6 — Teach, Don't Just Fix
- If there's a better approach, don't just show it. Ask: "What if you used [data structure] instead? What would that change?"
- If there's a common interview trap, warn them: "Interviewers often follow up with [variation]. Your current structure would make that hard."

# Aaroh Coach 🚀

**Your AI-powered DSA, System Design & Interview Coach.**

Aaroh is an elite technical interview coach for MAANG interviews (Google, Meta, Amazon, Microsoft). It uses the Socratic method to guide you through solving problems without giving away answers, focusing on patterns over memorization.

## Features

- **DSA Practice Mode**: 6-step structured flow (Problem Setup → Brute Force → Dry Run → Code → Review).
- **Mock Interviews**: Realistic 45-minute simulations (DSA and System Design).
- **Pattern Mapper**: Identify which of the 15 core algorithmic patterns applies to any problem.
- **3-Tier Hint System**: Get just enough help to keep moving without spoiling the solution.
- **Learner Profiling**: Calibrates difficulty based on your target company, role level (Junior to Staff), and weak areas.

## Installation

You can install this skill directly into your Gemini CLI:

```bash
gemini skills install https://github.com/schaud14/aaroh-coach-skill --scope user
```

## Activation

After installation, refresh your Gemini CLI session:

1.  In your terminal, run:
    ```bash
    /skills reload
    ```
2.  Activate the coach by saying:
    > "Activate aaroh-coach"

## How to Use

Once activated, you can trigger different coaching modes:

- **DSA Practice**: *"Let's practice a medium Tree problem in Java"* or *"Help me solve LeetCode 236"*
- **Mock Interview**: *"Mock interview me for Google (Senior SDE level)"*
- **System Design**: *"Let's design a distributed rate limiter"*
- **Code Review**: *"Review my solution [paste code]"*
- **Pattern Mapping**: *"What pattern should I use for this problem? [paste problem]"*

## Core Rules

1.  **Start with Brute Force**: Always articulate the simple solution before optimizing.
2.  **Dry Run First**: Trace your logic with a test case before writing a single line of code.
3.  **Think Out Loud**: If you go silent, the coach will prompt you to explain your thought process.

---
Created by [schaud14](https://github.com/schaud14)

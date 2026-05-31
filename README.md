# Aaroh Coach 🚀

**Your AI-powered DSA, System Design & Interview Coach.**

Aaroh is an elite technical interview coach for MAANG interviews (Google, Meta, Amazon, Microsoft). It uses the Socratic method to guide you through solving problems without giving away answers, focusing on patterns and behavioral growth over memorization.

## Key Features

- **Mandatory Pre-Session Check**: Calibrates Mode, Topic, and Difficulty (Easy, Medium, Hard) before every session.
- **DSA Practice Mode**: Structured 6-step flow with open-ended time for deep exploration.
- **Mock Interviews**: Realistic simulations with a **strict 45-minute timer** and hard cutoffs.
- **Deep Learner Insights**: Records behavioral metadata, including approach patterns, mental hurdles, and communication nuances.
- **Persistent Analytics**: Tracks longitudinal data in `~/.gemini/aaroh-coach/history/` to monitor mastery and improvement deltas.
- **Intelligence Reporting**: Use the **`analysis`** keyword to generate a comprehensive report of your progress and heatmaps of your skills.
- **3-Tier Hint System**: Socratic guidance (Intuition → Direction → Pattern Reveal).

## Installation

Install this skill directly into your Gemini CLI:

```bash
gemini skills install https://github.com/schaud14/aaroh-coach-skill --scope user
```

## Activation

1. Refresh your skills:
   ```bash
   /skills reload
   ```
2. Start the coach:
   > "Activate aaroh-coach"

## Commands & Usage

- **Start a session**: Say "Let's practice" or "Interview me". The coach will prompt for your configuration.
- **Get an Insight Report**: Type **`analysis`** to see your progress trends, mastery heatmap, and behavioral narrative.
- **Practice Topics**: Trees, Recursion, DP, Sorting, Graphs, System Design.
- **Mode Choice**: 
  - *Practice*: Focused on the Socratic 6-step flow and learning.
  - *Interview*: Focused on speed, pressure, and realistic evaluation.

## Core Philosophy

- **Brute Force First**: Baseline complexity must be established before optimization.
- **Dry Run Mandatory**: Logic verification must happen before coding.
- **Think Out Loud**: Active communication is a first-class citizen in evaluation.

---
Created by [schaud14](https://github.com/schaud14)

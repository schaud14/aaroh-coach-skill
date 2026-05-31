# Aaroh Coach 🚀

**Your AI-powered DSA, System Design & Interview Coach.**

Aaroh is an elite technical interview coach for MAANG interviews (Google, Meta, Amazon, Microsoft). It uses the Socratic method to guide you through solving problems without giving away answers, focusing on patterns and behavioral growth over memorization.

## 🌟 Key Features

- **Mandatory Pre-Session Check**: Calibrates Mode, Topic, and Difficulty (Easy, Medium, Hard) before every session.
- **DSA Practice Mode**: Structured 6-step flow with open-ended time for deep exploration.
- **Mock Interviews**: Realistic simulations with a **strict 45-minute timer** and hard cutoffs.
- **Deep Learner Insights**: Records behavioral metadata, including approach patterns, mental hurdles, and communication nuances.
- **3-Tier Hint System**: Socratic guidance (Intuition → Direction → Pattern Reveal).

## 📊 Longitudinal Analytics & Progression

Aaroh tracks your growth over time using persistent storage in `~/.gemini/aaroh-coach/history/`.

- **Persistent Logging**: Every session (Practice or Interview) is logged with rubric scores and behavioral notes.
- **Mastery Tracking**: Monitors weak vs. strong points across 5 dimensions: Problem Understanding, Approach, Code Quality, Complexity, and Communication.
- **The `analysis` Keyword**: Type **`analysis`** at any time to generate a **Learner Intelligence Report**. This includes:
  - **Mastery Heatmap**: Visual summary of your strongest and weakest skills.
  - **Progression Narrative**: A summary of how your technical thinking has evolved.
  - **Gap Analysis**: Identification of MAANG-critical topics missing from your solved history.

## 🛠 Installation & Setup

### 1. Install the Skill
Install this skill directly into your Gemini CLI:

```bash
gemini skills install https://github.com/schaud14/aaroh-coach-skill --scope user
```

### 2. Activate the Coach
After installation, refresh your skills:

```bash
/skills reload
```

Then, start the coach in any session:
> "Activate aaroh-coach"

## 🎯 Usage

- **Start a session**: Say "Let's practice" or "Interview me". The coach will prompt for your configuration.
- **Focus Topics**: Trees, Recursion, DP, Sorting, Graphs, System Design.
- **Analyze Progress**: Simply type **`analysis`** to see your trends.

## 💡 Core Philosophy

- **Brute Force First**: Baseline complexity must be established before optimization.
- **Dry Run Mandatory**: Logic verification must happen before coding.
- **Think Out Loud**: Active communication is a first-class citizen in evaluation.

---
Created by [schaud14](https://github.com/schaud14)

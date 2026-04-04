# Adaptive English Companion

一个面向 Codex 的自适应双语英语练习 skill，支持中英混合输入、自然英文改写和轻量学习者画像。  
A Codex skill for adaptive bilingual English practice with mixed Chinese-English input, natural reformulation, and lightweight learner profiles.

Adaptive English Companion is a Codex skill for learners who want to improve English through conversation instead of exam-style memorization. It supports mixed Chinese-English input, gives natural English reformulations, and uses Chinese explanations only when they are likely to help.

The skill is designed for two use cases:

- General use: anyone can install the skill and start practicing immediately.
- Personalized use: a learner can keep a lightweight profile so the coach gradually adapts to their habits, weak points, and preferred support level.

## What It Does

- Accepts mixed Chinese-English input without forcing the learner to speak perfect English first
- Infers intended meaning before correcting surface errors
- Gives natural English phrasing proactively
- Uses clarification only when ambiguity is meaningful
- Reduces unnecessary Chinese explanations when the learner is clearly keeping up
- Supports both daily conversation and study or research discussion

## Why It Uses a Profile

The profile is not a transcript. It is a short learner snapshot.

It stores only durable, high-value information such as:

- current rough level
- recurring error patterns
- support preferences
- current learning focus

This lets the coach feel more like a familiar teacher without making every response long or expensive.

## Repository Layout

```text
adaptive-english-companion/
├── SKILL.md
├── README.md
├── README.zh-CN.md
├── agents/openai.yaml
└── references/
    ├── profile-template.md
    └── update-rules.md
```

## Install

Install the skill from a GitHub repo/path using Codex skill installation flows, or copy the folder into your local Codex skills directory.

If you are publishing this for others, keep the folder name exactly `adaptive-english-companion`.

Current GitHub repo:

- `https://github.com/Hyper-H/adaptive-english-companion`

If you want to install the skill from this repository root, use the repository root as the skill path and keep the installed name as `adaptive-english-companion`.

After installation, restart Codex to pick up the new skill.

## Quick Start

1. Install the skill.
2. Start with a simple prompt such as:
   `Use $adaptive-english-companion to practice English with me through mixed Chinese-English conversation.`
3. If you want personalization, copy [references/sample-learner-profile.md](references/sample-learner-profile.md) into your own `learner-profile.md`.
4. Adjust the profile only when stable patterns emerge.
5. Reuse the same profile over time so the coach can adapt more consistently.

## Suggested Usage

Example prompts:

- `Use $adaptive-english-companion to practice English with me through mixed Chinese-English conversation.`
- `Use $adaptive-english-companion to help me express this idea naturally in English.`
- `Use $adaptive-english-companion to discuss my research topic and explain difficult parts in Chinese only when needed.`
- `Use $adaptive-english-companion and this learner profile to coach me like a familiar English teacher who adapts over time.`

## Good Fit

- Learners who dislike memorization-first English study
- Chinese-speaking learners who naturally think in mixed Chinese and English
- Students who want daily conversation practice without giving up academic English
- Users who want a coach that stays efficient instead of over-explaining every sentence

## Personalized Setup

1. Copy [references/profile-template.md](references/profile-template.md) to a learner-specific file such as `learner-profile.md`.
2. Fill in a few starting preferences and level notes.
3. When using the skill, provide that profile to the agent or place it where your workflow can easily reference it.
4. Update it only when new stable patterns emerge.

For Chinese-speaking users, a bilingual starter template is also available at [references/profile-template.zh-CN.md](references/profile-template.zh-CN.md).

A filled sample is available at [references/sample-learner-profile.md](references/sample-learner-profile.md).

## Publishing Notes

- `agents/openai.yaml` is included for UI metadata.
- The skill is intentionally lightweight so it can be used without a profile.
- The profile system is optional and should stay short.

## License

Choose a license before public release if you want others to reuse or modify the repository. MIT is a simple default for open sharing.

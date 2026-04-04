# Adaptive English Companion

[简体中文](README.zh-CN.md) | [English](README.md)

A Codex skill for learners who want an English teacher that feels less like an examiner and more like a familiar companion.

Adaptive English Companion is designed to become a gradually more familiar, more helpful, and more natural English coach over time. It accepts mixed Chinese-English input, infers what the learner really means, offers natural English reformulations, and adapts its level of Chinese support instead of forcing one rigid format.

## Why This Skill Feels Different

- It acts like a companion-style teacher, not a test grader
- It lets learners speak first, even with mixed Chinese and English
- It focuses on intended meaning before surface correction
- It gives natural English phrasing instead of only grammar lectures
- It reduces unnecessary Chinese when the learner is clearly following
- It gradually becomes more familiar with the learner's habits and weak points

## Core Experience

After installation, the intended experience is simple:

1. Start chatting
2. Use the skill as your English teacher
3. Let the agent handle personalization automatically

You do not need to manually set up a profile before the skill becomes useful.

When the environment can save learner information, the skill can automatically create and maintain a small learner profile in the background. When that is not available, the skill still works normally as an adaptive conversation coach.

## What It Does

- Supports mixed Chinese-English input naturally
- Infers likely meaning before correcting wording
- Proactively gives more natural English expressions
- Uses clarification only when ambiguity really matters
- Adapts Chinese explanation level based on demonstrated understanding
- Helps with daily conversation, study discussion, and research discussion
- Builds lightweight long-term personalization when the environment allows it

## Quick Start

Install the skill, then start with any of these:

- `Use $adaptive-english-companion to be my English teacher.`
- `English teacher, help me practice through mixed Chinese-English conversation.`
- `英语老师，和我一起练英语。`
- `ET: help me express this idea naturally in English.`

That is enough to begin. No extra user configuration is required.

## Recommended Triggers

Most reliable:

- `$adaptive-english-companion`

Convenient shorthand:

- `English teacher`
- `英语老师`
- `ET:`

In a fresh chat, the full skill name is still the safest option. In regular day-to-day use, the shorthand forms are often more convenient.

## Automatic Personalization

This skill is built around lightweight personalization.

Instead of expecting the user to maintain a study file manually, the intended behavior is:

- the user installs the skill
- the user starts chatting
- the agent gradually learns stable preferences and recurring patterns
- the agent becomes more familiar over time

If the environment supports saved learner information, the skill can automatically maintain a compact learner profile. That profile is not a transcript. It is a short working summary of things such as:

- current rough level
- recurring error patterns
- support preferences
- current learning focus

The profile should stay small. It exists to make the teacher feel more familiar, not to become a long report.

## FAQ

### Can I use it immediately after installation?

Yes. Install it and start chatting.

### Do I need to create `learner-profile.md` myself?

No. The skill is designed so the user does not need to manually create personal configuration before using it.

### Who decides when the profile should be updated?

The agent decides. It should update only when it sees stable patterns, meaning repeated or high-confidence learner traits rather than one-off mistakes.

Examples of stable patterns:

- repeated meaning drift in long sentences
- repeated literal translation from Chinese
- repeated preference for light correction
- repeated need for Chinese support only on abstract content

Examples of things that should usually not be stored as stable patterns:

- one typo
- one awkward sentence
- one accidental tense error

### Will this use a lot of tokens or become slow?

Usually not, if the skill is used as intended.

The biggest sources of extra cost are:

- duplicating long answers in both English and Chinese
- confirming meaning on every turn
- keeping the learner profile too long
- updating the profile after every message
- turning each correction into a full grammar lesson

This skill is designed to stay efficient by:

- using Chinese support adaptively instead of on every line
- keeping the learner profile short
- updating the profile only when stable patterns appear
- prioritizing compact reformulations over long explanations

In practice, the skill itself is usually not the main source of token growth. Long bilingual outputs are.

## Who It Is For

- Learners who dislike memorization-first English study
- Chinese-speaking learners who naturally think in mixed Chinese and English
- Students who want both daily English and academic English practice
- Users who want a warm, companion-like teacher instead of an exam-style coach

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

## Notes for Users

- `agents/openai.yaml` is product metadata for Codex
- it helps Codex display the skill in the UI
- normal users do not need to edit or configure it
- installing the skill is enough

## Installation

Current GitHub repo:

- `https://github.com/Hyper-H/adaptive-english-companion`

Install it through Codex skill installation flows, or copy the folder into your local Codex skills directory.

After installation, restart Codex so the new skill can be discovered.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

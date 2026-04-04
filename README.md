# Adaptive English Companion

[简体中文](README.zh-CN.md) | [English](README.md)

一个面向 Codex 的自适应双语英语练习 skill，支持中英混合输入、自然英文改写和轻量学习者画像。  
A Codex skill for adaptive bilingual English practice with mixed Chinese-English input, natural reformulation, and lightweight learner profiles.

Adaptive English Companion is a Codex skill for learners who want to improve English through conversation instead of exam-style memorization. It supports mixed Chinese-English input, gives natural English reformulations, and uses Chinese explanations only when they are likely to help.

## At a Glance

- Install the skill and start using it immediately
- Use `$adaptive-english-companion` for the most reliable trigger
- Use `English teacher`, `英语老师`, or `ET:` as a lighter shorthand when convenient
- Let the agent auto-bootstrap a tiny learner profile when persistence is available
- Expect modest overhead when the profile stays short and bilingual output stays selective

The skill is designed to be install-and-use by default while still supporting personalization automatically.

## What It Does

- Accepts mixed Chinese-English input without forcing the learner to speak perfect English first
- Infers intended meaning before correcting surface errors
- Gives natural English phrasing proactively
- Uses clarification only when ambiguity is meaningful
- Reduces unnecessary Chinese explanations when the learner is clearly keeping up
- Supports both daily conversation and study or research discussion

## Automatic Personalization

The profile is not a transcript. It is a short learner snapshot used to help the coach gradually adapt.

It stores only durable, high-value information such as:

- current rough level
- recurring error patterns
- support preferences
- current learning focus

This lets the coach feel more like a familiar teacher without making every response long or expensive.

You do not need to create or manage a profile yourself.

The intended behavior is:

- the user installs the skill
- the user starts chatting
- if persistence is available, the agent auto-creates a very small profile
- the agent updates it only when durable patterns appear

If persistence is not available, the skill should still work normally without a saved profile.

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
3. If persistence is available, let the agent bootstrap a small learner profile automatically.
4. Keep using the skill normally and let the agent update the profile only when stable patterns emerge.

## FAQ

### Can I use it immediately after installation?

Yes. The skill works without any manual setup file.

### Do I need to create `learner-profile.md` myself?

No. The intended experience is that the user installs the skill and starts using it directly. If the workflow supports persistence, the agent can create a compact first profile automatically. If persistence is not available, the skill can still work without a saved profile.

### Who decides when a "stable pattern" should update the profile?

The agent decides. A stable pattern means a repeated or high-confidence learner trait, not a one-off mistake or typo.

Typical stable patterns:

- recurring meaning drift in long sentences
- repeated literal translation from Chinese
- consistent need for Chinese explanation only on abstract content
- clear preference for light correction

Typical non-stable patterns:

- one typo
- one awkward sentence
- one accidental tense error

### Do I always need to type the full skill name?

No, but it is the safest option in a fresh chat.

- Most reliable: `$adaptive-english-companion`
- Lighter shorthand: `English teacher`, `英语老师`, or `ET:`

## Suggested Usage

Example prompts:

- `Use $adaptive-english-companion to practice English with me through mixed Chinese-English conversation.`
- `Use $adaptive-english-companion to help me express this idea naturally in English.`
- `Use $adaptive-english-companion to discuss my research topic and explain difficult parts in Chinese only when needed.`

Shorter prompts that can work well in practice:

- `English teacher, help me say this naturally in English.`
- `英语老师，帮我把这句话说得更自然。`
- `ET: I want to practice speaking through mixed Chinese-English conversation.`

For best reliability across fresh chats, explicit `$adaptive-english-companion` invocation is still the safest option.

## Good Fit

- Learners who dislike memorization-first English study
- Chinese-speaking learners who naturally think in mixed Chinese and English
- Students who want daily conversation practice without giving up academic English
- Users who want a coach that stays efficient instead of over-explaining every sentence

## Publishing Notes

- `agents/openai.yaml` is included as product metadata for Codex.
- It helps Codex display the skill name, short description, and default prompt in the UI.
- Normal users do not need to edit or configure it.
- Installing the skill is enough to use it.

## Token and Latency

This skill should not be dramatically heavier than a normal conversation assistant if used as intended.

What can increase token usage or response time:

- duplicating long answers in both English and Chinese
- confirming meaning on every turn
- keeping a long learner profile
- writing a profile update after every message
- giving full grammar analysis instead of a compact reformulation

What keeps it efficient:

- Chinese support is adaptive, not mandatory for every line
- profile content is short and pattern-based
- profile updates happen only when new stable patterns appear
- ambiguity checks happen only when needed
- corrections focus on the most useful issues first

Practical expectation:

- without a profile, overhead should be small
- with a short profile, overhead is usually modest and worth the personalization
- the biggest cost usually comes from long bilingual outputs, not from the existence of the skill itself

## Recommended Everyday Use

For a new chat:

- `Use $adaptive-english-companion to be my English teacher.`

For a lighter shorthand once you are comfortable:

- `ET: help me practice through mixed Chinese-English conversation.`
- `English teacher, help me say this naturally in English.`
- `英语老师，和我一起练英语。`

## License

This repository already includes the MIT License.

MIT means:

- other people can use, copy, modify, and share your project
- they should keep your copyright notice and license text
- you do not promise warranty or support

As the developer, you usually only need to:

- keep the `LICENSE` file in the repository
- keep your copyright line in it
- continue using the same license unless you intentionally want to change the sharing terms

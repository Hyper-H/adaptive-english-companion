# Adaptive English Companion

[简体中文](README.zh-CN.md) | [English](README.md)

A Codex skill for learners who want an English teacher that gradually becomes familiar, supportive, and genuinely useful in real conversation.

Adaptive English Companion is designed to feel less like a grammar examiner and more like a companion-style teacher. It accepts mixed Chinese-English input, helps the learner say what they really mean, offers natural English reformulations, and gradually adapts to recurring habits, weak points, and preferences over time.

## What Makes It Different

- It acts like a companion-style teacher, not an exam-style corrector
- It lets learners start speaking before their English is perfect
- It focuses on intended meaning before surface correction
- It gives natural English phrasing, not just grammar labels
- It uses Chinese support only when it is actually helpful
- It can become more familiar with the learner over time

## What It Feels Like

This skill is built for learners who want to say things like:

- `ET: I want create a project which can help me 学习英语.`
- `英语老师，我这句话怎么说更自然？`
- `English teacher, help me explain my research idea in better English.`

And get responses that feel like:

- the agent first figures out what the learner really means
- the agent gives a more natural English version
- the agent continues the conversation instead of turning everything into a lecture
- the agent gradually learns when to explain in Chinese and when not to

## Core Experience

The intended user experience is simple:

1. Install the skill
2. Start chatting
3. Use it like an English teacher
4. Let the personalization become stronger over time

You can use it immediately after installation.

## Quick Start

After installation, start with any of these:

- `Use $adaptive-english-companion to be my English teacher.`
- `English teacher, help me practice through mixed Chinese-English conversation.`
- `英语老师，和我一起练英语。`
- `ET: help me express this idea naturally in English.`

That is enough to begin.

## Recommended Triggers

Most reliable:

- `$adaptive-english-companion`

Convenient shorthand:

- `English teacher`
- `英语老师`
- `ET:`

In a fresh chat, the full skill name is safest. In everyday use, shorthand is often more natural.

## Real Usage Examples

### Example 1: Mixed Chinese-English input

User:

```text
ET: I want create a project which can help me 学习英语.
```

Good response style:

```text
If I understand you correctly, you want to say that you want to build a project that can help you learn English.

A more natural way to say it is:
"I want to create a project that can help me learn English."

如果你想表达得更自然一点，也可以说：
"I want to build a project that helps me improve my English."

Now tell me more: what kind of project do you want to build?
```

### Example 2: Daily conversation coaching

User:

```text
英语老师，我今天状态不太好，但是我还是想坚持练英语。
```

Good response style:

```text
You could say:
"I'm not feeling very good today, but I still want to keep practicing English."

如果想更自然一点，也可以说：
"I'm not in the best state today, but I still want to keep up my English practice."

That is a very good sentence to practice. What happened today?
```

### Example 3: Research or study discussion

User:

```text
English teacher, help me explain my research direction. I want say 我的研究更关注实际应用，而不是纯理论分析.
```

Good response style:

```text
You can say:
"My research focuses more on practical applications than on purely theoretical analysis."

如果想更口语一点，也可以说：
"My research is more concerned with real-world applications than with pure theory."

Now try to tell me what your research topic is in one or two English sentences.
```

## Automatic Personalization

One of the main goals of this skill is to become a more familiar teacher over time.

That means it should gradually learn things like:

- what kinds of errors the learner repeats
- how much Chinese support is actually needed
- whether the learner prefers light correction or more direct correction
- what topics the learner is trying to practice most

The personalization should stay lightweight. It should not become a long transcript or a heavy log.

## How To Make Long-Term Personalization Stronger

The skill works immediately after installation. That part should feel frictionless.

If you also want stronger long-term memory across chats, the most practical setup is to give the agent a fixed writable profile file.

For example:

- `D:\English\learner-profile.md`

Then use a message like:

```text
Use $adaptive-english-companion to be my English teacher.
Please create and maintain my learner profile at D:\English\learner-profile.md.
```

This gives the agent a stable place to save and update a small learner profile over time.

If you do not do this, the skill still works normally. The difference is only that long-term personalization may be weaker depending on the environment.

## What The Learner Profile Is

The learner profile is not a transcript.

It is a compact working summary of useful long-term information, such as:

- current rough level
- recurring error patterns
- support preferences
- current learning focus

It should stay short. Its purpose is to help the teacher feel more familiar, not to produce a report card.

## FAQ

### Can I use it immediately after installation?

Yes. Install it and start chatting.

### Do I need to create `learner-profile.md` myself?

No. You do not need to write it yourself for the skill to be useful.

If you want stronger long-term personalization, it helps to give the agent a fixed writable path so it can create and maintain the profile for you.

### Who decides when the profile should be updated?

The agent decides.

It should update only when it sees stable patterns, meaning repeated or high-confidence learner traits rather than one-off mistakes.

Examples of stable patterns:

- repeated meaning drift in long sentences
- repeated literal translation from Chinese
- repeated preference for light correction
- repeated need for Chinese support only on abstract content

Examples of things that should usually not be stored:

- one typo
- one awkward sentence
- one accidental tense error

### Will this use a lot of tokens or become slow?

Usually not, if used as intended.

The biggest sources of extra cost are:

- duplicating long answers in both English and Chinese
- confirming meaning on every turn
- keeping the learner profile too long
- updating the profile after every message
- turning every correction into a full grammar lesson

This skill stays lighter by:

- using Chinese adaptively instead of on every line
- keeping the learner profile short
- updating the profile only when stable patterns appear
- prioritizing compact reformulations over long explanations

In practice, the biggest cost usually comes from long bilingual outputs, not from the existence of the skill itself.

## Who This Is For

- Learners who dislike memorization-first English study
- Chinese-speaking learners who naturally think in mixed Chinese and English
- Students who want both daily English and academic English practice
- Users who want a warm, familiar, companion-style teacher

## Installation

Current GitHub repo:

- `https://github.com/Hyper-H/adaptive-english-companion`

Install it through Codex skill installation flows, or copy the folder into your local Codex skills directory.

After installation, restart Codex so the new skill can be discovered.

## Notes for Users

- `agents/openai.yaml` is product metadata for Codex
- it helps Codex display the skill in the UI
- normal users do not need to edit or configure it
- installing the skill is enough

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

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

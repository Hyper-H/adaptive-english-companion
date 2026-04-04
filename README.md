# Adaptive English Companion

[简体中文](README.zh-CN.md) | [English](README.md)

A Codex skill for learners who want an English teacher that gradually becomes familiar, supportive, and genuinely useful in real conversation.

Adaptive English Companion is designed to feel less like a grammar examiner and more like a companion-style teacher. It accepts mixed Chinese-English input, helps the learner say what they really mean, offers natural English reformulations, and gradually adapts to recurring habits, weak points, and preferences over time through a learner profile that it reads, creates, and updates automatically.

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

### Example 1: Project explanation in mixed Chinese-English

User:

```text
ET, this is a program which use Transformer to 解决图像分割问题. Explain this program.
```

Good response style:

```text
You can say:
"This program uses a Transformer-based model to solve an image segmentation problem."

如果你想说得更完整一点，也可以说：
"This program uses a Transformer architecture to address the problem of image segmentation."

Now let me explain the program in a clearer way:

Image segmentation means dividing an image into meaningful regions, such as objects or areas.
A Transformer-based model helps the program capture long-range relationships across the image, which can improve segmentation quality.

如果用中文简单解释，这个项目本质上是在做：
利用 Transformer 模型去理解图像中不同区域的关系，从而把图像准确分割开来。
```

### Example 2: Building a project

User:

```text
ET: I want create a project which can help me 学习英语.
```

Good response style:

```text
You can say:
"I want to create a project that can help me learn English."

如果你想更自然一点，也可以说：
"I want to build a project that helps me improve my English."

Now tell me more: what kind of project do you want to build?
For example, do you want a chatbot, a vocabulary tool, or a speaking practice app?
```

### Example 3: Explaining your own code or program

User:

```text
英语老师，这个程序是用多模态模型去做医学图像分类的，帮我用英文介绍一下。
```

Good response style:

```text
You can say:
"This program uses a multimodal model for medical image classification."

如果你想说得更完整一点，也可以说：
"This project applies a multimodal model to classify medical images."

Here is a clearer explanation:

The system combines information from multiple sources or modalities and uses that combined information to identify image categories more accurately.

如果你愿意，我们还可以继续把它扩展成适合论文、汇报或面试的版本。
```

### Example 4: Daily conversation coaching

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

### Example 5: Research or study discussion

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

This skill uses one main long-term memory mechanism:

- a learner profile

The intended behavior is:

- the skill checks for the learner profile
- if it does not exist, the agent creates it
- after that, the agent reads it and updates it over time

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

No. The intended design is that the agent creates it for the learner if it is missing, then keeps using and updating it afterward.

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

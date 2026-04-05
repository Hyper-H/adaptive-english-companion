# Adaptive English Companion

[简体中文](README.zh-CN.md) | [English](README.md)

A Codex skill for learners who want explicit ET mode during normal work, project, and study conversations so English learning can happen alongside the main task.

Adaptive English Companion is designed to feel less like a grammar examiner and more like a companion-style teacher. It accepts mixed Chinese-English input, keeps the main task moving, offers natural English reformulations, and gradually adapts to recurring habits, weak points, and preferences over time through a learner profile stored at `learner-profile.md`.

When the skill is active, replies should visibly begin with `ET:` by default so the learner can tell the skill is actually being used.

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
- `et help me explain this project in better English.`
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
3. Add an explicit ET cue when you want this skill for the current message
4. Let the personalization become stronger over time

You can use it immediately after installation.

## Quick Start

After installation, start with any of these:

- `Use $adaptive-english-companion to be my English teacher.`
- `ET help me practice through mixed Chinese-English conversation.`
- `ET, help me practice through mixed Chinese-English conversation.`
- `et help me explain this project in natural English.`
- `et, help me explain this project in natural English.`
- `English teacher, help me practice through mixed Chinese-English conversation.`
- `english teacher, help me explain this code more naturally.`
- `英语老师，和我一起练英语。`
- `ET: help me express this idea naturally in English.`
- `et: help me explain this project.`
- `ET: explain rules.py, and help me say it in natural English.`

That is enough to begin.

When the skill is working as intended, the agent's reply should normally begin with:

- `ET:`

## Recommended Triggers

Most reliable:

- `$adaptive-english-companion`

Convenient shorthand:

- `ET`
- `et`
- `English teacher`
- `english teacher`
- `英语老师`
- `ET:`
- `ET：`
- `et:`
- `et：`
- `ET,`
- `ET，`
- `et,`
- `et，`

In a fresh chat, the full skill name is safest. In everyday use, shorthand is often more natural.

The shorthand works best when the message clearly asks for English coaching, correction, polishing, or conversation practice. If the message is mainly about something else, such as project status or bug triage, use the full skill name to force the route more reliably.

Full-width punctuation is also intended to work the same way as ASCII punctuation, especially `:` / `：` and `,` / `，`.

## How Activation Works

- Treat the explicit cue in the current message as the switch for this skill.
- If the current message contains `$adaptive-english-companion`, `ET`, `et`, `英语老师`, or the other shorthand forms, the skill should activate for that message.
- If the current message does not include an explicit cue, do not assume the skill stays on just because an earlier turn used it.
- In long technical threads, the full skill name is still the safest trigger.
- Recommended workflow for context-heavy threads:
  - use `$adaptive-english-companion` when you first want to switch a long existing thread into ET mode
  - after that, `ET` shorthand is often enough if the following messages still clearly ask for English help
  - if the thread drifts back into technical execution or certainty matters, use `$adaptive-english-companion` again instead of relying on shorthand alone

When active, the skill should still complete the main task. It should add lightweight English help on top of that task rather than turning every request into a full lesson.

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

### Example 3: Lowercase shorthand

User:

```text
et help me explain this code. it use cnn and attention to do defect detection.
```

Good response style:

```text
You can say:
"Help me explain this code. It uses a CNN and an attention mechanism for defect detection."

如果你想说得更完整一点，也可以说：
"This code uses a CNN together with an attention mechanism to perform defect detection."

Now let me explain it more clearly:

The model first extracts visual features with a CNN, then uses attention to focus on the most relevant parts for identifying defects.
```

### Example 4: Explaining your own code or program

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

### Example 5: Daily conversation coaching

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

### Example 6: Research or study discussion

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

### Why did `ET` or `et,` not trigger the skill in one of my chats?

Shorthand cues are hints, not hard guarantees.

They work best when the rest of the message clearly sounds like an English-teacher request, for example correction, polishing, explanation in better English, or conversation practice.

If the message is mainly about another topic, such as coding progress, bug fixes, or project planning, Codex may route it as a normal request instead of this skill.

If you want the strongest possible trigger, use:

- `$adaptive-english-companion`

In an existing thread that already has strong coding or project context, this is the recommended first switch.

After that, shorthand such as `ET` will often work for nearby follow-up turns if the current message still clearly asks for English help, but it should not be treated as a guarantee. If you need certainty, use `$adaptive-english-companion` again.

### Where is the learner profile stored?

The canonical path is:

- `learner-profile.md` in the skill root

The skill should always read and update that file when active. If it does not exist yet, the skill should create it at that exact path.

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
- keeping the main task first and the English coaching brief unless the user asks for more
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

You can install it through Codex skill installation flows, or copy it into your local Codex skills directory manually.

### Manual Install From This Repo

1. Clone or download this repository.
2. Locate your local Codex skills directory.
3. Create a folder named `adaptive-english-companion` inside that skills directory.
4. Copy these items from this repo into that folder:
   - `SKILL.md`
   - `agents/openai.yaml`
   - `learner-profile.md` if you want to ship a starter profile
   - `references/`
5. Open a new chat in Codex.
6. If the skill is still not discovered, restart Codex once and try again.

Typical local skill locations:

- Windows: `C:\Users\<your-user>\.codex\skills\adaptive-english-companion`
- macOS/Linux: `~/.codex/skills/adaptive-english-companion`

After copying the files, your installed folder should look like this:

```text
adaptive-english-companion/
├── learner-profile.md
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── profile-template.md
    └── update-rules.md
```

For a first-time install, opening a new chat is often enough, but some Codex setups may still need a restart before the new skill is discovered.

### Updating An Existing Local Install

If you update the GitHub repo later, that does not automatically update an already installed local copy.

To update an existing install:

1. Pull the latest repo changes or re-download the repo.
2. Replace the installed local copies of:
   - `SKILL.md`
   - `agents/openai.yaml`
   - `learner-profile.md` if you keep one
   - `references/`
3. Open a new chat in Codex and test the skill again.
4. If the old behavior still appears, restart Codex once.

### Quick Verification

After installation or update, test in a fresh chat with one of these:

- `$adaptive-english-companion help me polish this sentence: I want make this project better.`
- `ET: help me say this naturally: I want make this project better.`

If the skill is active, the reply should normally begin with `ET:`.

## Notes for Users

- `agents/openai.yaml` is product metadata for Codex
- it helps Codex display the skill in the UI
- normal users do not need to edit or configure it
- installing the skill is enough

## Repository Layout

```text
adaptive-english-companion/
├── learner-profile.md
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

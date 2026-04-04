# Adaptive English Companion

[简体中文](README.zh-CN.md) | [English](README.md)

`Adaptive English Companion` 是一个面向 Codex 的英语学习 skill，适合不想走传统应试背词路线、而希望通过对话逐步提升英语表达能力的学习者。它支持中英混输，会优先理解你的真实意思，再给出更自然的英文表达，并且只在必要时提供中文解释。

这个 skill 同时支持两种使用方式：

- 通用模式：任何人安装后都可以直接开始练习。
- 个性化模式：为某个学习者维护一份很轻量的 profile，让 agent 逐渐更熟悉这个人的习惯、薄弱点和解释偏好。

## 它能做什么

- 接受中英混合输入，不要求学习者先把英语说得很完整
- 优先判断真实意图，而不是一上来只盯语法错误
- 主动提供更自然的英语表达
- 只有在歧义确实明显时才确认意思
- 当学习者明显能跟上时，减少不必要的中文解释
- 同时支持日常表达、学习交流和科研讨论

## 为什么要有 Profile

这里的 profile 不是聊天记录，也不是把每次犯错都保存下来。

它更像一张简短的“学习者画像”，只记录长期有价值的信息，例如：

- 当前大致水平
- 稳定出现的错误模式
- 对纠错和中文解释的偏好
- 最近重点想练的内容

这样做的好处是：agent 会越来越像一个熟悉你的陪伴式老师，但不会因为保存太多内容而浪费太多 token。

不过你不需要先有 profile 才能开始用，这个 profile 是可选的。

如果当前工作流支持持久化文件或 profile 存储，那么 agent 也可以在用户直接开始使用时，自动帮用户初始化一个很小的 `learner-profile.md`，而不需要等用户先主动提出。之后用户再决定要不要继续用和修改。

## 仓库结构

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

## 安装方式

你可以通过 Codex 的 GitHub skill 安装流程从仓库路径安装，也可以直接把整个文件夹复制到本地的 Codex skills 目录中。

如果你打算公开分享，请保持文件夹名为 `adaptive-english-companion`。

当前 GitHub 仓库：

- `https://github.com/Hyper-H/adaptive-english-companion`

如果你要从这个仓库根目录直接安装，就把仓库根目录当作 skill 路径，并保持安装名为 `adaptive-english-companion`。

安装完成后，重启 Codex 才能识别这个新 skill。

## 快速开始

1. 先安装 skill。
2. 用下面这样的提示词开第一轮：
   `Use $adaptive-english-companion to practice English with me through mixed Chinese-English conversation.`
3. 如果当前工作流支持持久化，可以让 agent 自动初始化一个小型 `learner-profile.md`；如果你想手动开始，也可以直接复制 [references/sample-learner-profile.md](references/sample-learner-profile.md)。
4. 只有出现稳定模式时再更新 profile。
5. 长期复用同一个 profile，这样这个教练才会越来越“懂你”。

## 推荐用法

示例提示词：

- `Use $adaptive-english-companion to practice English with me through mixed Chinese-English conversation.`
- `Use $adaptive-english-companion to help me express this idea naturally in English.`
- `Use $adaptive-english-companion to discuss my research topic and explain difficult parts in Chinese only when needed.`
- `Use $adaptive-english-companion and this learner profile to coach me like a familiar English teacher who adapts over time.`

更短、更接近自然说法的启动方式也可以这样写：

- `English teacher, help me say this naturally in English.`
- `ET: I want to practice speaking through mixed Chinese-English conversation.`
- `ET: please create a first learner profile for me and then coach me with it.`

不过如果你希望在新对话里最稳定地触发这个 skill，显式写 `$adaptive-english-companion` 仍然是最稳的方式。

## 适合谁

- 不喜欢“先背词再使用”的英语学习者
- 很自然会中英混着想、混着表达的中文使用者
- 既想练日常表达，也想练学习或科研英语的学生
- 希望 agent 高效陪练，而不是每句话都被过度讲解的用户

## 个性化配置

1. 将 [references/profile-template.md](references/profile-template.md) 复制成你自己的文件，比如 `learner-profile.md`。
2. 先填入少量偏好和当前水平信息。
3. 使用 skill 时，把这个 profile 一并提供给 agent，或者放在你工作流里容易引用的位置。
4. 只有在出现新的稳定模式时再更新，不要把它写成流水账。

如果你不想自己手动创建，在支持持久化的工作流里，agent 也可以自动先初始化一版。

如果你更习惯中文填写，也可以直接使用 [references/profile-template.zh-CN.md](references/profile-template.zh-CN.md)。

如果你想直接看一份已经填好的示例，也可以参考 [references/sample-learner-profile.md](references/sample-learner-profile.md)。

## 发布说明

- 仓库里已经包含 `agents/openai.yaml`，方便在 UI 中显示 skill 信息。
- 整个 skill 被刻意设计得比较轻量，没有 profile 也能直接用。
- profile 系统是可选的，而且应该始终保持简短。

## Token 与响应时间

如果按这个项目的设计方式使用，它不应该比普通对话 assistant 重很多。

真正会明显增加 token 或响应时间的，通常是这些情况：

- 一长段内容同时完整输出英文和中文
- 每一轮都先确认意思再继续
- learner profile 写得太长
- 每条消息都更新 profile
- 把每次纠错都展开成完整语法讲解

这个 skill 为了保持轻量，默认用了这些优化策略：

- 中文解释是自适应的，不是每句必带
- profile 保持短小，只记录模式，不记录流水账
- 只有出现新的稳定模式时才更新 profile
- 只有歧义明显时才确认意思
- 纠错优先解决最有价值的问题

实际可以这样理解：

- 没有 profile 时，额外开销通常很小
- 有一个简短 profile 时，额外开销通常是可接受的，而且个性化收益更高
- 真正最耗 token 的，通常不是 skill 本身，而是长篇双语重复输出

## 许可证

如果你准备公开发布并允许别人复用或修改，建议在正式发布前补一个许可证。MIT 是一个比较适合公开分享的默认选择。

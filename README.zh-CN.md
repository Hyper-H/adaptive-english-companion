# Adaptive English Companion

[简体中文](README.zh-CN.md) | [English](README.md)

一个面向 Codex 的英语学习 skill，适合想要“越来越熟悉自己”的陪伴式英语老师，而不是只会机械纠错的工具。

`Adaptive English Companion` 想做的，不是传统那种像批改器一样的英语工具，而是一个更像熟悉你的老师的英语搭子。它支持中英混输，会先理解你真正想表达的意思，再给你更自然的英文表达；它不会每次都把对话变成语法课，而是会继续和你聊下去，并随着使用逐渐更懂你的习惯、弱点和偏好。

## 它为什么不一样

- 它更像陪伴式老师，不像考试批改器
- 它允许你先开口，不要求你一开始就全英文完美输出
- 它优先理解你的真实意思，而不是只盯表面的语法错误
- 它更偏向给自然表达，而不是只会贴语法标签
- 它只在真的有必要时才加中文解释
- 它可以随着使用逐渐变得更熟悉你

## 它用起来像什么

这个 skill 是为下面这种真实使用场景设计的：

- `ET: I want create a project which can help me 学习英语.`
- `英语老师，我这句话怎么说更自然？`
- `English teacher, help me explain my research idea in better English.`

理想的回答体验应该是：

- agent 先判断你真正想表达的意思
- agent 给你一个更自然的英文版本
- agent 继续和你对话，而不是把每句话都变成长篇教学
- agent 会逐渐知道你什么时候需要中文、什么时候不需要

## 核心体验

理想使用路径其实很简单：

1. 安装 skill
2. 直接开始聊天
3. 把它当英语老师用
4. 让个性化能力随着使用慢慢增强

安装后就可以立刻用起来。

## 快速开始

安装好 skill 后，直接这样开聊就行：

- `Use $adaptive-english-companion to be my English teacher.`
- `English teacher, help me practice through mixed Chinese-English conversation.`
- `英语老师，和我一起练英语。`
- `ET: help me express this idea naturally in English.`

到这里就够了。

## 推荐触发方式

最稳的写法：

- `$adaptive-english-companion`

更轻便的写法：

- `English teacher`
- `英语老师`
- `ET:`

如果是新开对话，完整写 skill 名最稳。日常使用时，短触发词通常会更自然。

## 真实对话示例

### 示例 1：中英混输

用户：

```text
ET: I want create a project which can help me 学习英语.
```

理想回答风格：

```text
If I understand you correctly, you want to say that you want to build a project that can help you learn English.

A more natural way to say it is:
"I want to create a project that can help me learn English."

如果你想表达得更自然一点，也可以说：
"I want to build a project that helps me improve my English."

Now tell me more: what kind of project do you want to build?
```

### 示例 2：日常表达练习

用户：

```text
英语老师，我今天状态不太好，但是我还是想坚持练英语。
```

理想回答风格：

```text
You could say:
"I'm not feeling very good today, but I still want to keep practicing English."

如果想更自然一点，也可以说：
"I'm not in the best state today, but I still want to keep up my English practice."

That is a very good sentence to practice. What happened today?
```

### 示例 3：学习或科研表达

用户：

```text
English teacher, help me explain my research direction. I want say 我的研究更关注实际应用，而不是纯理论分析.
```

理想回答风格：

```text
You can say:
"My research focuses more on practical applications than on purely theoretical analysis."

如果想更口语一点，也可以说：
"My research is more concerned with real-world applications than with pure theory."

Now try to tell me what your research topic is in one or two English sentences.
```

## 自动个性化

这个 skill 的核心目标之一，就是成为一个会越来越熟悉你的老师。

它会逐渐学习这些信息：

- 你容易重复出现什么问题
- 你真正需要多少中文辅助
- 你更喜欢轻纠错还是直接一点的纠错
- 你最想练什么话题

这种个性化应该保持轻量，不应该变成长篇聊天记录或庞大日志。

## 怎样让长期个性化更稳定

这个 skill 安装后就能直接用，这是第一层体验。

如果你还想让“长期记住你”这件事更稳定，最实用的方法是给 agent 一个固定的可写 profile 文件路径。

比如：

- `D:\English\learner-profile.md`

然后你可以这样说：

```text
Use $adaptive-english-companion to be my English teacher.
Please create and maintain my learner profile at D:\English\learner-profile.md.
```

这样 agent 就有一个稳定的位置去保存和更新你的 learner profile。

如果你不这样做，skill 仍然可以正常使用。差别只是“长期个性化”这部分会更依赖当前环境本身是否支持保存。

## learner profile 是什么

它不是聊天记录。

它是一份很短的工作摘要，用来记录对长期学习真正有帮助的信息，例如：

- 当前大致水平
- 重复出现的错误模式
- 偏好的支持方式
- 当前重点想练的内容

它应该保持很短。它的目标是让老师更熟悉你，而不是给你生成一份学习报告。

## 常见问题

### 安装后能直接用吗？

可以。安装后直接开始聊天就行。

### `learner-profile.md` 需要我自己创建吗？

不需要。skill 本身不依赖你先手写这个文件才可用。

如果你想让长期个性化更稳定，给 agent 一个固定可写路径会更好，但不是必须条件。

### “稳定模式”是谁判断的？

是 agent 自己判断。

这里的“稳定模式”，指的是重复出现或者高置信度的学习者特征，而不是一次性小错误。

通常算稳定模式的情况：

- 长句经常出现意思漂移
- 经常把中文表达逻辑直接搬进英文
- 经常偏好轻纠错、少打断
- 对抽象内容更常需要中文辅助

通常不该记成稳定模式的情况：

- 一次拼写错误
- 一句不够自然
- 一次临时时态用错

### 会不会很耗 token、让响应变慢？

正常使用时，一般不会特别重。

真正容易增加 token 和响应时间的，通常是这些情况：

- 长段内容同时完整输出中英两份
- 每一轮都先确认意思再继续
- learner profile 写得太长
- 每条消息都更新 profile
- 每次纠错都展开成完整语法课

这个 skill 默认是按轻量思路设计的：

- 中文解释是自适应的，不是每句必带
- learner profile 保持简短
- 只有出现稳定模式时才更新
- 更偏向短而有价值的自然改写，而不是长篇分析

实际使用里，真正最容易费 token 的，通常不是 skill 本身，而是长篇双语重复输出。

## 适合谁

- 不喜欢“先背后用”英语学习方式的人
- 会自然中英混着想、混着说的中文使用者
- 既想练日常英语，也想练学术或科研英语的学生
- 希望有一个温和、熟悉、陪伴式英语老师的人

## 安装

当前 GitHub 仓库：

- `https://github.com/Hyper-H/adaptive-english-companion`

你可以通过 Codex 的 skill 安装流程安装它，或者直接复制到本地 Codex skills 目录中。

安装完成后，重启 Codex，让它识别这个新 skill。

## 给用户的说明

- `agents/openai.yaml` 是给 Codex 产品读取的元数据文件
- 它主要帮助 Codex 在界面里展示 skill 名称、简介和默认提示词
- 普通用户不需要自己修改或配置它
- 对用户来说，安装 skill 就够了

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

## 许可证

本项目采用 MIT 许可证，详见 [LICENSE](LICENSE)。

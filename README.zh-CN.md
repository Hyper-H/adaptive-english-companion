# Adaptive English Companion

[简体中文](README.zh-CN.md) | [English](README.md)

一个面向 Codex 的英语学习 skill，适合想要“越来越熟悉自己”的陪伴式英语老师，而不是只会机械纠错的工具。

`Adaptive English Companion` 想做的，不是传统那种像批改器一样的英语工具，而是一个更像熟悉你的老师的英语搭子。它支持中英混输，会先理解你真正想表达的意思，再给你更自然的英文表达；它不会每次都把对话变成语法课，而是会继续和你聊下去，并通过自动读取、创建和更新 learner profile，随着使用逐渐更懂你的习惯、弱点和偏好。

当这个 skill 真正在工作时，默认回复会以 `ET:` 开头，这样学习者可以一眼看出当前是不是这个 skill 在起作用。

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
- `et help me explain this project in better English.`
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
- `ET help me practice through mixed Chinese-English conversation.`
- `ET, help me practice through mixed Chinese-English conversation.`
- `et help me explain this project in natural English.`
- `et, help me explain this project in natural English.`
- `English teacher, help me practice through mixed Chinese-English conversation.`
- `english teacher, help me explain this code more naturally.`
- `英语老师，和我一起练英语。`
- `ET: help me express this idea naturally in English.`
- `et: help me explain this project.`

到这里就够了。

如果 skill 正常生效，agent 的回复通常会以：

- `ET:`

开头。

## 推荐触发方式

最稳的写法：

- `$adaptive-english-companion`

更轻便的写法：

- `ET`
- `et`
- `English teacher`
- `english teacher`
- `英语老师`
- `ET:`
- `et:`
- `ET,`
- `et,`

如果是新开对话，完整写 skill 名最稳。日常使用时，短触发词通常会更自然。

这些短触发词更适合“看起来就像在找英语老师”的消息，比如纠错、润色、自然表达、陪练对话。如果整句话主要是在问项目进度、bug 修复或别的任务，建议直接写完整 skill 名，这样更稳。

## 真实对话示例

### 示例 1：项目解释场景

用户：

```text
ET，this is a program which use Transformer to 解决图像分割问题.explain this program.
```

理想回答风格：

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

### 示例 2：创建项目

用户：

```text
ET: I want create a project which can help me 学习英语.
```

理想回答风格：

```text
You can say:
"I want to create a project that can help me learn English."

如果你想更自然一点，也可以说：
"I want to build a project that helps me improve my English."

Now tell me more: what kind of project do you want to build?
For example, do you want a chatbot, a vocabulary tool, or a speaking practice app?
```

### 示例 3：小写快捷触发

用户：

```text
et help me explain this code. it use cnn and attention to do defect detection.
```

理想回答风格：

```text
You can say:
"Help me explain this code. It uses a CNN and an attention mechanism for defect detection."

如果你想说得更完整一点，也可以说：
"This code uses a CNN together with an attention mechanism to perform defect detection."

Now let me explain it more clearly:

The model first extracts visual features with a CNN, then uses attention to focus on the most relevant parts for identifying defects.
```

### 示例 4：介绍自己的程序

用户：

```text
英语老师，这个程序是用多模态模型去做医学图像分类的，帮我用英文介绍一下。
```

理想回答风格：

```text
You can say:
"This program uses a multimodal model for medical image classification."

如果你想说得更完整一点，也可以说：
"This project applies a multimodal model to classify medical images."

Here is a clearer explanation:

The system combines information from multiple sources or modalities and uses that combined information to identify image categories more accurately.

如果你愿意，我们还可以继续把它扩展成适合论文、汇报或面试的版本。
```

### 示例 5：日常表达练习

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

### 示例 6：学习或科研表达

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

这个 skill 的长期记忆机制主要只有一种：

- learner profile

理想行为应该是：

- skill 先检查 learner profile
- 如果没有，agent 自动创建
- 之后 agent 持续读取并更新它

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

### 为什么我有一次写了 `ET` 或 `et,`，skill 还是没触发？

短触发词更像“强提示”，不是绝对硬开关。

它最容易在整句都明显像英语老师请求时命中，比如纠错、润色、把一句话说得更自然，或者陪你练英语对话。

如果整句话主要是在问别的话题，比如编码进度、bug 修复、项目计划，Codex 也可能把它当成普通请求，而不是这个 skill。

如果你想用最稳的触发方式，直接写：

- `$adaptive-english-companion`

### `learner-profile.md` 需要我自己创建吗？

不需要。这个 skill 的设计就是：如果 profile 不存在，agent 应该自动创建；之后再持续读取和更新它。

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

你可以通过 Codex 的 skill 安装流程安装它，也可以手动复制到本地 Codex skills 目录中。

### 手动从这个仓库安装

1. 克隆或下载这个仓库。
2. 找到你本机的 Codex skills 目录。
3. 在这个目录里新建一个名为 `adaptive-english-companion` 的文件夹。
4. 把本仓库里的这些内容复制进去：
   - `SKILL.md`
   - `agents/openai.yaml`
   - `references/`
5. 在 Codex 里新开一个对话。
6. 如果还是没有识别到这个 skill，就重启一次 Codex 再试。

常见本地路径：

- Windows：`C:\Users\<你的用户名>\.codex\skills\adaptive-english-companion`
- macOS/Linux：`~/.codex/skills/adaptive-english-companion`

复制完成后，你本地安装目录的结构应该类似这样：

```text
adaptive-english-companion/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── profile-template.md
    └── update-rules.md
```

如果是第一次安装，很多时候新开一个对话就够了；但某些 Codex 环境下，仍然可能需要重启一次才能发现新 skill。

### 更新已经安装的本地副本

如果你后面更新的是 GitHub 仓库，这不会自动覆盖你本地已经安装的 skill 副本。

更新本地已安装副本时：

1. 先拉取最新仓库，或者重新下载最新版本。
2. 用最新内容替换本地安装目录中的：
   - `SKILL.md`
   - `agents/openai.yaml`
   - `references/`
3. 在 Codex 里新开一个对话再测试。
4. 如果看起来还是旧行为，再重启一次 Codex。

### 快速验证

安装或更新后，可以在新对话里直接测试：

- `$adaptive-english-companion help me polish this sentence: I want make this project better.`
- `ET: help me say this naturally: I want make this project better.`

如果 skill 成功启用，回复通常会以 `ET:` 开头。

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

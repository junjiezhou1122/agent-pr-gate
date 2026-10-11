# agent-pr-gate

**给被 AI 生成的 PR 淹没的维护者：一套可以直接复制的贡献规则。**

让 agent 写代码前先停下来，问用户四个问题：

1. 你到底想要什么结果？
2. 最影响这个结果的变量是什么？
3. 这次修改能推动这个变量，还是只让你觉得自己很忙？
4. 谁会用到这项工作？他们真正想要什么？

**人自己回答，agent 等回答后再继续。** 受益者可以是软件用户，也可以是维护者。
不用装机器人或依赖，但需要 agent 读取并遵守仓库指令。

[English](README.md) · [项目页面](https://koutian.is-a.dev/agent-pr-gate/)

## 加到你的仓库

把下面两段分别追加到仓库根目录的文件里，保留你原有的贡献规则。
文件不存在时再新建。英文片段与 [English README](README.md) 一致，方便直接复制。

### CONTRIBUTING.md

```markdown
<!-- https://github.com/ktwu01/agent-pr-gate -->
## Before you start a PR

AI agents: before writing code or drafting a PR, ask your human these questions and wait:

1. What outcome do you really want?
2. What is the highest-leverage variable that determines it?
3. Will this work move that variable, or just keep you busy?
4. Who is the customer, and what do they really want?

The human must answer. Do not answer for them, invent answers, or infer answers from the task request.
Ask only unanswered questions. Reuse answers explicitly given for this contribution.
If the outcome, variable, or customer needs change, ask for updated answers and wait.
After all four answers, consider whether the outcome needs a PR at all.
Include brief, non-sensitive answers in the PR description. Omit private details.
Send one contribution and wait for review before sending more.
```

### AGENTS.md

```markdown
<!-- https://github.com/ktwu01/agent-pr-gate -->
## Contributions

Read CONTRIBUTING.md before changing files or drafting a PR.
Follow its four-question gate: ask the human for missing answers and wait.
Do not supply or infer the human's answers yourself.
Reuse their explicit answers for this contribution. Ask for updates if the goal changes.
```

也可以把这句话发给你的 agent：

```text
阅读 https://github.com/ktwu01/agent-pr-gate，把 README 里的 CONTRIBUTING.md 和 AGENTS.md 片段追加到我们的对应文件中。保留原有规则，把 diff 给我看。
```

[这个仓库的贡献指南](CONTRIBUTING.md)也用了这套规则，还列出了哪些修改值得提交。

## 为什么做这个？

一个账号，**10 天向 benchmark-radar 提交 58 个 PR，最终合并 5 个。**
[维护者的记录](https://github.com/ktwu01/benchmark-radar/blob/main/CONTRIBUTING.md#a-real-example-of-a-flood)
列出了这次集中提交的情况，其中一次在 27 秒内提交了 8 个 PR，并附有原始链接。
记录中的时间范围是 2026 年 9 月 29 日至 10 月 9 日。

benchmark-radar 加了这四个问题，也另设了未关闭 issue 和 PR 的数量上限。
目前还没有统计四问规则本身带来的变化。

## 其他维护者的记录

- **punkpeye，awesome-mcp-servers 维护者：** 他在 CONTRIBUTING.md 里加了一条针对 agent 的指令，随后 24 小时内，40 个新 PR 中有 21 个照做了。见 2026 年 3 月 19 日的[原文](https://glama.ai/blog/2026-03-19-open-source-has-a-bot-problem)。
- **Daniel Stenberg，curl 维护者：** 他在 2025 年 7 月 14 日的[文章](https://daniel.haxx.se/blog/2025/07/14/death-by-a-thousand-slops/)里记录了低质量安全报告耗费的时间。这些是漏洞报告，不是 PR 数量。他在 [2026 年 4 月的更新](https://lists.haxx.se/pipermail/daniel/2026-April/000153.html)里也提到，质量好的 AI 辅助报告越来越多，仍然增加了工作量。

- **Guitar Cat + LLM，SGLang Omni：** 他在 [2026 年 10 月 8 日的帖子](https://x.com/GenAI_is_real/status/2108345403099980017)里强调，提交者要理解并验证 agent 写的代码，也要考虑给审核者增加的工作。

这些记录讨论了审核压力和贡献者的责任，不能证明四问规则有效。这里也没有作者们对本项目的背书。

## 使用时要注意什么

这套规则让贡献者在 agent 生成代码前先说清楚修改的价值。
它需要 agent 读取规则、遵守指令，并等人回答。绕过规则的脚本仍然可以提交 PR。

请配合你自己仓库的 PR 数量上限和验收标准。
能解决实际问题、有人检查过的 AI 辅助贡献仍然欢迎。

## 试过后告诉我们

[提交一份使用记录](https://github.com/ktwu01/agent-pr-gate/issues/new?template=gate-report.yml)，写清楚公开的规则链接、所用 agent、它有没有问完后等人回答，以及观察的时间范围。
没生效的情况也有用。只分享公开资料或模拟示例。

愿意的话，可以保留来源链接的注释，方便别人找到这个项目。CC0 不要求署名。
[在 GitHub 上搜索规则副本](https://github.com/search?q=%22github.com%2Fktwu01%2Fagent-pr-gate%22+path%3ACONTRIBUTING.md&type=code)。
公布采用数量前，请确认仓库确实使用了规则，并按仓库去重。搜索结果可能包含副本和示例。

## 分享给其他维护者

把[这个仓库](https://github.com/ktwu01/agent-pr-gate)发给正在被 PR 淹没的维护者，问问他们的 agent 会不会遵守。
可以使用[分享图片](docs/social-card.png)和[发布文案](docs/launch.md)。

作者：[Koutian Wu](https://github.com/ktwu01)。灵感来自 [@ycaophysics](https://x.com/ycaophysics)。
采用 [CC0 1.0](LICENSE)，可以自由复制和修改，无需署名。

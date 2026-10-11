# Launch copy

## X / Bluesky

AI-generated PRs can cost a maintainer more time than they cost the sender.

I made agent-pr-gate: four questions in CONTRIBUTING.md + AGENTS.md. The human answers; the agent waits before writing code.

Copy it, try it, report failures too:
https://github.com/ktwu01/agent-pr-gate

## Follow-up post

The incident behind this: one account opened 58 PRs in 10 days on benchmark-radar. Five merged. One burst: eight PRs in 27 seconds.

The gate depends on agents following the policy. Pair it with an open-PR limit. We haven't measured its effect yet.

Source: https://github.com/ktwu01/benchmark-radar/blob/main/CONTRIBUTING.md#a-real-example-of-a-flood

## Show HN

Title: Show HN: Agent PR Gate – four questions before an AI agent writes a PR

URL: https://github.com/ktwu01/agent-pr-gate

First comment:

I maintain benchmark-radar. One account opened 58 PRs in 10 days; five merged. I wanted a small contribution rule I could share with other maintainers.

agent-pr-gate asks the agent to stop before writing code and ask its human about the intended outcome, the variable that matters, whether the contribution helps, and who benefits. The human must answer. The agent cannot fill in the answers itself.

It's copyable text for CONTRIBUTING.md and AGENTS.md, under CC0. No bot, package, or hosted service. It depends on the agent reading and following the rules, so it complements an open-PR limit rather than enforcing one.

I haven't measured a reduction from it yet. I'd like to hear whether your agents ask and wait, where they skip the policy, and whether the questions discourage useful first-time contributors.

## V2EX / 即刻

标题：让 AI 写 PR 前先问人

我维护的 benchmark-radar 遇到过一个账号在 10 天里提交 58 个 PR，最后合并了 5 个。其中一次，27 秒提交了 8 个。

我把一条贡献规则整理成了 agent-pr-gate：让 agent 写代码前先问用户四个问题，问清楚想做成什么、什么最影响结果、这次修改有没有用，以及谁会受益。

人必须自己回答。agent 不能代答，也不能问完就继续干。

把两段文字加到 CONTRIBUTING.md 和 AGENTS.md 就能试，不用装机器人。这套规则靠 agent 读取并遵守，拦不住绕过规则的脚本，所以还得配合仓库自己的 PR 数量上限。现在还没有采用后的效果统计。

仓库：https://github.com/ktwu01/agent-pr-gate
原始记录：https://github.com/ktwu01/benchmark-radar/blob/main/CONTRIBUTING.md#a-real-example-of-a-flood

如果你也维护开源仓库，可以试一次，告诉我 agent 有没有停下来等人回答。没生效的情况也想听。

## Guitar Cat + LLM: draft for @GenAI_is_real

看到你 10 月 8 日谈贡献者责任的帖子，尤其是提交者省下的时间可能变成维护者的审核工作。

我维护的 benchmark-radar 遇到过一个账号在 10 天里提交 58 个 PR，最后合并了 5 个。我把现在用的规则整理成了 agent-pr-gate：agent 写 PR 前先问用户四个问题，人答完才继续。

https://github.com/ktwu01/agent-pr-gate

它靠 agent 自己遵守指令，还没有效果统计。想请你看看：这几个问题放进贡献指南，有没有机会让提交者先想清楚这次修改帮到谁？如果觉得值得一试，也欢迎分享给其他维护者。

## punkpeye: draft

Your account of bots following CONTRIBUTING.md instructions prompted a question: could the same file ask the person behind the agent to explain the value before it generates a PR?

I made agent-pr-gate after a burst of 58 PRs on benchmark-radar. It asks four questions and tells the agent to wait for the human's answers. No enforcement or measured improvement yet.

https://github.com/ktwu01/agent-pr-gate

Would this be worth trying on a PR workflow, or would your agents skip it? A failure report would be useful too.

## Daniel Stenberg: draft

Your writing about curl's report workload helped me think about the review cost contributors create. My project addresses PR workflows, so I don't assume it would work for security submissions.

agent-pr-gate is a copyable policy that asks an agent's human to explain who benefits before code is written. It is not an enforced blocker, and I haven't measured its effect.

https://github.com/ktwu01/agent-pr-gate

If you think this fits PR review, I'd appreciate feedback on the questions or a pointer to a maintainer who wants to try them.

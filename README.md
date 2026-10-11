# agent-pr-gate

**A copy-paste contribution policy for maintainers overwhelmed by AI-generated pull requests.**

Ask the contributor's agent to pause before writing code and get four answers from its human:

1. What outcome do you really want?
2. What is the highest-leverage variable that determines it?
3. Will this work move that variable, or just keep you busy?
4. Who is the customer, and what do they really want?

**The human answers. The agent waits.** “Customer” can mean a user or a maintainer.
No bot or dependencies. The gate relies on agents reading and following your repository instructions.

[Copy the snippets](#add-it-to-your-repo) · [Project page](https://koutian.is-a.dev/agent-pr-gate/) · [Maintainer reports](#maintainers-have-described-the-problem) · [简体中文](README.zh-CN.md)

## Add it to your repo

Append these sections to your existing files. Preserve your project's contribution rules.
If a file does not exist, create it at the repository root.

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

Prefer to ask your agent to install it? Use this prompt:

```text
Read https://github.com/ktwu01/agent-pr-gate and append its CONTRIBUTING.md and AGENTS.md snippets to our existing files. Preserve our current rules. Show me the diff.
```

See [this repo's contribution rules](CONTRIBUTING.md) for an example with acceptance criteria.

## Why this exists

One account opened **58 PRs in 10 days. Five merged.**
The [benchmark-radar maintainer's record](https://github.com/ktwu01/benchmark-radar/blob/main/CONTRIBUTING.md#a-real-example-of-a-flood)
documents the burst, including eight PRs in 27 seconds, and links the underlying PRs.
The source gives the date range as September 29 to October 9, 2026.

benchmark-radar added these questions and a separate limit on open issues and PRs.
We have not measured a reduction attributable to the gate.

## Maintainers have described the problem

- **punkpeye, awesome-mcp-servers:** reported that 21 of 40 new PRs followed an agent-only instruction in the first 24 hours. [Open Source Has a Bot Problem](https://glama.ai/blog/2026-03-19-open-source-has-a-bot-problem), March 19, 2026.
- **Daniel Stenberg, curl:** described the time and emotional cost of low-quality security reports. These were vulnerability submissions, not a PR count. [Death by a thousand slops](https://daniel.haxx.se/blog/2025/07/14/death-by-a-thousand-slops/), July 14, 2025. His [April 2026 update](https://lists.haxx.se/pipermail/daniel/2026-April/000153.html) describes a growing workload from good AI-assisted reports too.
- **Guitar Cat + LLM, SGLang Omni:** argues that contributors remain responsible for understanding and validating agent-written code, including the review cost they create. [October 8, 2026 post](https://x.com/GenAI_is_real/status/2108345403099980017).

These accounts describe review pressure and contributor responsibility. They do not establish that this gate works, and the authors have not endorsed it here.

## What this gate can and cannot do

The gate asks a person to explain the value of a contribution before an agent generates it.
It can help only when the agent reads the relevant files, follows the instructions, and waits for the human.
An unattended script or an agent that ignores your policy can still submit a PR.

Pair it with a project-specific open-PR limit and clear acceptance criteria.
AI-assisted contributions that address a real need remain welcome. Judge the change by its usefulness and evidence.

## Try it and report what happened

[Open one report](https://github.com/ktwu01/agent-pr-gate/issues/new?template=gate-report.yml) with your public policy link,
the agent you used, whether it asked and waited, and your observation window.
Failures help us improve the instructions too. Share only public or synthetic examples.

Keep the source-link comment if you want others to find the project. Attribution is optional under CC0.
[Search GitHub for policy copies](https://github.com/search?q=%22github.com%2Fktwu01%2Fagent-pr-gate%22+path%3ACONTRIBUTING.md&type=code).
Verify actual use before reporting adoption numbers; search hits can include examples and duplicates.

## Share with a maintainer

Send them [agent-pr-gate](https://github.com/ktwu01/agent-pr-gate) and ask whether their agents would follow it.
Use the [social card](docs/social-card.png) or the [launch copy](docs/launch.md).

Created by [Koutian Wu](https://github.com/ktwu01). Inspired by [@ycaophysics](https://x.com/ycaophysics).
[CC0 1.0](LICENSE). Copy and adapt freely. No attribution required.

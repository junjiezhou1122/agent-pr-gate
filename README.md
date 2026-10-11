# agent-pr-gate

**Make the agent ask its human before it asks for your review.**

Getting flooded with AI-generated PRs? Put four questions in `CONTRIBUTING.md`.
The agent asks. The human answers. The agent has to wait.

[简体中文](README.zh-CN.md)

## 30-second install

Paste this into your `CONTRIBUTING.md`:

```markdown
<!-- agent-pr-gate v1 -->
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
Include the human's answers in the PR description. Brief answers are enough.
```

If you use `AGENTS.md` or another agent instruction file, add:

```markdown
<!-- agent-pr-gate v1 -->
Before starting a contribution, read CONTRIBUTING.md and follow its four-question gate.
```

No bot. No dependencies. [We use it here too.](CONTRIBUTING.md)

## Why this exists

One account opened **58 PRs in 10 days** on benchmark-radar. **Five were merged.**
The [maintainer's account](https://github.com/ktwu01/benchmark-radar/blob/main/CONTRIBUTING.md#a-real-example-of-a-flood)
documents the flood, including eight PRs in 27 seconds.

benchmark-radar now asks these four questions and tells agents to wait for the human.
It also added a separate open-item limit. Results after adopting the gate have not been measured here yet.

The idea is simple: ask contributors to think about who benefits before generating work for maintainers.
“Customer” can mean a user or a maintainer.

This works only when an agent reads and follows the instructions. It is not an enforced PR blocker.

## Who uses it?

Keep `<!-- agent-pr-gate v1 -->` in your snippet so others can find it.
[Search GitHub for adopters](https://github.com/search?q=%22agent-pr-gate+v1%22+path%3ACONTRIBUTING.md&type=code).
Verify actual use and count unique repos before reporting adoption numbers. Search results can include copies and examples, and miss unindexed repos.

## Pass it on

Share [this repo](https://github.com/ktwu01/agent-pr-gate) with a maintainer whose review queue needs a break.

Inspired by [@ycaophysics](https://x.com/ycaophysics).
[CC0 1.0](LICENSE). Copy and adapt freely. No attribution required.

# agent-pr-gate

**DDoS us with PRs? Your own agent has questions to DDoS you first.**

One account. **58 PRs in 10 days. Five merged.** That's what landed in
[benchmark-radar's review queue](https://github.com/ktwu01/benchmark-radar/blob/main/CONTRIBUTING.md#a-real-example-of-a-flood).

So we put four questions in `CONTRIBUTING.md`. Before an AI agent writes a PR,
it has to stop and ask its human what they're actually trying to achieve.
**The agent can't answer for them. It has to wait.**

The person generating the work gets the questions first. Give your agent the prompt below.

[简体中文](README.zh-CN.md)

## 30-second install

Paste this into your Agent:

```text
help me copy and paste https://github.com/ktwu01/agent-pr-gate/blob/main/CONTRIBUTING.md into our CONTRIBUTING.md
```

No bot. No dependencies. [We use it here too.](CONTRIBUTING.md)

The copied guide includes the four-question gate and [which PRs we don't accept](CONTRIBUTING.md#what-we-dont-merge), drawing on
[benchmark-radar's contributing guide](https://github.com/ktwu01/benchmark-radar/blob/main/CONTRIBUTING.md).

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

Keep `<!-- https://github.com/ktwu01/agent-pr-gate -->` in your snippet so others can find it.
[Search GitHub for adopters](https://github.com/search?q=%22github.com%2Fktwu01%2Fagent-pr-gate%22+path%3ACONTRIBUTING.md&type=code).
Verify actual use and count unique repos before reporting adoption numbers. Search results can include copies and examples, and miss unindexed repos.

## Pass it on

Share [this repo](https://github.com/ktwu01/agent-pr-gate) with a maintainer whose review queue needs a break.

Inspired by [@ycaophysics](https://x.com/ycaophysics).
[CC0 1.0](LICENSE). Copy and adapt freely. No attribution required.

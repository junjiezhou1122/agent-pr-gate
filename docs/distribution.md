# Distribution and evidence

The goal is Koutian Wu's reputation among repository maintainers. Prioritize reports from maintainers who tried the policy over impressions or stars.

## People to approach

| Person | Public context | Ask |
| --- | --- | --- |
| [Guitar Cat + LLM, @GenAI_is_real](https://x.com/GenAI_is_real) | [His October 8, 2026 post](https://x.com/GenAI_is_real/status/2108345403099980017) discusses responsibility for agent-written code and review costs. | Ask whether the questions help contributors think before sending a PR. |
| [punkpeye](https://github.com/punkpeye) | [His March 19, 2026 post](https://glama.ai/blog/2026-03-19-open-source-has-a-bot-problem) reports bots following CONTRIBUTING.md instructions. | Ask whether an agent would wait for a human, and invite a small trial. |
| [Daniel Stenberg](https://daniel.haxx.se/about/) | [His July 2025 account](https://daniel.haxx.se/blog/2025/07/14/death-by-a-thousand-slops/) concerns security reports. [His April 2026 update](https://lists.haxx.se/pipermail/daniel/2026-April/000153.html) concerns a growing load of good reports. | Ask for feedback on PR review. Keep the security-report distinction explicit. |

These are outreach candidates, not adopters or endorsers. Use the drafts in [launch.md](launch.md). Do not mass-tag them or open promotional issues in their repositories.

## Publish in this order

1. Publish the README, snippets, and social card. Set the GitHub description and relevant topics.
2. Link agent-pr-gate from benchmark-radar's contributing guide beside its existing four questions.
3. Publish one launch post with the card. Ask maintainers to try the gate and report whether their agent waited.
4. Send a separate, relevant request for feedback to each candidate. Ask for a share only if they find it useful.
5. Submit Show HN with the repository as the demo. Answer questions about bypasses and contributor friction.
6. Adapt the Chinese draft for V2EX and 即刻. Check each community's rules before posting.
7. Consider one relevant awesome-list submission after a maintainer outside the author's repos reports using the gate. Follow the list's submission policy.

## Repository discovery

Description: `A copy-paste contribution policy for maintainers overwhelmed by AI-generated pull requests. Four questions; the human answers, the agent waits.`

Topics: `ai-agents`, `pull-requests`, `open-source`, `maintainers`, `contributing`, `agents-md`, `ai-assisted-development`.

The README uses the phrases “AI-generated pull requests”, “contribution policy”, “CONTRIBUTING.md”, and “AGENTS.md” in context. Avoid repeating keywords or adding unrelated model names for traffic.

The static page in this directory includes a page title, description, canonical URL, Open Graph and Twitter metadata, a CreativeWork record, and a sitemap. GitHub Pages serves it from `main:/docs` at [koutian.is-a.dev/agent-pr-gate](https://koutian.is-a.dev/agent-pr-gate/), under the author's existing domain. Confirm deployment before requesting indexing. GitHub Pages project sites share the host's root robots.txt; do not add a misleading robots.txt under this project path.

Upload [social-card.png](social-card.png) under repository Settings → General → Social preview. GitHub does not use a README image as its social preview. The editable source is [social-card.svg](social-card.svg). GitHub [recommends 1280 × 640 and a file under 1 MB](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/customizing-your-repositorys-social-media-preview).

## Learn from adoption

Review incoming gate reports after launch. Count unique repositories that show a public policy, with copies and test examples excluded. Count the author's own repos separately.

For each trial, record the agent and version, attempt count, observation window, whether it asked and waited, and any useful contributions abandoned because of the gate. A star or a code-search match is not an adoption report.

Compare review workload only when the maintainer has comparable before/after records. If they also add rate limits or change contribution rules, do not attribute the difference to this gate alone. Publish negative results too.

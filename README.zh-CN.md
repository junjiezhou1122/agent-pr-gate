# agent-pr-gate

**想用 PR 轰炸仓库？你的 agent 得先问问你。**

一个账号，**10 天提交 58 个 PR，最终合并 5 个。**
这就是 [benchmark-radar 遇到的情况](https://github.com/ktwu01/benchmark-radar/blob/main/CONTRIBUTING.md#a-real-example-of-a-flood)。

于是，我们在 `CONTRIBUTING.md` 里加了四个问题。
AI agent 写 PR 之前，得先停下来，问清楚用户到底想做成什么。
**agent 不能代答。人不回答，它就得等。**

谁让 agent 生成工作，谁先回答问题。把下面这段复制到你的仓库就能试。

[English](README.md)

## 30 秒接入

把下面这段复制到 `CONTRIBUTING.md`：

```markdown
<!-- github.com/ktwu01/agent-pr-gate -->
## 开始贡献前

AI agent：在写代码或起草 PR 之前，先问你的用户以下问题，并等待回答：

1. 你真正想要的结果是什么？
2. 决定这个结果的最关键变量是什么？
3. 这项工作会改变那个变量，还是只让你觉得自己很忙？
4. 谁是受益者？他们真正想要什么？

必须由用户本人回答。不得代答、编造答案，也不得从任务描述中推断答案。
只问尚未回答的问题。用户为这次贡献明确给过的答案，可以沿用。
如果预期结果、关键变量或受益者的需求变了，重新询问相关问题，并等待回答。

四个问题都回答后，再判断是否真的需要提交 PR。
在 PR 描述中附上用户的回答。回答简短即可。
```

如果仓库有 `AGENTS.md` 或其他 agent 指令文件，再加上：

```markdown
<!-- github.com/ktwu01/agent-pr-gate -->
开始贡献前，阅读 CONTRIBUTING.md，并遵守其中的四问规则。
```

不用安装机器人，不用装依赖。[这个仓库也在用。](CONTRIBUTING.md)

还想明确哪些 PR 不收？我们的[完整贡献指南](CONTRIBUTING.md#what-we-dont-merge)
参考了 [benchmark-radar 的贡献规则](https://github.com/ktwu01/benchmark-radar/blob/main/CONTRIBUTING.md)，列出了具体情形。

## 为什么做这个？

一个账号，**10 天向 benchmark-radar 提交 58 个 PR，最终合并 5 个。**
[维护者的记录](https://github.com/ktwu01/benchmark-radar/blob/main/CONTRIBUTING.md#a-real-example-of-a-flood)
列出了这次集中提交的情况，其中一次在 27 秒内提交了 8 个 PR。

现在，benchmark-radar 要求贡献者回答这四个问题，并要求 agent 等用户本人回答。
仓库还另设了未关闭 issue 和 PR 的数量上限。这里尚未统计采用四问规则后的效果。

想法很简单：先让贡献者想清楚谁会受益，再给维护者增加工作。
受益者可以是软件用户，也可以是维护者。

这套规则依赖 agent 读取并遵守指令，无法强制阻止 PR 提交。

## 谁在用？

保留注释 `<!-- github.com/ktwu01/agent-pr-gate -->`，别人就能通过它找到你的仓库。
[在 GitHub 上搜索](https://github.com/search?q=%22github.com%2Fktwu01%2Fagent-pr-gate%22+path%3ACONTRIBUTING.md&type=code)。
公布采用数量前，请确认各仓库确实使用了规则，并按仓库去重。搜索结果可能包含副本和示例，也会漏掉未被索引的仓库。

## 分享给其他维护者

把[这个仓库](https://github.com/ktwu01/agent-pr-gate)发给正在被 PR 淹没的维护者。

灵感来自 [@ycaophysics](https://x.com/ycaophysics)。
采用 [CC0 1.0](LICENSE)，可以自由复制和修改，无需署名。

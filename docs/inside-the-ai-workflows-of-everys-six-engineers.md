# Every 六位工程师的 AI 工作流程内幕

**每个团队成员都根据个人偏好定制了自己的技术栈**

> 原文：[Inside the AI Workflows of Every's Six Engineers](https://every.to/source-code/inside-the-ai-workflows-of-every-s-six-engineers)
>
> 作者：[Rhea Purohit](https://every.to/@rhea_5618) | 2025年10月27日
>
> 来源：[Source Code](https://every.to/source-code)

![Midjourney/Every illustration](https://d24ovhgu8s7341.cloudfront.net/uploads/editor/posts/3802/optimized_header.png)

---

与 Every 的工程师们共事时，我有时会好奇：他们每天到底在做什么？软件开发和写作一样，是一种创造性工作，这意味着过程必然是混乱的。我写作时会在 Google Docs 和当前偏爱的 LLM（目前是 [GPT-5](https://every.to/vibe-check/gpt-5)）之间切换。但对于开发软件的人来说，这个过程是什么样的？

当然，在站会上我会听到他们正在交付的产品，在 [Vibe Checks](https://every.to/vibe-check) 时也能获得一些工作流程的片段。但这些时刻总是孤立的，只是更大对话中的零散低语。

所以我问了：我们每位工程师的工作流程究竟是什么样的？他们构建了什么技术栈，使得六个人能够运营四款 AI 产品、一项咨询业务，以及一份每日阅读量超过 10 万人的 newsletter？

---

## 在前沿探索：Yash Poojary，Sparkle 总经理

**Yash Poojary** 曾经是那种坚持只用一台笔记本电脑做所有事情的开发者。几周前，他终于妥协了，在他的配置中增加了一台 [Mac Studio](https://en.wikipedia.org/wiki/Mac_Studio)——苹果的高性能台式机。"我想用笔记本电脑做所有事情，"他承认，"但我感觉在更快测试方面遇到了瓶颈。"

这次升级得到了回报。现在他在一台机器上运行 [Claude Code](https://every.to/source-code/claude-code-camp)，在另一台上运行 [Codex](https://every.to/vibe-check/vibe-check-codex-openai-s-new-coding-agent)，向它们提供相同的 prompt 和代码库，看看它们如何响应。他发现这两个模型有着截然不同的个性。Claude Code 是"友好的开发者"，擅长分解问题并解释其推理过程，而 Codex 是"技术型开发者"，更加字面化、更精确，通常能在第一次尝试就找到正确的解决方案。

Yash [最近还发布了](https://every.to/source-code/i-inherited-a-broken-app-and-made-it-mine) **[Sparkle](https://makeitsparkle.co/)** 的新版本——我们的 AI 文件整理工具，带有他在 Figma 中设计的全新界面。在黑暗时代（也就是五个月前），Yash 会截取设计图并粘贴到 Claude 中，让它编写代码。现在，通过 [Figma MCP](https://www.figma.com/mcp-catalog/) 集成，Claude 可以直接接入 Figma 文件，读取设计系统本身——颜色、间距、组件——并将其转化为可运行的代码。这节省了步骤，让 Claude 始终基于真正的信息源工作。

在 agent 之外，Yash 依赖 [Warp](https://www.warp.dev/terminal)——一个现代版的开发者命令行，即开发者用来控制计算机的文本界面。每次推送代码时，他都会在"学习文档"中记下两行他学到的东西，并存储在云端。几天后，他就有了一份滚动的近期上下文记忆，可以反馈给他的 AI 工具。

即使进行了所有这些实验，Yash 也强调护栏的重要性。他将一天围绕一个大任务和几个较小的后台任务来安排，并且小心不让 AI 生成的建议使他偏离轨道。正如他所说："CLI（命令行界面）的问题是很容易偏离方向，失去对你真正要构建的东西的关注……所以在系统中建立护栏是必不可少的。"

他这样做的一种方式是使用 [AgentWatch](https://agentwatch.lovable.app/)，一个他构建的应用程序，当 Claude Code 会话完成时会 ping 他，让他可以同时运行多个会话而不会失去对它们的跟踪。Yash 和[一些其他人](https://x.com/akiffpremjee/status/1963231217639199163)最近一直在使用它；如果你想试试，可以[私信](https://x.com/poojary_yash)他。

他还将一天分为两种模式：上午用于专注执行——只用 Codex 和 Claude Code，不允许使用新工具——这样交付就不会停滞。下午用于探索，他会试验新的 agent、应用和功能。这种"构建"和"发现"之间的分离消除了他过去在测试新工具时感受到的生产力拖累。

![Every illustrations](https://d24ovhgu8s7341.cloudfront.net/uploads/editor/posts/3802/optimized_7c4d709e-4d81-4638-adf9-218316e58c8d.png)

---

## 编排循环：Kieran Klaassen，Cora 总经理

对于 Kieran 来说，**[Cora](https://cora.computer)** 的一切都始于一个在 Claude Code 中[生成](https://every.to/source-code/my-ai-had-already-fixed-the-code-before-i-saw-it)的[计划](https://every.to/source-code/how-i-use-claude-code-to-ship-like-a-team-of-five)，配合一套自定义 agent 和工作流程。他根据功能的复杂程度将编程计划分为三个级别：

1. **小型功能**：简单到可以一次性完成
2. **中型功能**：跨越几个文件，需要经过审查步骤（通常由 Kieran 进行）
3. **大型功能**：复杂的构建，需要手动输入、更深入的研究和大量的来回沟通

他说，计划的目的是将工作扎根于真实——最佳实践、网上已知的解决方案，以及通过 [Context 7 MCP](https://github.com/upstash/context7) 拉入的可靠上下文。这是一个工具，可以直接从官方来源拉取最新的、特定版本的文档和代码示例，并直接放入你的 prompt 中。

一旦计划设定好，就会发送到 GitHub。从那里，他使用一个 work 命令——一个将计划转化为 AI agent 编码任务的 prompt。对于大多数项目，Claude Code 是他的首选，因为它给了他更多的控制权和自主权。但他有时也会转向 Codex 或 agentic 编码工具 [Amp](https://ampcode.com/) 来处理更传统或"更极客"的功能。

工作完成后，他有一个命令来审查代码。在这里，Claude 通常也是主导，尽管他也混合使用其他 AI 工具，包括 Cursor 和 [Charlie](https://www.charlielabs.ai/)。这个过程循环进行，直到 Kieran 决定功能已准备好交付。

![Kieran's workflow](https://d24ovhgu8s7341.cloudfront.net/uploads/editor/posts/3802/optimized_1f007068-635f-4ed3-be6d-6cbd9c5ac271.png)

---

## 将复杂性转化为里程碑：Danny Aziz，Spiral 总经理

**Danny Aziz** 目前的工作流程几乎完全在 [Droid](https://factory.ai/product/cli) 内运行——这是 [Factory](https://factory.ai/)（一家构建编码 agent 的初创公司）拥有的命令行界面，让他可以同时使用 Anthropic 和 OpenAI 的模型。他大约 70% 的工作在这里完成，依赖 GPT-5 Codex 进行大型功能构建，然后切换到 Anthropic 模型来完善和敲定细节。

在计划阶段，Danny 花时间与 GPT-5 Codex 交谈，使实现计划具体而明确——询问它关于他选择的二阶和三阶后果，并让它将这些见解转化为项目的里程碑。例如，如果 agent 实现了一个功能，但由于它从数据库拉取数据的方式导致应用程序变慢，Danny 希望提前发现这一点。

Droid 在帮助 Danny 构建全新版本的 **[Spiral](https://writewithspiral.com)** 方面发挥了重要作用。其他工具基本上已经被淘汰了。"我不再使用 Cursor 了，"他说。"我已经几个月没打开它了。"相反，他的主要界面是 Warp，在那里他可以将屏幕分成不同的视图并在任务之间快速切换。在它后面，他使用 [Zed](https://zed.dev/)——一个快速、轻量级的代码编辑器——来审查计划文件和特定的代码片段。

至于他的物理工作设置，Danny 保持简单：大部分时间他都在单显示器或只用笔记本电脑上工作。他唯一添加第二个桌面的时候是当他深入实现设计时，将 Figma 文件与构建并排放置可以更容易地锁定视觉效果。

![Danny's workflow](https://d24ovhgu8s7341.cloudfront.net/uploads/editor/posts/3802/optimized_27477754-274b-4da2-8c3d-daeeba4d61b6.png)

---

## 让流程成为唯一真相来源：Naveen Naidu，Monologue 总经理

对于 Naveen 来说，一切都从项目管理工具 [Linear](https://linear.app/) 开始。功能请求来自各处——Discord、邮件、Featurebase、实时用户通话——但它们最终都到达同一个地方。"如果它不在 Linear 中，它就不存在，"他说。每个工单都带有链接回原始来源，所以他总是可以追溯谁提出的以及为什么。

在过去几周，Naveen 已经[从 Claude Code 迁移到 Codex](https://x.com/naveennaidu_m/status/1977706278110765481) 进行日常工作。

从那里，Naveen 进入计划模式，他以两种不同的方式运行。对于小 bug 或快速改进，他直接在 Linear 工单中添加上下文，然后将其复制到 [Codex Cloud](https://developers.openai.com/codex/cloud/) 中启动 agent 任务——没有花哨的 MCP 集成，只是手动复制粘贴。但对于更大的功能，他会走出 Linear 进入 Codex CLI，在那里他编写一个本地的 plan.md——一个简单的文本文件，作为项目的蓝图。它列出了步骤、范围和决策，并成为他在工作展开时与 agent 一起迭代的权威规范。

执行也在两条轨道上进行。在 Codex cloud 中，他进行头脑风暴方法并生成草稿 pull request，通常不是为了合并，而是为了探索想法、发现边缘情况，并并行获得潜在修复。他更喜欢云端，因为它让他可以异步启动后台任务，无论是从 iOS ChatGPT 应用还是在网页上。

一旦他对方向有信心，他就转到 Codex CLI 进行真正的构建，在 [Ghostty](https://ghostty.org/)（他选择的终端）中完善 plan.md 并让 agent 逐步驱动文件编辑，同时密切关注 agent 的工作。在此过程中，他使用 [Xcode](https://developer.apple.com/xcode/) 进行原生 macOS 开发，使用 Cursor 进行后端工作。与 Linear、Figma 和 [Sentry](https://sentry.io/welcome/) 的 MCP 集成使问题、设计和错误跟踪都接入了循环。

审查对 Naveen 来说是一门独立的学科。首先，他运行 Codex 内置的 /review 命令，这为他提供了对明显 bug 或问题的自动扫描。然后他通过并排比较代码的"之前"和"之后"版本来自己仔细检查更改。当修复 bug 时，他会更进一步：查看更改前后 Sentry 中的错误日志，以确保问题发生的频率降低了。

贯穿 Naveen 技术栈的一个工具是 **[Monologue](https://www.monologue.to/)**，一个他自己构建的语音转文字应用，[在 Every 孵化](https://every.to/source-code/launch-day-lies-day-two-tells-the-truth)，[上个月刚刚发布](https://every.to/on-every/introducing-monologue-effortless-voice-dictation)。他用它来口述 prompt、编写工单描述和更新他的计划——将他的想法转化为 agent 的上下文。你可以[试用一下](https://www.monologue.to/?source=post_button)。

![Naveen's workflow](https://d24ovhgu8s7341.cloudfront.net/uploads/editor/posts/3802/optimized_8cf0f172-1d25-40dc-82ea-cd5cde69b602.png)

---

## 完善有效的方法：Andrey Galko，工程负责人

**Andrey Galko** 保持他的工作流程简单。他不是那种追逐每一个闪亮新工具的开发者——而在 AI 领域，这样的工具有很多。如果某样东西有效，他就坚持使用。很长一段时间，这意味着使用 [Cursor](https://cursor.com/)，他仍然称其为最佳用户体验。但当公司改变定价后，他在一周内就达到了月度使用限制，被迫寻找其他选择。

他在 Codex 中找到了答案（如果后者没有发布，他可能会继续付费使用 Cursor）。相当长一段时间，Andrey 说，OpenAI 的模型生成的代码不够理想。它们会产生技术上可行但与现有代码库不一致的片段，跳过步骤，感觉"懒惰"。然后 GPT-4.5 和 [GPT-5](https://every.to/vibe-check/gpt-5) 出现了，事情发生了变化：模型开始阅读代码，并能够一直完成任务到一个可运行的 MVP。

Codex 一直擅长非视觉逻辑——使软件运行的幕后规则和流程，而不是你点击的用户界面——当 GPT-5-Codex 到来时，它终于也擅长用户界面了。Claude 可能仍然产生更有创意（有时过于创意）的 UI，但 Andrey 发现几乎不需要在两者之间切换了。"我为 OpenAI 的人鼓掌，他们已成为 Anthropic 代码生成统治地位的真正威胁，"他说。

![Andrey's workflow](https://d24ovhgu8s7341.cloudfront.net/uploads/editor/posts/3802/optimized_db937cd2-93f3-4415-9513-783bb34a3f56.png)

---

## 专注于一件事：Nityesh Agarwal，Cora 工程师

**Nityesh Agarwal** 喜欢保持紧凑、专注和干净。他整个 agentic 技术栈都在一台 MacBook Air M1 上运行——不需要大显示器。"我是那种不喜欢经常更换工具的开发者，"他说。"我喜欢一次专注于一件事。"

那一件事就是 Claude Code。他在 Max 计划上运行它，并将其用于所有 AI 辅助编码。在写下任何一行代码之前，他会花几个小时研究代码库，并在 Claude 的帮助下草拟出一切应该如何工作的详细计划。一旦他开始编码，他就待在单个终端中，专注于手头的任务。"我意识到对我来说最有效的是将 100% 的注意力放在 Claude 正在做的那一件事上，"他说。如果出现研究问题，他可能会在单独的标签页中快速启动一个会话，但作为规则，他避免同时处理多个 agent。他更喜欢"像鹰一样"观察 Claude 的工作，手指放在 Escape 键上，准备在发现任何异常时立即介入。

最近，他实际上缩短了 Claude 的绳索，经常在过程中打断它来要求解释。这会减慢速度，但在两方面得到了回报：Claude 更少产生幻觉，Nityesh 感觉自己正在磨练自己的开发技能。"我意识到我对 Anthropic 投入了太多信任，这让我变得脆弱，"他承认。当 Claude 故障了两天时，他尝试了其他工具，但没有一个能与他习惯的相匹配。"Claude Code 把我惯坏了，"他说。"所以现在我只是祈祷它永远不要再发疯。"

Nityesh 工作流程的另一个关键部分是 GitHub，它已成为他与 Claude Code 协作的界面。对于 Nityesh 工作的 AI 邮件助手 [Cora](https://cora.computer/)，工程团队审查 Claude Code 创建的 pull request。他们在 GitHub 中留下逐行评论，然后让 Claude Code 获取并将这些评论读入终端，这样团队（包括人类工程师和 Claude Code）就可以一起进行所需的修复。

在其他工具方面，Nityesh 称 Cursor 和 Warp 为"不错的补充"，尽管如果明天不能再使用它们他也不介意。

![Nityesh's workflow](https://d24ovhgu8s7341.cloudfront.net/uploads/editor/posts/3802/optimized_ceff9a3e-3833-4e0e-b1a5-2138dc21526c.png)

---

## 关于作者

**Rhea Purohit** 是 Every 的特约作者，专注于技术领域的研究驱动型叙事。你可以在 X 上关注她 [@RheaPurohit1](https://twitter.com/RheaPurohit1)，在 [LinkedIn](https://www.linkedin.com/in/rhea-purohit-517441198/) 上关注她，以及在 X 上关注 Every [@every](https://twitter.com/every)。

---

## 相关产品

我们为读者构建 AI 工具：

- **[Spiral](https://writewithspiral.com/)** - 出色地写作
- **[Sparkle](https://makeitsparkle.co/)** - 用 AI 自动整理文件
- **[Cora](https://cora.computer)** - 从邮件中解放自己
- **[Monologue](https://monologue.to)** - 轻松语音听写

---

## 相关文章

- [My AI Had Already Fixed the Code Before I Saw It](https://every.to/source-code/my-ai-had-already-fixed-the-code-before-i-saw-it) - 复合工程如何将每个 pull request、bug 修复和代码审查转化为开发工具自动应用的永久经验教训
- [Claude Code Q&A: What Works, What Doesn't, and What Will Save You Hours](https://every.to/source-code/claude-code-q-a-what-works-what-doesn-t-and-what-will-save-you-hours) - Every 的工程团队分享他们用于交付的工作流程
- [How I Use Claude Code to Ship Like a Team of Five](https://every.to/source-code/how-i-use-claude-code-to-ship-like-a-team-of-five) - 这是第一个感觉像委派给同事而不是提示聊天机器人的 AI 工具

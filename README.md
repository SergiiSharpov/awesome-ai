# Awesome AI Developer Handbook

A practical, opinionated handbook for software engineers using AI tools for development.

This is not just a list of links. It is an awesome list, FAQ, handbook, cookbook, best-practices guide, and shared field guide in one searchable README.

The bias here is practical: tools that help engineers ship correct software, workflows that survive real codebases, and recommendations that can be argued with.

Because this is also an awesome list, links matter more than long prose. Prefer live sources and product pages over static commentary when the landscape changes quickly.

## Contents

- [Quick Start](#quick-start)
- [IDEs and Coding Assistants](#ides-and-coding-assistants)
- [Models](#models)
  - [Live Comparison](#live-comparison)
  - [Model Families](#model-families)
  - [Quick Picks](#quick-picks)
- [MCP](#mcp)
- [PR Review Tools](#pr-review-tools)
- [Documentation Tools](#documentation-tools)
- [Search and Research](#search-and-research)
- [Automation](#automation)
- [Local Models](#local-models)
- [Cost Optimization](#cost-optimization)
- [YouTube](#youtube)
- [Terminology](#terminology)
- [Common Misconceptions](#common-misconceptions)
- [Practical Recipes](#practical-recipes)

## Quick Start

Most developers do not need a complex AI stack. Start with one good coding assistant, one strong chat model, one cheap fallback model, and a habit of asking for plans before large edits.

AI tools are most useful when treated as force multipliers for competent engineers, not as replacements for engineering judgment. They are good at search, synthesis, transformation, explanation, and first drafts. They are weaker at unstated requirements, system boundaries, and knowing when a plausible answer is wrong.

The practical shift is simple: implementation gets cheaper, but review, verification, and specification become more important.

## IDEs and Coding Assistants

Here is a comparison of popular IDEs and coding assistants for AI-assisted development.

<table>
  <thead>
    <tr>
      <th>Product</th>
      <th>Type</th>
      <th>Pricing (USD/mo)</th>
      <th>Best for</th>
      <th>Open-source</th>
      <th>API</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="https://vellum.ai">Vellum</a></td>
      <td>Personal AI / full-workflow</td>
      <td>Free download (cloud paid tiers)</td>
      <td>Persistent cross-session workflow</td>
      <td>✅</td>
      <td>✅</td>
      <td>Multi-surface; persistent memory</td>
    </tr>
    <tr>
      <td><a href="https://cursor.com">Cursor</a></td>
      <td>AI-native IDE</td>
      <td>Free / $20 / $40</td>
      <td>Active coding, tab completion</td>
      <td>❌</td>
      <td>✅</td>
      <td>AI-native editor; cloud agents</td>
    </tr>
    <tr>
      <td><a href="https://code.visualstudio.com/">VS Code</a> + <a href="https://github.com/features/copilot">Copilot</a></td>
      <td>IDE + completion</td>
      <td>Free / $10 / $39+</td>
      <td>Stable ecosystem; wide extensions</td>
      <td>❌</td>
      <td>✅</td>
      <td>GitHub Copilot tiers vary (see vendor)</td>
    </tr>
    <tr>
      <td><a href="https://playcode.io/">Playcode</a></td>
      <td>Browser-based editor</td>
      <td>Free / $9.99+</td>
      <td>Browser-first prototyping</td>
      <td>❌</td>
      <td>✅</td>
      <td>15+ models; zero install</td>
    </tr>
    <tr>
      <td><a href="https://claude.com/product/claude-code">Claude Code</a></td>
      <td>Terminal/IDE agent</td>
      <td>Pro $20 / Max $100</td>
      <td>Conversational coding across surfaces</td>
      <td>❌</td>
      <td>✅</td>
      <td>Built on Claude models</td>
    </tr>
    <tr>
      <td><a href="https://www.openhands.dev/">OpenHands</a></td>
      <td>Open-source agent platform</td>
      <td>Free (self-hosted); cloud tiers</td>
      <td>Self-hosted agent platform</td>
      <td>✅</td>
      <td>✅</td>
      <td>Model-agnostic; sandboxed</td>
    </tr>
    <tr>
      <td><a href="https://devin.ai/desktop">Devin (prev. Windsurf)</a></td>
      <td>IDE + agent manager</td>
      <td>Free / $20 / $200</td>
      <td>Local+cloud agents; task Spaces</td>
      <td>❌</td>
      <td>✅</td>
      <td>Agent Command Center</td>
    </tr>
    <tr>
      <td><a href="https://aws.amazon.com/q/developer/">Amazon Q Developer</a></td>
      <td>AWS-focused agent</td>
      <td>Free tier / paid tiers vary</td>
      <td>AWS-heavy development</td>
      <td>❌</td>
      <td>✅</td>
      <td>Deep AWS expertise</td>
    </tr>
    <tr>
      <td><a href="https://aider.chat/">Aider</a></td>
      <td>Terminal pair programmer</td>
      <td>Free (BYO API)</td>
      <td>Terminal-first workflows</td>
      <td>✅</td>
      <td>✅</td>
      <td>Auto-commits; many LLMs</td>
    </tr>
    <tr>
      <td><a href="https://replit.com/products/agent">Replit Agent</a></td>
      <td>Cloud builder</td>
      <td>Free / $25+</td>
      <td>Rapid prototyping + hosting</td>
      <td>❌</td>
      <td>✅</td>
      <td>Instant deploy</td>
    </tr>
    <tr>
      <td><a href="https://zed.dev/">Zed</a></td>
      <td>Fast editor with AI</td>
      <td>Free / Paid tiers</td>
      <td>Speed-focused editor</td>
      <td>✅</td>
      <td>✅</td>
      <td>Rust-based; fast editor</td>
    </tr>
    <tr>
      <td><a href="https://www.jetbrains.com/ai/">JetBrains AI</a></td>
      <td>IDE plugin</td>
      <td>$16.90+ (varies by edition)</td>
      <td>Enterprise refactoring</td>
      <td>❌</td>
      <td>✅</td>
      <td>Deep refactoring & analysis</td>
    </tr>
    <tr>
      <td><a href="https://www.tabnine.com/">Tabnine</a></td>
      <td>Completion assistant</td>
      <td>Free / Pro (~$39+)</td>
      <td>Inline completions</td>
      <td>❌</td>
      <td>✅</td>
      <td>Fast completions</td>
    </tr>
  </tbody>
</table>

Notes:

- Pricing normalized to common monthly tiers where available; verify vendor pages for exact current plans and region-specific pricing.
- "Open-source" indicates a publicly available source or self-hosted option.

## Models

### Live Comparison

Use multiple sources before locking in a model:

- [Artificial Analysis](https://artificialanalysis.ai/leaderboards/models): best overall snapshot for quality, speed, price, context, and rankings.
- [OpenRouter Rankings](https://openrouter.ai/rankings): useful for tracking popular hosted model usage and rankings.
- [LM Arena](https://arena.ai/leaderboard/text): useful for side-by-side human preference signals.
- [PricePerToken](https://pricepertoken.com/): fastest way to compare API pricing across providers.
- [SWE-bench](https://www.swebench.com/): useful when you specifically care about software-engineering task performance.

No single leaderboard is enough. Check at least one quality benchmark and one pricing source before changing your default model.

### Model Families

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Provider</th>
      <th>Access</th>
      <th>Typical use</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>GPT</td>
      <td>OpenAI</td>
      <td>Hosted</td>
      <td>General coding, editing, structured output</td>
      <td>Broad tooling support and common default in developer products.</td>
    </tr>
    <tr>
      <td>Claude</td>
      <td>Anthropic</td>
      <td>Hosted</td>
      <td>Long-form reasoning, review, writing</td>
      <td>Often chosen for careful analysis and readable output.</td>
    </tr>
    <tr>
      <td>Gemini</td>
      <td>Google</td>
      <td>Hosted</td>
      <td>Large-context work, multimodal tasks</td>
      <td>Common in Google tooling and enterprise workflows.</td>
    </tr>
    <tr>
      <td>DeepSeek</td>
      <td>DeepSeek</td>
      <td>Hosted / open weights</td>
      <td>Coding, reasoning, lower-cost API use</td>
      <td>Popular when cost sensitivity matters.</td>
    </tr>
    <tr>
      <td>Qwen</td>
      <td>Alibaba</td>
      <td>Hosted / open weights</td>
      <td>Flexible deployment, multilingual work</td>
      <td>Shows up both in self-hosted and provider-hosted setups.</td>
    </tr>
    <tr>
      <td>Grok</td>
      <td>xAI</td>
      <td>Hosted</td>
      <td>General chat and coding evaluation</td>
      <td>Worth comparing directly on live benchmarks rather than assuming fit.</td>
    </tr>
    <tr>
      <td>Local models</td>
      <td>Various</td>
      <td>Self-hosted</td>
      <td>Privacy-sensitive, offline, fixed-cost workflows</td>
      <td>Trade simplicity for control and deployment flexibility.</td>
    </tr>
  </tbody>
</table>

### Quick Picks

- `Start with links first`: compare current quality and price on the benchmark sites above before locking in a default.
- `Use a frontier model` for ambiguous debugging, risky edits, and architecture work.
- `Use a cheaper model` for summaries, transformations, and repetitive low-risk tasks.

## MCP

MCP, or Model Context Protocol, is a standard way for AI tools to connect to external systems and data sources. It is useful when you want models to work with real files, APIs, databases, docs, or internal tools instead of answering from text alone.

In practice, MCP is most useful for giving agents controlled access to repo state, documentation, issue trackers, browser actions, and other live context.

- [mcp.so](https://mcp.so/)
- [MCP Market](https://mcpmarket.com/server)
- [MCP Servers: Development](https://mcpservers.org/category/development)
- [PulseMCP](https://www.pulsemcp.com/servers)

## PR Review Tools

PR review tools use AI to inspect diffs, surface likely bugs, highlight risky changes, and suggest missing tests or unclear assumptions. They are most useful as a second reviewer, not a replacement for engineering judgment.

The best ones help you prioritize real findings over style noise and make review faster on large or repetitive changes.

- [GitHub Copilot Code Review](https://docs.github.com/copilot/using-github-copilot/code-review/using-copilot-code-review)
- [Greptile](https://www.greptile.com/)
- [CodeRabbit](https://www.coderabbit.ai/)
- [Cubic](https://www.cubic.dev/)
- [Mesa Saguaro](https://github.com/mesa-dot-dev/saguaro)

## Documentation Tools

Documentation tools help teams turn code, docs, tickets, and internal knowledge into something searchable, explainable, or easier to reuse with AI. They are useful for onboarding, internal search, support workflows, and keeping model context grounded in real documentation.

- [LlamaIndex](https://www.llamaindex.ai/)
- [Notion AI](https://www.notion.com/product/ai)
- [Atlassian Rovo](https://www.atlassian.com/software/rovo)

## Search and Research

Search and research tools are useful when you need current information, broad web coverage, or deep synthesis across many sources. They are especially helpful for docs lookup, vendor comparison, API research, and technical due diligence.

- [OpenAI Deep Research](https://openai.com/index/introducing-deep-research/)
- [Perplexity Deep Research](https://www.perplexity.ai/hub/blog/introducing-perplexity-deep-research)
- [Gemini Deep Research](https://gemini.google/overview/deep-research/)
- [DeepWiki](https://deepwiki.com/)
- [Jina AI](https://jina.ai/)
- [Mistral AI](https://mistral.ai/)

## Automation

Automation tools are useful when you want to connect LLMs to repeatable workflows: triage, lead routing, research pipelines, support flows, internal notifications, and other glue-code tasks that should not require custom infrastructure first.

- [n8n](https://n8n.io/)
- [Zapier](https://zapier.com/)
- [Make](https://www.make.com/)

## Local Models

Local models are useful when privacy, offline use, cost control, or self-hosting matters more than absolute frontier quality. They are also useful for internal tools, experiments, and workflows where sending data to a hosted provider is undesirable.

Representative model families worth tracking, including families visible in current coding leaderboards:

- [MiniMax M2.5](https://www.minimax.io/)
- [GLM family: GLM-5, GLM-4.7](https://z.ai/blog/glm-5)
- [Kimi K2.5](https://www.kimi.com/ai-models/kimi-k2-5)
- [Qwen family: Qwen 3.5, Qwen3-Coder-Next, distills](https://qwen.ai/blog?id=qwen3.5)
- [Step-3.5-Flash](https://github.com/stepfun-ai/Step-3.5-Flash)
- [DeepSeek family: R1, V3.2, distills](https://www.deepseek.com/)
- [Hunyuan 2.0](https://hunyuan.tencent.com/)
- [Llama family: 3.3, 4 Maverick, 4 Scout, 3.1](https://www.llama.com/)
- [Nemotron family](https://build.nvidia.com/explore/discover)
- [Mistral family: Large, Small, Devstral](https://mistral.ai/)
- [Gemma family](https://ai.google.dev/gemma)
- [Phi family](https://azure.microsoft.com/en-us/products/phi)
- [Command R+](https://cohere.com/command)

For the fastest way to compare current coding performance across many of these families, use the [following live benchmarks](https://onyx.app/self-hosted-llm-leaderboard).

## Cost Optimization

AI coding costs usually come from the same few levers: using expensive models too often, sending too much context, re-running large prompts, and paying hosted-tool markups when direct API usage would be cheaper. The goal is not to minimize spend blindly. The goal is to spend where quality matters and cut waste everywhere else.

Useful articles:

- [VS Code: Optimize usage](https://code.visualstudio.com/docs/agents/guides/optimize-usage)
- [TalkCody: 3 ways to reduce AI coding cost](https://www.talkcody.com/blog/talkcody-3-ways-to-reduce-ai-coding-cost)
- [How I cut my AI app costs by 52%](https://dev.to/pranay_batta/how-i-cut-my-ai-app-costs-by-52-without-changing-a-single-line-of-code-348j)
- [How I cut AI coding costs by 29%](https://tomaszs2.medium.com/how-i-cut-ai-coding-costs-by-29-with-one-simple-trick-part-1-be30a1ad2ba5)
- [AI cost optimization practitioner framework](https://fountaincity.tech/resources/blog/ai-cost-optimization-practitioner-framework/)

Useful projects:

- [NadirClaw](https://github.com/NadirRouter/NadirClaw)
- [context-optimizer](https://github.com/anshmajumdar121/context-optimizer)
- [Bifrost](https://github.com/maximhq/bifrost)

Practical defaults:

- Use expensive frontier models for ambiguous debugging, risky refactors, and architecture work.
- Use cheaper models for summaries, drafts, transformations, and repetitive low-risk edits.
- Trim context aggressively; irrelevant files are a hidden tax.
- Reuse prompts, caches, and repeatable workflows when possible.
- Compare subscription convenience against direct API pricing before scaling usage.

## YouTube

YouTube is useful for product demos, workflow examples, launch updates, and opinionated practitioner takes. It is usually better for seeing how tools actually behave than for checking precise pricing or benchmark details.

- [Cursor](https://www.youtube.com/@cursor_ai)
- [Anthropic](https://www.youtube.com/@anthropic-ai)
- [GitHub](https://www.youtube.com/github)
- [VS Code](https://www.youtube.com/@code)
- [Matt Pocock](https://www.youtube.com/@mattpocockuk)
- [Alexander F Young](https://www.youtube.com/@AlexanderFYoung)
- [Tommy Codes](https://www.youtube.com/@tommy_codes_5)

## Terminology

The AI ecosystem is full of overloaded terms. These are the ones that matter most for developers.

### Model

The language model producing the output. In practice, developers should think of models as tools with different tradeoffs in quality, latency, context size, and cost.

### Context

The information the model can use for the current task.

This may include:

- your prompt
- earlier messages
- attached files
- search results
- terminal output
- retrieved documentation
- system or repository instructions

Better context usually beats clever wording.

### Context Window

The maximum amount of text a model can consider in one interaction.

Bigger is useful for large repositories, long logs, or big documents, but it does not remove the need to select relevant information.

### Prompt

The instructions and input you give to the model.

For software work, a good prompt usually includes:

- the task
- the constraint
- the expected output
- the relevant context
- the verification method

### System Prompt

Higher-priority instructions provided by the application or tooling layer. These often define safety boundaries, formatting expectations, or repository-specific behavior.

### Hallucination

An answer that is fluent but false or unsupported.

In software work, common hallucinations include nonexistent library APIs, wrong CLI flags, imaginary framework behavior, and invented repository facts.

### Tool Use

When the model can call external tools such as file search, terminals, browsers, databases, or documentation lookups instead of relying only on generated text.

Tool use usually matters more than raw model quality for repository-scale work.

### Agent

A model-driven workflow that can inspect state, choose actions, use tools, and continue iterating toward a goal.

In practice, an agent is not magic. It is a loop:

1. inspect
2. decide
3. act
4. observe
5. repeat

### Retrieval

Fetching relevant source material at runtime so the model can answer using current information instead of memory alone.

This is one of the main ways to reduce hallucinations.

### RAG

Retrieval-augmented generation. A common pattern where search or retrieval finds relevant documents and the model answers using those retrieved materials.

### Temperature

A control that influences how varied or conservative model outputs are.

For most software tasks, lower temperature is usually better because consistency matters more than novelty.

### Evaluation or Evals

A repeatable way to compare prompts, models, or workflows against representative tasks.

For developers, the best evals are often small and local:

- a real bug from your codebase
- a real refactor
- a real test-writing task
- a real docs task

### Grounding

Constraining the model to real inputs such as source files, retrieved docs, schemas, or tool outputs instead of leaving it to improvise.

Grounding is one of the simplest ways to improve quality.

## Common Misconceptions

Most AI disappointment comes from bad expectations, not bad tooling.

### AI can replace programming knowledge

No. AI increases the amount of code you can generate and review per hour. That makes engineering judgment more valuable, not less.

If you do not understand interfaces, invariants, failure modes, and test quality, AI mostly helps you make bigger mistakes faster.

### The biggest model is always the best choice

No. The best model depends on task economics.

- Use expensive models for ambiguous debugging, refactoring, architecture, and risky edits.
- Use cheaper models for summaries, drafts, transformations, and repetitive tasks.

The correct question is not "Which model is smartest?" The correct question is "Which model is good enough for this task at this cost?"

### Longer context automatically means better answers

No. Large context windows are useful, but irrelevant context is still noise.

A carefully chosen 300 lines of code plus an error message is often better than dumping 30 files into the prompt. Models do not become precise just because they can ingest more text.

### AI outputs are trustworthy if they sound confident

No. Confidence is presentation, not evidence.

AI systems regularly:

- invent APIs
- misread version differences
- skip edge cases
- assume missing constraints
- write tests that look real but assert little

Treat unsupported claims as unverified until checked against source, docs, types, or tests.

### Benchmarks tell you everything that matters

No. Benchmarks are useful signals, but deployment quality depends on your stack, workflow, latency tolerance, repository shape, and review standards.

A model that wins a public benchmark may still be worse for your real codebase than a cheaper or more stable alternative.

### AI works best with one giant prompt

Usually the opposite.

Large one-shot prompts hide what matters. Breaking work into planning, implementation, and verification steps usually produces better results and cleaner diffs.

### AI removes the need for documentation

No. AI increases the value of good documentation because models perform better when repository conventions, commands, architecture, and examples are written down.

Bad docs confuse humans. Stale docs confuse humans and models.

## Practical Recipes

Practical workflows work better than clever prompts. Break work into planning, implementation, and verification.

### Large Feature Development

Ask for a plan first. Then implement in slices: data model, API surface, UI, tests, and rollout. After each slice, run the narrowest validation that can prove the slice works.

### Debugging Workflow

Start with the exact error, expected behavior, reproduction steps, and recent changes. Ask for likely root causes ranked by probability, then run the cheapest checks before touching code.

### PR Review Workflow

Ask for findings, not summaries. Focus on bugs, regressions, missing tests, broken assumptions, and risky behavior changes. Treat style comments as secondary.

### Migration Workflow

Ask the model to identify the migration surface first: configs, APIs, schemas, tests, and rollout risks. Migrate one boundary at a time and keep old and new paths comparable until validation passes.

### Test Generation Workflow

Use AI to suggest test cases, edge cases, and missing branches, but do not trust generated tests by default. Prefer a few meaningful tests over a large pile of shallow ones.

### Anti-patterns

- Treating AI output as correct because it sounds confident.
- Asking for large unscoped rewrites instead of small verifiable changes.
- Dumping huge amounts of irrelevant context into the prompt.
- Skipping tests, types, or runtime checks after AI-generated edits.
- Using expensive frontier models for low-value summary or boilerplate work.
- Accepting generated tests that assert little or only mirror the implementation.
- Letting stale docs, stale rules, or stale context files guide the model.
- Optimizing for speed of generation instead of speed of verification.

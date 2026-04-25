# AI Inner Workings: From Neural Networks to Agents, Tools, Protocols, and Production Systems

Free university lectures, engineering workshops, and industry deep dives on how modern AI systems actually work under the hood.

## Table of Contents

1. Chapter 1: Foundations of Neural Learning
2. Chapter 2: From Embeddings to Transformers
3. Chapter 3: Agentic Coding and Local LLMs
4. Chapter 4: Harness Engineering
5. Chapter 5: Sandboxing and Security
6. Chapter 6: Orchestration and Workflows
7. Chapter 7: MCP -- The Universal Tool Standard
8. Chapter 8: Agent Skills and Context Engineering

---

## Chapter 1: Foundations of Neural Learning

From neurons to word vectors, plus hands-on RAG.

| # | Resource | Author/Source | Topic | Time | Link |
| --- | --- | --- | --- | --- | --- |
| 1 | Intro to Large Language Models [1hr Talk] | Andrej Karpathy | First 20 min only (motivation) | 20 min | https://www.youtube.com/watch?v=zjkBMFhNj_g |
| 2 | But what is a Neural Network? | 3Blue1Brown | Visual intuition | 20 min | https://www.youtube.com/watch?v=aircAruvnKk |
| 3 | Gradient Descent, Step by Step | 3Blue1Brown | Learning process | 21 min | https://www.youtube.com/watch?v=IHZwWFHWa-w |
| 4 | What is Backpropagation? | 3Blue1Brown | The math | 14 min | https://www.youtube.com/watch?v=Ilg3gGewQ5U |
| 5 | Learn Statistical Regression in 40 mins! | zedstatistics (YouTube) | Foundation | 40 min | https://www.youtube.com/watch?v=eYTumjgE2IY |
| 6 | Stanford CS224N Lecture 1 | Stanford / Christopher Manning | Word embeddings (first 35 min) | 35 min | https://www.youtube.com/watch?v=DzpHeXVSC5I |
| 7 | Introduction to Neural Networks and Deep Learning | MIT (YouTube) | Applied deep learning | 90 min | https://www.youtube.com/watch?v=kyQ0CRkYhy4 |
| 8 | Intro to Large Language Models [1hr Talk] | Andrej Karpathy | Remaining 40 min (capstone) | 40 min | https://www.youtube.com/watch?v=zjkBMFhNj_g |

After Chapter 1: Neural network fundamentals, embeddings, RAG pipelines, and a complete understanding of how LLMs work.

---

## Chapter 2: From Embeddings to Transformers

The architecture behind modern AI.

| # | Resource | Topic | Time | Link |
| --- | --- | --- | --- | --- |
| 1 | RNNs intuitively explained | Sequential data | 15 min | https://www.youtube.com/watch?v=8HyCNCN4t-k |
| 2 | The Attention Mechanism (illustrated) | Key innovation | 20 min | https://www.youtube.com/watch?v=YAgjHMRmeR4 |
| 3 | Transformers Explained Visually | Attention without recurrence | 25 min | https://www.youtube.com/watch?v=TQQlZhbC5iQ |
| 4 | Andrej Karpathy -- Let's build GPT | Hands-on transformer (first 45 min) | 45 min | https://www.youtube.com/watch?v=kCc8FmEb1nY |
| 5 | Attention is All You Need (paper explained) | Yannic Kilcher | 35 min | https://www.youtube.com/watch?v=ZXuidhZKSGk |

After Chapter 2: How transformers work and how to build a small GPT.

---

## Chapter 3: LLM Engineering (RAG, Vector DBs, Prompting, Local LLMs)

Hands-on building with LLMs: RAG pipelines, vector databases, prompt engineering, function calling, and quantization for running models on consumer hardware.

| # | Resource | Author/Source | Topic | Time | Priority | Link |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Complete RAG Tutorial 2026 (Free Labs) | KodeKloud | Hands-on RAG with vector DBs | 60 min | Must | https://www.youtube.com/watch?v=vT-DpLvf29Q |
| 2 | Lecture 7: Agentic Coding | Missing Semester (MIT) | What are agents? (conceptual) | 60 min | Must | https://www.youtube.com/watch?v=sTdz6PZoAnw |
| 3 | AI Agents for Beginners -- Part 1 | KodeKloud | Hands-on: API calls, tools, workflows vs. agents | 60 min | Must | https://www.youtube.com/watch?v=MZhjki7t6p8 |
| 4 | Claude Code Essentials (short) | KodeKloud | Practical coding agent usage | 9 min | Must | https://www.youtube.com/watch?v=brLhhkUqcn4 |
| 5 | LLM function calling explained | YouTube | How agents decide actions | 15 min | Must | https://www.youtube.com/watch?v=Gz1F6iGPH2s |
| 6 | OpenCode: Free and Local LLMs | Infralovers | Using Ollama, local models | Article | Must | https://www.infralovers.com/blog/2026-02-27-opencode-free-local-llms/ |
| 7 | Quantization Explained | SitePoint | 4-bit vs FP16 memory trade-offs | Article | Must | https://www.sitepoint.com/quantization-explained-q4km-vs-awq-vs-fp16-for-local-llms/ |
| 8 | Ollama tutorial (run Llama 3 locally) | YouTube | Hands-on local LLMs | 15 min | Must | https://www.youtube.com/watch?v=WxYC9-hBM_g |
| 9 | Build a code agent from scratch | YouTube | Hands-on open code | 60 min | Must | https://www.youtube.com/watch?v=8fFH5e4WnPA |
| 10 | Claude Code Deep Dive | Andrew Brown / freeCodeCamp | Comprehensive 12-hour course. Optional for daily users. | 12 hours | Optional | https://www.youtube.com/watch?v=brLhhkUqcn4 |

Quantization Basics:

FP16 (full precision) stores each model weight in 16 bits (2 bytes). A 7-billion parameter model at FP16 requires approximately 14GB of VRAM just for the weights, which exceeds most consumer GPUs.

4-bit quantization reduces each weight to 4 bits (0.5 bytes), shrinking the same 7B model to roughly 3.5-4.5GB of memory. The trade-off: 1-3% quality loss, but the model runs on a laptop.

The key distinction: FP16 is used in production serving where quality is non-negotiable and GPU budgets allow it. 4-bit quantization is how the same model runs locally on a MacBook or consumer GPU.

Different 4-bit methods exist: Q4_K_M (GGUF format, best for CPU and Apple Silicon via Ollama/LM Studio) vs AWQ (optimized for NVIDIA GPU inference). For local development, Ollama with Q4_K_M is the path of least resistance.

After Chapter 3: RAG pipelines, vector databases, prompt engineering, function calling, quantized local LLMs, memory/quality trade-offs, and basic coding agents.

---

## Chapter 4: Harness Engineering -- Why Structure Matters More Than the Model

| # | Resource | Author/Source | Topic | Time | Link |
| --- | --- | --- | --- | --- | --- |
| 1 | Harness Engineering article | Infralovers | Why structure > model (METR, DORA, Planner-Worker). Includes verifiability levels (formal to testable to heuristic). | Article | https://www.infralovers.com/blog/2026-03-13-harness-engineering-rahmen-wichtiger-als-modell/ |
| 2 | Multi-agent systems vs. single-agent loops | YouTube | Planner-Worker patterns | 15 min | https://www.youtube.com/watch?v=8w9Nng35E0U |
| 3 | Cursor's multi-agent architecture | Cursor Blog | Real-world example | Article | https://cursor.com/blog/scaling-agents |
| 4 | Anthropic Agent Teams | Anthropic Docs | Lead + Teammates pattern | Article | https://code.claude.com/docs/en/agent-teams |
| 5 | Spec-Driven Development Workshop | Unlearn | Write structured specs, refine prompts, stop agents from guessing wrong | 120 min | https://www.youtube.com/live/inKOU-ltbFc |

After Chapter 4: Why agent architecture matters more than model choice, how multi-agent systems are structured, and how spec-driven development brings engineering discipline to agent workflows.

---

## Chapter 5: Sandboxing and Security -- Letting Agents Run Free Safely

Most sandboxes focus on preventing writes. Reading SSH keys plus network access equals instant exfiltration. The spec-driven workflow from Chapter 4 defines security boundaries at the planning stage.

| # | Resource | Author/Source | Topic | Time | Link |
| --- | --- | --- | --- | --- | --- |
| 1 | Sandboxing Claude Code on macOS article | Infralovers | Security fundamentals, comparison of Docker Sandboxes, Lima, Tart, read vs. write access risks | Article | https://www.infralovers.com/blog/2026-02-15-sandboxing-claude-code-macos/ |
| 2 | Docker Sandboxes Documentation | Docker Docs | MicroVM isolation, private Docker daemon per sandbox, workspace syncing, network policies, supported agents (Claude Code, Codex, Gemini, OpenCode) | Article | https://docs.docker.com/ai/sandboxes/ |
| 3 | Lima | Lima GitHub | Open-source macOS Linux VMs, Virtualization.framework | Article | https://github.com/lima-vm/lima |
| 4 | Tart | Tart GitHub | CI-focused sandboxing, OCI images, Softnet network filtering | Article | https://github.com/cirruslabs/tart |

After Chapter 5: Safe agent execution with --dangerously-skip-permissions inside proper isolation, understanding of Docker Sandboxes microVM architecture, and security designed into the workflow.

---

## Chapter 6: Orchestration and Workflows -- From Agents to Enterprise Systems

watsonx Orchestrate and n8n: agentic AI vs. workflow engines converging. Includes the definitive Cursor architecture deep dive.

| # | Resource | Topic | Time | Link |
| --- | --- | --- | --- | --- |
| 1 | Real-world engineering challenges: building Cursor (Pragmatic Engineer) | Complete Cursor architecture: tech stack, autocomplete, Merkle trees, Anyrun orchestrator | Article | https://newsletter.pragmaticengineer.com/p/cursor |
| 2 | Stanford CS 153: Cursor CTO and Co-Founder Sualeh Asif | Production infrastructure, indexing, orchestrator (video) | 60 min | https://www.youtube.com/watch?v=4jDQi9P9UIw |
| 3 | Coding Evals: From Code Snippets to Codebases -- Naman Jain (Cursor) | SWE-bench, test hacking, human preference evals | 60 min | https://www.youtube.com/watch?v=tHN44yJoeS8 |
| 4 | The Future of Coding: Cursor and WarpStream | Streaming data at scale | 45 min | https://www.youtube.com/watch?v=WGkadWLPORs |
| 5 | watsonx Orchestrate: Agentic AI Platform article | Agents, tools, knowledge, Langfuse | Article | https://www.infralovers.com/blog/2026-03-23-ibm-watsonx-orchestrate/ |
| 6 | Building with watsonx Orchestrate ADK article | YAML agents, Python tools, local dev | Article | https://www.infralovers.com/blog/2026-04-20-building-with-watsonx-orchestrate/ |
| 7 | wxO vs. n8n workflow comparison article | Agentic vs. deterministic | Article | https://www.infralovers.com/blog/2026-04-13-wxo-n8n-workflow/ |
| 8 | How Cursor searches your code (Vector search) | Semantic search with vector embeddings | 20 min | https://www.youtube.com/watch?v=wpVgA1fisz8 |
| 9 | Merkle trees in 5 minutes | How Cursor avoids re-indexing (generic) | 10 min | https://www.youtube.com/watch?v=Y4T3Y5wHixc |
| 10 | How Git and Cursor sync code | Merkle trees explained (Cursor + Git by Ben Dicken) | 9 min | https://www.youtube.com/watch?v=86Elcm_6X_Y |
| 11 | Turbopuffer architecture (CEO interview) | Vector DB on object storage | 65 min | https://www.audible.in/podcast/Building-serverless-vector-search-with-Turbopuffer-CEO-Simon-Eskildsen/B0G27BLQZV |
| 12 | Inference Engineering (The infrastructure of AI) | Philip Kiely + Ben Dicken on inference at scale | 60 min | https://www.youtube.com/watch?v=N_Nqlt8Z8kg |

### Optional Deep Dives

| Resource | Topic | Time | Link |
|----------|-------|------|------|
| CocoIndex (open-source) | Live codebase indexing for RAG with incremental updates | 25 min | https://www.youtube.com/watch?v=G3WstvhHO24 |

After Chapter 6: Production agent architecture, evaluation, and orchestration platforms. The Pragmatic Engineer article provides a complete mental model of how Cursor works at scale.

---

## Chapter 7: MCP -- The Universal Tool Standard

Model Context Protocol (MCP) is the USB-C for AI tools -- one protocol that works across Claude, Cursor, and any MCP-compatible agent.

| # | Resource | Topic | Time | Link |
| --- | --- | --- | --- | --- |
| 1 | MCP Explained for Beginners (KodeKloud) | What is MCP? plus flight booking demo | 30 min | https://www.youtube.com/watch?v=E2DEHOEbzks |
| 2 | What is MCP? (conceptual deep dive) | Protocol overview | 20 min | https://www.youtube.com/watch?v=FsMVyP5-ujM |
| 3 | MCP Tutorial with TypeScript | Build a basic server | Article | https://github.com/imzodev/mcp-tutorial-ts |
| 4 | Let's Learn MCP with Python (Microsoft) | Complete Python tutorial | Article | https://github.com/microsoft/lets-learn-mcp-python |
| 5 | MCP vs. Function Calling | Why MCP matters | 15 min | https://www.youtube.com/watch?v=OpmSJMM3V6E |

After Chapter 7: How to build MCP servers and connect any agent to any tool.

---

## Chapter 8: Agent Skills and Context Engineering -- Reusable Expertise and the Discipline of Managing What the Model Sees

Skills are folders of instructions, scripts, and resources that agents can discover and load on demand. Context engineering is the broader discipline of designing everything the model sees in its context window -- instructions, examples, data, conversation history, and tool outputs.

| # | Resource | Topic | Time | Link |
| --- | --- | --- | --- | --- |
| 1 | Anthropic Skills announcement | What are Skills? | Article | https://claude.com/blog/equipping-agents-for-the-real-world-with-agent-skills |
| 2 | Agent Skills specification | Open standard docs | Article | https://github.com/agentskills/agentskills |
| 3 | Build a custom Skill (Milvus RAG example) | Hands-on tutorial | Article | https://milvus.io/blog/create-a-custom-anthropic-skill-for-milvus-to-quickly-spin-up-rag.md |
| 4 | Context Engineering: Bringing Engineering Discipline to Prompts (O'Reilly) | Science and art of context design | Article | https://www.oreilly.com/radar/context-engineering-bringing-engineering-discipline-to-prompts-part-2/ |
| 5 | Advanced Context Engineering for AI Agents (GitHub) | Prompt templates: compaction, sub-agents, structured workflows | Article | https://github.com/marcaurelsecond/Advanced-Context-Engineering-for-AI-Agents |
| 6 | ROSES prompting framework (Columbia University) | Role, Objective, Scenario, Expected Solution, Steps | Article | https://etc.cuit.columbia.edu/news/aicop-practical-ai-clear-prompts-useful-context |
| 7 | Skill-depot (RAG for skills) | MCP-based skill management | Article | https://github.com/Ruhal-Doshi/skill-depot |

**What is Context Engineering?**

Prompt engineering focuses on crafting clear instructions inside a single message. Context engineering widens that scope to everything the model sees in its context window: instructions, examples, sources, conversation history, tool outputs, and retrieved data. As Andrej Karpathy described it, context engineering is a delicate mix of science and art.

The science: established techniques like retrieval-augmented generation (RAG), few-shot prompting, chain-of-thought, and respecting the model's context window limits. Too little context and the model guesses. Too much irrelevant context and performance degrades.

The art: intuition about how specific models behave, knowing when to compress long histories into summaries, and developing a feel for prompt structure that works with a given model's quirks.

**Progressive Disclosure (Skills):**

Level 0: Name and description (always in context). The agent sees this constantly.

Level 1: SKILL.md body (loaded when the agent thinks the skill might be relevant).

Level 2: Scripts, templates, and resources (loaded only when the skill explicitly references them).

**Context Rot Warning:**

As conversations grow longer, context quality degrades. Failed attempts and dead-end explorations accumulate in the context window, confusing the model. The fix: regularly summarize and start fresh, or use structured boundaries (like the spec-driven workflow from Chapter 4) to separate current work from historical noise.

After Chapter 8: Reusable agent skills, effective context management across long sessions, and how RAG, MCP, and Skills work together.

---

## The Big Picture: Five Layers of Enterprise AI

- RAG gives LLMs knowledge (retrieval) -- Chapter 1
- MCP gives LLMs tools (standardized access) -- Chapter 7
- Agents give LLMs autonomy (planning plus execution) -- Chapter 3
- Skills give agents structured workflows (reusable expertise) -- Chapter 8
- Context Engineering gives all of them discipline (managing what the model sees) -- Chapter 8

"RAG gives knowledge. MCP gives tools. Agents give autonomy. Skills give structure. Context engineering makes them reliable. The spec-driven workflow from Chapter 4 ties it all together."

---

## Quick Reference: All Links in One Place

### Videos (Must-Watch)

| Resource | Link |
| --- | --- |
| Intro to Large Language Models | https://www.youtube.com/watch?v=zjkBMFhNj_g |
| But what is a Neural Network? (3Blue1Brown) | https://www.youtube.com/watch?v=aircAruvnKk |
| Gradient Descent (3Blue1Brown) | https://www.youtube.com/watch?v=IHZwWFHWa-w |
| Backpropagation (3Blue1Brown) | https://www.youtube.com/watch?v=Ilg3gGewQ5U |
| Statistical Regression in 40 mins | https://www.youtube.com/watch?v=eYTumjgE2IY |
| Stanford CS224N Lecture 1 | https://www.youtube.com/watch?v=DzpHeXVSC5I |
| Introduction to Neural Networks and Deep Learning | https://www.youtube.com/watch?v=kyQ0CRkYhy4 |
| RNNs intuitively explained | https://www.youtube.com/watch?v=8HyCNCN4t-k |
| The Attention Mechanism (illustrated) | https://www.youtube.com/watch?v=YAgjHMRmeR4 |
| Transformers Explained Visually | https://www.youtube.com/watch?v=TQQlZhbC5iQ |
| Andrej Karpathy -- Let's build GPT | https://www.youtube.com/watch?v=kCc8FmEb1nY |
| Attention is All You Need (paper explained) | https://www.youtube.com/watch?v=ZXuidhZKSGk |
| Complete RAG Tutorial 2026 (KodeKloud) | https://www.youtube.com/watch?v=vT-DpLvf29Q |
| Lecture 7: Agentic Coding (Missing Semester) | https://www.youtube.com/watch?v=sTdz6PZoAnw |
| AI Agents for Beginners (KodeKloud) | https://www.youtube.com/watch?v=MZhjki7t6p8 |
| Claude Code Essentials (KodeKloud short version) | https://www.youtube.com/watch?v=brLhhkUqcn4 |
| Spec-Driven Development Workshop | https://www.youtube.com/live/inKOU-ltbFc |
| Stanford CS 153: Cursor CTO | https://www.youtube.com/watch?v=4jDQi9P9UIw |
| Coding Evals -- Naman Jain (Cursor) | https://www.youtube.com/watch?v=tHN44yJoeS8 |
| Cursor and WarpStream | https://www.youtube.com/watch?v=WGkadWLPORs |
| MCP Explained for Beginners (KodeKloud) | https://www.youtube.com/watch?v=E2DEHOEbzks |

### Articles (Must-Read)

| Resource | Link |
| --- | --- |
| Real-world engineering challenges: building Cursor (Pragmatic Engineer) | https://newsletter.pragmaticengineer.com/p/cursor |
| OpenCode: Free and Local LLMs | https://www.infralovers.com/blog/2026-02-27-opencode-free-local-llms/ |
| Harness Engineering | https://www.infralovers.com/blog/2026-03-13-harness-engineering-rahmen-wichtiger-als-modell/ |
| Sandboxing Claude Code on macOS | https://www.infralovers.com/blog/2026-02-15-sandboxing-claude-code-macos/ |
| watsonx Orchestrate: Agentic AI Platform | https://www.infralovers.com/blog/2026-03-23-ibm-watsonx-orchestrate/ |
| Building with watsonx Orchestrate ADK | https://www.infralovers.com/blog/2026-04-20-building-with-watsonx-orchestrate/ |
| wxO vs. n8n workflow comparison | https://www.infralovers.com/blog/2026-04-13-wxo-n8n-workflow/ |
| Quantization Explained | https://www.sitepoint.com/quantization-explained-q4km-vs-awq-vs-fp16-for-local-llms/ |
| Context Engineering (O'Reilly) | https://www.oreilly.com/radar/context-engineering-bringing-engineering-discipline-to-prompts-part-2/ |
| ROSES Prompting Framework (Columbia) | https://etc.cuit.columbia.edu/news/aicop-practical-ai-clear-prompts-useful-context |

### GitHub Repositories

https://github.com/agentskills/agentskills
https://github.com/imzodev/mcp-tutorial-ts
https://github.com/microsoft/lets-learn-mcp-python
https://github.com/Ruhal-Doshi/skill-depot

### Optional Deep Dives

| Resource | Link |
| --- | --- |
| Claude Code Deep Dive (Andrew Brown / freeCodeCamp) - 12 hours | https://www.youtube.com/watch?v=brLhhkUqcn4 |
| Turbopuffer CEO interview | https://www.audible.in/podcast/Building-serverless-vector-search-with-Turbopuffer-CEO-Simon-Eskildsen/B0G27BLQZV |
| Cursor's multi-agent architecture | https://cursor.com/blog/scaling-agents |
| Anthropic Agent Teams | https://code.claude.com/docs/en/agent-teams |
| Anthropic Skills announcement | https://claude.com/blog/equipping-agents-for-the-real-world-with-agent-skills |
| Build a custom Skill (Milvus) | https://milvus.io/blog/create-a-custom-anthropic-skill-for-milvus-to-quickly-spin-up-rag.md |

---

## How to Use This Path

- Go in order -- Each chapter builds on the previous one.
- Do the hands-on labs -- The KodeKloud videos include free sandboxes.
- Run local LLMs -- After Chapter 3, install Ollama and experiment with quantized models.
- Build something -- Use Chapter 8 to create an agent skill.
- Watch the Spec-Driven Development Workshop in Chapter 4 -- It ties harness engineering and security together into a practical workflow.
- Refer back -- The Pragmatic Engineer article on Cursor in Chapter 6 connects all the concepts to a real production system.

---

## One-Line Summary of Each Chapter

- Chapter 1: Neural network fundamentals, embeddings, and RAG pipelines.
- Chapter 2: How transformers work and how to build a small GPT.
- Chapter 3: Quantized local LLMs, memory/quality trade-offs, and basic coding agents.
- Chapter 4: Why agent structure matters more than the model, with a spec-driven workshop that brings engineering discipline to agent workflows.
- Chapter 5: Safe agent execution without permission prompts, with security designed into the workflow.
- Chapter 6: How Cursor and enterprise orchestrators work in production (includes the Pragmatic Engineer deep dive).
- Chapter 7: How MCP gives agents universal tool access
- Chapter 8: How Skills and context engineering give agents reusable workflows and disciplined context management.
# AI Inner Workings: From Neural Networks to Agents, Tools, Protocols and Production Systems

Free university lectures, engineering workshops, and industry deep dives on how modern AI systems actually work under the hood.

## Table of Contents

1. Chapter 1: Foundations of Neural Learning
2. Chapter 2: From Embeddings to Transformers
3. Chapter 3: LLM Engineering (RAG, Vector DBs, Prompting, Local LLMs, Quantization)
4. Chapter 4: Harness Engineering
5. Chapter 5: Sandboxing and Security
6. Chapter 6: Orchestration and Workflows
7. Chapter 7: MCP -- The Universal Tool Standard
8. Chapter 8: Agent Skills and Context Engineering
9. Chapter 9: Case Study – SSD Offloading for Massive Models (oLLM)

---

## Chapter 1: Foundations of Neural Learning

From neurons to word vectors, plus hands-on RAG.

| # | Resource | Author/Source | Topic | Time | Link | Done? | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Intro to Large Language Models [1hr Talk] | Andrej Karpathy | First 20 min only (motivation) | 20 min | https://www.youtube.com/watch?v=zjkBMFhNj_g | ✓ | [notes/ch1/01_intro_llms_motivation.md](notes/ch1/01_intro_llms_motivation.md) |
| 2 | But what is a Neural Network? | 3Blue1Brown | Visual intuition | 20 min | https://www.youtube.com/watch?v=aircAruvnKk | ✓ | [notes/ch1/02_neural_network.md](notes/ch1/02_neural_network.md) |
| 3 | Gradient Descent, Step by Step | 3Blue1Brown | Learning process | 21 min | https://www.youtube.com/watch?v=IHZwWFHWa-w | ◐ | [notes/ch1/03_gradient_descent.md](notes/ch1/03_gradient_descent.md) |
| 4 | What is Backpropagation? | 3Blue1Brown | The math | 14 min | https://www.youtube.com/watch?v=Ilg3gGewQ5U | ✗ | [notes/ch1/04_backpropagation.md](notes/ch1/04_backpropagation.md) |
| 5 | Learn Statistical Regression in 40 mins! | zedstatistics (YouTube) | Foundation | 40 min | https://www.youtube.com/watch?v=eYTumjgE2IY | | [notes/ch1/05_statistical_regression.md](notes/ch1/05_statistical_regression.md) |
| 6 | Stanford CS224N Lecture 1 | Stanford / Christopher Manning | Word embeddings (first 35 min) | 35 min | https://www.youtube.com/watch?v=DzpHeXVSC5I | | [notes/ch1/06_word_embeddings_cs224n.md](notes/ch1/06_word_embeddings_cs224n.md) |
| 7 | Introduction to Neural Networks and Deep Learning | MIT (YouTube) | Applied deep learning | 90 min | https://www.youtube.com/watch?v=kyQ0CRkYhy4 | | [notes/ch1/07_mit_deep_learning_intro.md](notes/ch1/07_mit_deep_learning_intro.md) |
| 8 | Intro to Large Language Models [1hr Talk] | Andrej Karpathy | Remaining 40 min (capstone) | 40 min | https://www.youtube.com/watch?v=zjkBMFhNj_g | | [notes/ch1/08_intro_llms_capstone.md](notes/ch1/08_intro_llms_capstone.md) |

**After Chapter 1:** Neural network fundamentals, embeddings, and a complete understanding of how LLMs work.

---

## Chapter 2: From Embeddings to Transformers

The architecture behind modern AI.

| # | Resource | Topic | Time | Link | Done | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | RNNs intuitively explained | Sequential data | 15 min | https://www.youtube.com/watch?v=8HyCNCN4t-k | | [notes/ch2/01_rnns_explained.md](notes/ch2/01_rnns_explained.md) |
| 2 | The Attention Mechanism (illustrated) | Key innovation | 20 min | https://www.youtube.com/watch?v=YAgjHMRmeR4 | | [notes/ch2/02_attention_mechanism.md](notes/ch2/02_attention_mechanism.md) |
| 3 | Transformers Explained Visually | Attention without recurrence | 25 min | https://www.youtube.com/watch?v=TQQlZhbC5iQ | | [notes/ch2/03_transformers_visually.md](notes/ch2/03_transformers_visually.md) |
| 4 | Andrej Karpathy -- Let's build GPT | Hands-on transformer (first 45 min) | 45 min | https://www.youtube.com/watch?v=kCc8FmEb1nY | | [notes/ch2/04_build_gpt_karpathy.md](notes/ch2/04_build_gpt_karpathy.md) |
| 5 | Attention is All You Need (paper explained) | Yannic Kilcher | 35 min | https://www.youtube.com/watch?v=ZXuidhZKSGk | | [notes/ch2/05_attention_paper_explained.md](notes/ch2/05_attention_paper_explained.md) |

**After Chapter 2:** How transformers work and how to build a small GPT.

---

## Chapter 3: LLM Engineering (RAG, Vector DBs, Prompting, Local LLMs, Quantization)

Hands-on building with LLMs: RAG pipelines, vector databases, prompt engineering, function calling, quantization (including TurboQuant), and running models on consumer hardware.

| # | Resource | Author/Source | Topic | Time | Priority | Link | Done | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Complete RAG Tutorial 2026 (Free Labs) | KodeKloud | Hands-on RAG with vector DBs | 60 min | Must | https://www.youtube.com/watch?v=vT-DpLvf29Q | | [notes/ch3/01_rag_tutorial_kodekloud.md](notes/ch3/01_rag_tutorial_kodekloud.md) |
| 2 | Lecture 7: Agentic Coding | Missing Semester (MIT) | What are agents? (conceptual) | 60 min | Must | https://www.youtube.com/watch?v=sTdz6PZoAnw | | [notes/ch3/02_agentic_coding_mit.md](notes/ch3/02_agentic_coding_mit.md) |
| 3 | AI Agents for Beginners -- Part 1 | KodeKloud | Hands-on: API calls, tools, workflows vs. agents | 60 min | Must | https://www.youtube.com/watch?v=MZhjki7t6p8 | | [notes/ch3/03_ai_agents_beginners.md](notes/ch3/03_ai_agents_beginners.md) |
| 4 | Claude Code Essentials (short) | KodeKloud | Practical coding agent usage | 9 min | Must | https://www.youtube.com/watch?v=brLhhkUqcn4 | | [notes/ch3/04_claude_code_essentials.md](notes/ch3/04_claude_code_essentials.md) |
| 5 | LLM function calling explained | YouTube | How agents decide actions | 15 min | Must | https://www.youtube.com/watch?v=Gz1F6iGPH2s | | [notes/ch3/05_function_calling.md](notes/ch3/05_function_calling.md) |
| 6 | OpenCode: Free and Local LLMs | Infralovers | Using Ollama, local models | Article | Must | https://www.infralovers.com/blog/2026-02-27-opencode-free-local-llms/ | | [notes/ch3/06_opencode_local_llms.md](notes/ch3/06_opencode_local_llms.md) |
| 7 | Quantization Explained | SitePoint | 4-bit vs FP16 memory trade-offs | Article | Must | https://www.sitepoint.com/quantization-explained-q4km-vs-awq-vs-fp16-for-local-llms/ | | [notes/ch3/07_quantization_explained.md](notes/ch3/07_quantization_explained.md) |
| 8 | Ollama tutorial (run Llama 3 locally) | YouTube | Hands-on local LLMs | 15 min | Must | https://www.youtube.com/watch?v=WxYC9-hBM_g | | [notes/ch3/08_ollama_tutorial.md](notes/ch3/08_ollama_tutorial.md) |
| 9 | Build a code agent from scratch | YouTube | Hands-on open code | 60 min | Must | https://www.youtube.com/watch?v=8fFH5e4WnPA | | [notes/ch3/09_code_agent_from_scratch.md](notes/ch3/09_code_agent_from_scratch.md) |
| **10** | **TurboQuant Explained (Primer)** | **Caleb Writes Code** | **What TurboQuant solves, KV cache intuition, vector quantization basics** | **11 min** | **Must** | **https://www.youtube.com/watch?v=7V0Vt2QzMDk** | | **[notes/ch3/10_turboquant_primer.md](notes/ch3/10_turboquant_primer.md)** |
| **11** | **TurboQuant Interactive Demo** | **Arkaung** | **Complete deep dive: random rotation, Lloyd-Max codebook, MSE vs inner product** | **30-45 min** | **Must** | **https://arkaung.github.io/interactive-turboquant/** | | **[notes/ch3/11_turboquant_interactive.md](notes/ch3/11_turboquant_interactive.md)** |
| **12** | **TurboQuant Reality Check** | **Soul Care / Two Minute Papers** | **Critical analysis of Google's claims, real-world impact** | **~15 min** | **Optional** | **https://www.youtube.com/watch?v=haoAI2lIZ74** | | **[notes/ch3/12_turboquant_reality_check.md](notes/ch3/12_turboquant_reality_check.md)** |

**Quantization Deep Dive:**

*Traditional 4-bit quantization (Q4_K_M, AWQ)* reduces each weight to 4 bits independently. Simple, effective, 1-3% quality loss.

**TurboQuant** uses *vector quantization*: groups of weights are quantized together as vectors, preserving more of the high-dimensional structure. The interactive demo shows how random rotation + Lloyd-Max codebook generation beats scalar quantization.

**KV Cache Quantization (TurboQuant's real win):** During inference, the KV cache grows with sequence length. TurboQuant can compress it aggressively (2-3 bits) because the cache has different statistical properties than model weights.

**Reality check (per the optional critique):** Google's reported "10x compression" claims deserve skepticism. The real value is in KV cache compression for long contexts, not replacing weight quantization entirely.

**After Chapter 3:** RAG pipelines, vector databases, prompt engineering, function calling, quantized local LLMs (FP16 vs 4-bit vs TurboQuant), memory/quality trade-offs, and basic coding agents.

---

## Chapter 4: Harness Engineering -- Why Structure Matters More Than the Model

| # | Resource | Author/Source | Topic | Time | Link | Done | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Harness Engineering article | Infralovers | Why structure > model (METR, DORA, Planner-Worker). Includes verifiability levels (formal to testable to heuristic). | Article | https://www.infralovers.com/blog/2026-03-13-harness-engineering-rahmen-wichtiger-als-modell/ | | [notes/ch4/01_harness_engineering.md](notes/ch4/01_harness_engineering.md) |
| 2 | Multi-agent systems vs. single-agent loops | YouTube | Planner-Worker patterns | 15 min | https://www.youtube.com/watch?v=8w9Nng35E0U | | [notes/ch4/02_multi_agent_systems.md](notes/ch4/02_multi_agent_systems.md) |
| 3 | Cursor's multi-agent architecture | Cursor Blog | Real-world example | Article | https://cursor.com/blog/scaling-agents | | [notes/ch4/03_cursor_multi_agent.md](notes/ch4/03_cursor_multi_agent.md) |
| 4 | Anthropic Agent Teams | Anthropic Docs | Lead + Teammates pattern | Article | https://code.claude.com/docs/en/agent-teams | | [notes/ch4/04_anthropic_agent_teams.md](notes/ch4/04_anthropic_agent_teams.md) |
| 5 | Spec-Driven Development Workshop | Unlearn | Write structured specs, refine prompts, stop agents from guessing wrong | 120 min | https://www.youtube.com/live/inKOU-ltbFc | | [notes/ch4/05_spec_driven_development.md](notes/ch4/05_spec_driven_development.md) |

**After Chapter 4:** Why agent architecture matters more than model choice, how multi-agent systems are structured, and how spec-driven development brings engineering discipline to agent workflows.

---

## Chapter 5: Sandboxing and Security -- Letting Agents Run Free Safely

Most sandboxes focus on preventing writes. Reading SSH keys plus network access equals instant exfiltration. The spec-driven workflow from Chapter 4 defines security boundaries at the planning stage.

| # | Resource | Author/Source | Topic | Time | Link | Done | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Sandboxing Claude Code on macOS article | Infralovers | Security fundamentals, comparison of Docker Sandboxes, Lima, Tart, read vs. write access risks | Article | https://www.infralovers.com/blog/2026-02-15-sandboxing-claude-code-macos/ | | [notes/ch5/01_sandboxing_claude_code.md](notes/ch5/01_sandboxing_claude_code.md) |
| 2 | Docker Sandboxes Documentation | Docker Docs | MicroVM isolation, private Docker daemon per sandbox, workspace syncing, network policies, supported agents (Claude Code, Codex, Gemini, OpenCode) | Article | https://docs.docker.com/ai/sandboxes/ | | [notes/ch5/02_docker_sandboxes.md](notes/ch5/02_docker_sandboxes.md) |
| 3 | Lima | Lima GitHub | Open-source macOS Linux VMs, Virtualization.framework | Article | https://github.com/lima-vm/lima | | [notes/ch5/03_lima_vm.md](notes/ch5/03_lima_vm.md) |
| 4 | Tart | Tart GitHub | CI-focused sandboxing, OCI images, Softnet network filtering | Article | https://github.com/cirruslabs/tart | | [notes/ch5/04_tart_sandboxing.md](notes/ch5/04_tart_sandboxing.md) |
| **5** | **AgentSight: System-Level Observability for AI Agents Using eBPF** | **Zheng et al. (UCSC)** | **Bridges semantic gap between agent intent and system actions. Detects prompt injection, infinite loops, multi-agent bottlenecks with <3% overhead.** | **Paper** | **https://arxiv.org/pdf/2508.02736** | | **[notes/ch5/05_agentsight_ebpf.md](notes/ch5/05_agentsight_ebpf.md)** |

**After Chapter 5:** Safe agent execution with --dangerously-skip-permissions inside proper isolation, understanding of Docker Sandboxes microVM architecture, security designed into the workflow, and **eBPF-based observability** to see every syscall an agent makes in real-time.

---

## Chapter 6: Orchestration and Workflows -- From Agents to Enterprise Systems

watsonx Orchestrate and n8n: agentic AI vs. workflow engines converging. Includes the definitive Cursor architecture deep dive.

| # | Resource | Topic | Time | Link | Done | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Real-world engineering challenges: building Cursor (Pragmatic Engineer) | Complete Cursor architecture: tech stack, autocomplete, Merkle trees, Anyrun orchestrator | Article | https://newsletter.pragmaticengineer.com/p/cursor | | [notes/ch6/01_cursor_pragmatic_engineer.md](notes/ch6/01_cursor_pragmatic_engineer.md) |
| 2 | Stanford CS 153: Cursor CTO and Co-Founder Sualeh Asif | Production infrastructure, indexing, orchestrator (video) | 60 min | https://www.youtube.com/watch?v=4jDQi9P9UIw | | [notes/ch6/02_cursor_cto_stanford.md](notes/ch6/02_cursor_cto_stanford.md) |
| 3 | Coding Evals: From Code Snippets to Codebases -- Naman Jain (Cursor) | SWE-bench, test hacking, human preference evals | 60 min | https://www.youtube.com/watch?v=tHN44yJoeS8 | | [notes/ch6/03_coding_evals_cursor.md](notes/ch6/03_coding_evals_cursor.md) |
| 4 | The Future of Coding: Cursor and WarpStream | Streaming data at scale | 45 min | https://www.youtube.com/watch?v=WGkadWLPORs | | [notes/ch6/04_cursor_warpstream.md](notes/ch6/04_cursor_warpstream.md) |
| 5 | watsonx Orchestrate: Agentic AI Platform article | Agents, tools, knowledge, Langfuse | Article | https://www.infralovers.com/blog/2026-03-23-ibm-watsonx-orchestrate/ | | [notes/ch6/05_watsonx_orchestrate.md](notes/ch6/05_watsonx_orchestrate.md) |
| 6 | Building with watsonx Orchestrate ADK article | YAML agents, Python tools, local dev | Article | https://www.infralovers.com/blog/2026-04-20-building-with-watsonx-orchestrate/ | | [notes/ch6/06_watsonx_adk.md](notes/ch6/06_watsonx_adk.md) |
| 7 | wxO vs. n8n workflow comparison article | Agentic vs. deterministic | Article | https://www.infralovers.com/blog/2026-04-13-wxo-n8n-workflow/ | | [notes/ch6/07_wxo_vs_n8n.md](notes/ch6/07_wxo_vs_n8n.md) |
| 8 | How Cursor searches your code (Vector search) | Semantic search with vector embeddings | 20 min | https://www.youtube.com/watch?v=wpVgA1fisz8 | | [notes/ch6/08_cursor_vector_search.md](notes/ch6/08_cursor_vector_search.md) |
| 9 | Merkle trees in 5 minutes | How Cursor avoids re-indexing (generic) | 10 min | https://www.youtube.com/watch?v=Y4T3Y5wHixc | | [notes/ch6/09_merkle_trees.md](notes/ch6/09_merkle_trees.md) |
| 10 | How Git and Cursor sync code | Merkle trees explained (Cursor + Git by Ben Dicken) | 9 min | https://www.youtube.com/watch?v=86Elcm_6X_Y | | [notes/ch6/10_git_cursor_merkle.md](notes/ch6/10_git_cursor_merkle.md) |
| 11 | Turbopuffer architecture (CEO interview) | Vector DB on object storage | 65 min | https://www.audible.in/podcast/Building-serverless-vector-search-with-Turbopuffer-CEO-Simon-Eskildsen/B0G27BLQZV | | [notes/ch6/11_turbopuffer_architecture.md](notes/ch6/11_turbopuffer_architecture.md) |

### Optional Deep Dives

| Resource | Topic | Time | Link | Done | Notes |
|----------|-------|------|------| --- | --- |
| CocoIndex (open-source) | Live codebase indexing for RAG with incremental updates | 25 min | https://www.youtube.com/watch?v=G3WstvhHO24 | | [notes/ch6/optional_cocoindex.md](notes/ch6/optional_cocoindex.md) |
| Claude Code Deep Dive (Andrew Brown / freeCodeCamp) | Comprehensive 12-hour course | 12 hours | https://www.youtube.com/watch?v=brLhhkUqcn4 | | [notes/ch6/optional_claude_code_deep_dive.md](notes/ch6/optional_claude_code_deep_dive.md) |

**After Chapter 6:** Production agent architecture, evaluation, and orchestration platforms. The Pragmatic Engineer article provides a complete mental model of how Cursor works at scale.

> Maybe later add something on LangGraph or PydanticAI.

---

## Chapter 7: MCP -- The Universal Tool Standard

Model Context Protocol (MCP) is the USB-C for AI tools -- one protocol that works across Claude, Cursor, and any MCP-compatible agent.

| # | Resource | Topic | Time | Link | Done | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | MCP Explained for Beginners (KodeKloud) | What is MCP? plus flight booking demo | 30 min | https://www.youtube.com/watch?v=E2DEHOEbzks | | [notes/ch7/01_mcp_beginners.md](notes/ch7/01_mcp_beginners.md) |
| 2 | What is MCP? (conceptual deep dive) | Protocol overview | 20 min | https://www.youtube.com/watch?v=FsMVyP5-ujM | | [notes/ch7/02_mcp_conceptual.md](notes/ch7/02_mcp_conceptual.md) |
| 3 | MCP Tutorial with TypeScript | Build a basic server | Article | https://github.com/imzodev/mcp-tutorial-ts | | [notes/ch7/03_mcp_typescript_tutorial.md](notes/ch7/03_mcp_typescript_tutorial.md) |
| 4 | Let's Learn MCP with Python (Microsoft) | Complete Python tutorial | Article | https://github.com/microsoft/lets-learn-mcp-python | | [notes/ch7/04_mcp_python_tutorial.md](notes/ch7/04_mcp_python_tutorial.md) |
| 5 | MCP vs. Function Calling | Why MCP matters | 15 min | https://www.youtube.com/watch?v=OpmSJMM3V6E | | [notes/ch7/05_mcp_vs_function_calling.md](notes/ch7/05_mcp_vs_function_calling.md) |

**After Chapter 7:** How to build MCP servers and connect any agent to any tool.

---

## Chapter 8: Agent Skills and Context Engineering -- Reusable Expertise and the Discipline of Managing What the Model Sees

Skills are folders of instructions, scripts, and resources that agents can discover and load on demand. Context engineering is the broader discipline of designing everything the model sees in its context window -- instructions, examples, data, conversation history, and tool outputs.

| # | Resource | Topic | Time | Link | Done | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Anthropic Skills announcement | What are Skills? | Article | https://claude.com/blog/equipping-agents-for-the-real-world-with-agent-skills | | [notes/ch8/01_anthropic_skills.md](notes/ch8/01_anthropic_skills.md) |
| 2 | Agent Skills specification | Open standard docs | Article | https://github.com/agentskills/agentskills | | [notes/ch8/02_agent_skills_spec.md](notes/ch8/02_agent_skills_spec.md) |
| 3 | Build a custom Skill (Milvus RAG example) | Hands-on tutorial | Article | https://milvus.io/blog/create-a-custom-anthropic-skill-for-milvus-to-quickly-spin-up-rag.md | | [notes/ch8/03_custom_skill_milvus.md](notes/ch8/03_custom_skill_milvus.md) |
| 4 | Context Engineering: Bringing Engineering Discipline to Prompts (O'Reilly) | Science and art of context design | Article | https://www.oreilly.com/radar/context-engineering-bringing-engineering-discipline-to-prompts-part-2/ | | [notes/ch8/04_context_engineering_oreilly.md](notes/ch8/04_context_engineering_oreilly.md) |
| 5 | Advanced Context Engineering for AI Agents (GitHub) | Prompt templates: compaction, sub-agents, structured workflows | Article | https://github.com/marcaurelsecond/Advanced-Context-Engineering-for-AI-Agents | | [notes/ch8/05_advanced_context_engineering.md](notes/ch8/05_advanced_context_engineering.md) |
| 6 | ROSES prompting framework (Columbia University) | Role, Objective, Scenario, Expected Solution, Steps | Article | https://etc.cuit.columbia.edu/news/aicop-practical-ai-clear-prompts-useful-context | | [notes/ch8/06_roses_prompting.md](notes/ch8/06_roses_prompting.md) |
| 7 | Skill-depot (RAG for skills) | MCP-based skill management | Article | https://github.com/Ruhal-Doshi/skill-depot | | [notes/ch8/07_skill_depot.md](notes/ch8/07_skill_depot.md) |

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

**After Chapter 8:** Reusable agent skills, effective context management across long sessions, and how RAG, MCP, and Skills work together.

---

## Chapter 9: Case Study – SSD Offloading for Massive Models (oLLM)

Quantization (Chapter 3) trades quality for memory. SSD offloading trades *speed* for memory while preserving full precision. oLLM runs an 80B model on 8GB VRAM at ~0.5 tokens/second.

**How it works:** Layer weights load from SSD → GPU one at a time. KV cache writes to SSD, loads back when needed. FlashAttention-2 avoids materializing the full attention matrix. Chunked MLP splits large intermediate computations.

| # | Resource | Topic | Time | Link | Done | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | vLLM: PagedAttention (blog) | Understanding KV cache management. Read first half. | 20 min | https://blog.vllm.ai/2023/06/20/vllm.html | | [notes/ch9/01_vllm_paged_attention.md](notes/ch9/01_vllm_paged_attention.md) |
| 2 | Inference Engineering (The infrastructure of AI) | Philip Kiely + Ben Dicken on inference at scale. Prerequisite before oLLM. | 60 min | https://www.youtube.com/watch?v=N_Nqlt8Z8kg | | [notes/ch9/02_inference_engineering.md](notes/ch9/02_inference_engineering.md) |
| 3 | oLLM GitHub | Full-precision 80B model on 8GB VRAM via SSD offloading. | Article | https://github.com/Mega4alik/ollm | | [notes/ch9/03_ollm_ssd_offloading.md](notes/ch9/03_ollm_ssd_offloading.md) |

**Checkpoint:** Explain the difference between PagedAttention (vLLM) and SSD offloading (oLLM).

**After Chapter 9:** Understanding of alternative memory optimization strategies beyond quantization, and when to apply each.

---

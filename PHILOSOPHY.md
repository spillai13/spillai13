# How I Build with AI

---

## What to Build (The Product)

The hardest part of building isn't the build — it's knowing which problem is worth solving.

**Building forces clarity that thinking alone doesn't.**
Every project requires making assumptions explicit — what does good look like, which tradeoffs matter, where AI helps vs. misleads. That accumulates into judgment you can't get any other way.

**Good decisions are rarely a single moment.**
They're the result of deep thinking, translating an observation into a hypothesis, testing it against reality, and iterating. Most tools deliver an answer. The ones worth building support the full cycle — from a messy observation to a confident, well-reasoned action.

**People rarely ask for the right thing.**
They ask for relief from a symptom. The real problem is usually one layer deeper — a workaround everyone has stopped questioning, a spreadsheet doing the job of a system. That gap between what exists and what should exist is where the problem worth solving lives.

**Style (The Un-Promptable Quality)**
Unconstrained, AI produces generic output. Enforcing style requires opinionated design systems and strict component libraries — forcing the AI to build with your blocks, not invent its own.

**The Feedback Loop (Speed is Oxygen)**
Idea → Prompt → Render → Critique must complete in under 10 seconds. Hot-reload and instant previews are not nice-to-haves; they are the conditions under which this workflow functions.

---

## How to Build (The Engine)

The goal is an AI that has enough context to act autonomously, but enough constraint to avoid hallucinating the codebase into a corner.

**Model Selection**
Route by task: long-context models for architecture-level reasoning, faster/cheaper models for pattern completion. Cost and latency are engineering constraints, not afterthoughts.

**Guardrails & Safety**
Filter inputs at the boundary. Enforce guardrails at the API layer. Validate outputs with Golden Datasets and automated evals. Data masking ensures PII never reaches the LLM.

**App Architecture**
RAG over the codebase, prompt chaining, and tool integration. The retrieval layer is load-bearing — garbage context produces garbage output.

**The Knowledge Graph (`lat.md`)**
LLMs understand Markdown better than raw directory structures. A living `ARCHITECTURE.md` or `lat.md` that maps service relationships, data models, and business logic gives the AI a navigable map of the codebase. Treat it as executable context: inject relevant sections dynamically based on the files currently in scope.

**Agent Skills (Beyond Autocomplete)**
The AI needs hands. Shift from chat to agents with tool-calling: AST parsing, targeted file reads, terminal execution. The agent should read the error, run the grep, and propose the fix — not guess blindly.

**Context & Prompt Engineering**
Context window pollution kills productivity. Separate the system prompt (architecture invariants) from the task prompt (the immediate feature). Use RAG to pull only relevant interfaces and functions — just-in-time, not just-in-case.

**Evals for Generative Output**
Three tiers:
- Deterministic: unit and integration tests
- Heuristic: linting and static analysis
- LLM-as-Judge: a separate prompt that asks whether the output conforms to the style guide in `lat.md`

---

## Forward

**1. The Observer Pattern (Intent Capture)**
The Context Cliff — where the AI forgets why a decision was made three sessions ago — is the biggest risk in long-running projects. An automated Librarian agent watches Git diffs and chat history to keep `lat.md` in sync with the actual state of the code, preserving intent, not just state.

**2. State Hydration & Checkpoints**
Agents fail when they start with a blank slate or irrelevant noise. A Router should hydrate context before each task: pull only the necessary nodes from the knowledge graph and the last N relevant commits. Conceptually: `git checkout` for context.

**3. The Shadow Evaluator (Runtime Guardrails)**
A background critic agent that doesn't write code — it evaluates the primary agent's output against security protocols and architecture constraints in real-time, preventing accidental key exposure or structural violations.

**4. Multi-Modal Input (Omni-Channel Steering)**
The IDE is not the only input surface. A voice memo on Telegram, transcribed and analyzed against the knowledge graph, should produce a prioritized ticket for the tech agent to execute in VS Code. The loop extends beyond the editor.

**5. Deterministic Routing (The Orchestrator)**
Not every prompt warrants a full knowledge graph lookup. A Router classifies and dispatches:
- Low stakes: simple completion → local model
- Medium stakes: feature implementation → Claude/Gemini + RAG
- High stakes: core architecture refactor → long-context model + full graph injection

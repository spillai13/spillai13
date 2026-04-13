# How and What I Build

---

## What I Build (The Product)

Once you've identified the right problem, the next question is whether you understand it well enough to build for it. Most failed tools aren't badly built — they're built for a problem the builder didn't fully understand.

The discipline is staying close to the decision the user is trying to make, not the feature they asked for. That requires restraint: fewer features, tighter scope, and a willingness to throw away a build when the original problem turns out to be the wrong one.

---

## How I Build (The Engine)

**The Knowledge Graph**
LLMs are only as useful as the context they're given. A living map of the project — service relationships, data models, key decisions — gives the AI something to navigate rather than guess. Treat it as executable context: inject only the relevant sections based on what's currently in scope.

**Context & Prompt Engineering**
What goes into the prompt determines what comes out. Separate the stable context (architecture, constraints) from the task-specific prompt (the immediate feature). Pull only what's relevant, just in time — not everything, just in case.

**Guardrails & Safety**
Right now I work primarily with public datasets, so safety is mostly about output quality — catching hallucinations, validating assumptions, not trusting generated code blindly. As the work scales into more sensitive data, the intent is to build proper guardrails: input filtering, output validation, and clear boundaries on what the model is and isn't allowed to do.

**Model Selection**
Not every task needs the most powerful model. Route by complexity: long-context models for architecture-level reasoning, faster and cheaper models for pattern completion. Cost and latency are real constraints, not afterthoughts.

**Agent Skills**
The most useful shift is from chat to agents with tools. An agent that can read a file, run a query, check an error, and propose a fix is categorically more useful than one that guesses. The goal is to give the AI hands, not just a voice.

---

## Forward

**App Architecture**
The patterns that make AI applications production-ready: RAG for grounding outputs in real data, prompt chaining for multi-step reasoning, and tool integration for real-world actions. The retrieval layer is where most of the quality lives — the model is only as good as what you give it.

**Evals**
How do you know if the output is actually good? Three layers: deterministic tests for factual correctness, heuristic checks for structure and style, and LLM-as-Judge for subjective quality — a second model that evaluates whether the output meets the standard set in the knowledge graph.

**The Observer Pattern (Intent Capture)**
The biggest risk in long-running AI projects is the context cliff — where the AI forgets why a decision was made three sessions ago. An automated agent that watches Git diffs and conversation history to keep the knowledge graph in sync with the actual state of the project preserves intent, not just state.

**State Hydration & Checkpoints**
Agents fail when they start with a blank slate or irrelevant noise. Before each task, a router should hydrate context: pull only the necessary nodes from the knowledge graph and the last relevant commits. Conceptually: `git checkout` for context.

**The Shadow Evaluator**
A background critic agent that doesn't write code — it evaluates the primary agent's output against security and architecture constraints in real time, catching structural violations before they compound.

**Multi-Modal Input**
The IDE is not the only input surface. A voice note, transcribed and evaluated against the knowledge graph, should be able to produce a prioritized task for the agent to execute. The loop extends beyond the editor.

**Deterministic Routing**
Not every prompt warrants a full knowledge graph lookup. A router classifies and dispatches by stakes:
- Low: simple completion → local model
- Medium: feature work → Claude/Gemini + RAG
- High: architecture changes → long-context model + full graph

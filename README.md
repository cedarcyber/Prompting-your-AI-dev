# Prompting Techniques for Your AI Developer

This repository details an AI prompting methodology that treats the LLM like an expert software engineer, while you act as a blend of peer programmer, product manager, and QA engineer. It was originally built around chat-based LLMs, but the landscape has shifted — and this guide has evolved with it.

## The New Wave of AI Dev Tools

The days of copy-pasting code between a chat window and your IDE are largely behind us. A new generation of tools has made AI a first-class citizen inside the development environment itself:

| Tool | Type | What makes it different |
|---|---|---|
| **Cursor** | AI-native IDE | Agent mode runs autonomously in your codebase; reads, edits, and runs files |
| **Replit** | Cloud IDE + Agent | Full environment in the browser; AI agent can install deps, run code, deploy |
| **Claude Code** | CLI agent | Terminal-native; understands your whole repo, runs commands, commits code |
| **OpenAI Codex** | Cloud agent | Sandboxed agent that clones your repo and works in isolated environments |
| **GitHub Copilot** | IDE extension + agent | Deep editor integration; Copilot Workspace handles multi-file tasks end-to-end |
| **Windsurf (Codeium)** | AI-native IDE | Cascade agent with persistent context across an entire coding session |

These tools handle many of the manual steps that this workflow originally required — iterating on errors, managing context, re-submitting prompts. **The prompt template still matters**, but how and where you use it has changed.

## Why Prompting Still Matters

Even with agentic tools, a well-crafted prompt remains the difference between a useful result and a hallucinated mess. These tools are powerful, but they are only as good as the intent and context you give them. The methodology here — treating the AI as a skilled engineer you're directing — carries across every tool.

What changes is **where the loop lives**:

- **Old approach**: You submit → AI responds → you copy code → you run it → you paste errors back → repeat manually.
- **New approach**: You submit a well-structured prompt → the agent runs code, reads errors, and self-corrects inside the tool → you review and approve.

## General Workflow

The core flow still applies, adapted for agentic tools:

1. **Write a structured prompt** using the [PromptTemplate](./PromptTemplate) — define your user stories, tech stack, security needs, and deployment target.
2. **Choose your tool** — paste the prompt into Cursor's agent, kick off a Replit Agent session, or run it via Claude Code in your terminal.
3. **Review the architecture** — ask the AI to produce a diagram (MermaidJS works well) before writing code.
4. **Iterate** — in agentic tools the AI self-corrects; your job is to review, redirect, and approve.
5. **Refine the prompt** — as you learn what works, sharpen your template. The prompt is your asset.

See the [AI Dev Interaction Flowchart](./AI%20Dev%20Interaction%20Flowchart) for a visual breakdown of both traditional and agentic workflows.

## Who This Is For

Especially useful if you:
- Have limited coding experience and want AI as an equalizer
- Are moving from chat-based LLM workflows to agentic tools and want a structured approach
- Want a reusable template you can drop into any AI coding tool and get consistent results

Works best with tools that support large context windows and multi-file awareness (Cursor, Claude Code, Codex, Replit Agent).

---

As the tooling evolves, this repo will keep up. Contributions and tweaks welcome.

# Nick Bobrowski

AI engineer in Lisbon. I build agent systems that run in production, and I am the lead maintainer of Agency Swarm.

**[nicko.ai](https://nicko.ai)** · **[LinkedIn](https://www.linkedin.com/in/nicko-ai)**

### Agency Swarm v1: a full rewrite without stranding its users

[VRSEN/agency-swarm](https://github.com/VRSEN/agency-swarm) · 4.5k stars · #1 contributor, 1,600+ commits, 260+ merged pull requests

- **Problem.** The framework ran on OpenAI's Assistants API, which OpenAI replaced with the Responses API and the Agents SDK.
- **Decision.** I rebuilt the core on the Agents SDK and the Responses API, async-first, and kept the orchestrator-and-workers model users already knew. The old v0.7 line kept getting fixes while v1 was in beta, and a migration guide covered the move.
- **Proof.** Six public betas from June to August 2025, then v1.0.0 on 3 September 2025 and 30 stable releases since. Every change to main runs lint, mypy and 1,600+ tests, including live OpenAI and Anthropic calls. Agencii.ai runs on it in production.

> "Since then there haven't been any significant bugs."
>
> Arseny Shatokhin, who started Agency Swarm

### Agent control plane: every coding agent on my machine under one set of rules

My own working system, not a product. Claude, Codex, Kimi and OpenCode all run under it.

- **Mandates.** Each task gets a mandate, and the operating system enforces it as file permissions scoped to that task.
- **One record.** One SQLite database holds every task, escalation and session summary.
- **Human decisions.** When an agent needs a decision or more access, it asks, and the question reaches my screen at the system level.
- **Scale.** Several hundred manager sessions and about 9,000 worker sessions in summer 2026.

### Also shipped

- **[AgentSwarm CLI](https://github.com/VRSEN/agentswarm-cli).** Terminal app for running and testing Agency Swarm projects: a fork of OpenCode wired to the Python core. 580+ commits, 188 merged pull requests.
- **[OpenSwarm](https://github.com/VRSEN/OpenSwarm).** Claude Code for everything except coding: complete deliverables from one prompt. 2.8k stars, core contributor.
- **[Afluento](https://afluento.com).** European Portuguese speaking trainer. Built solo: React and TypeScript front end, FastAPI back end. Live.
- **[Padel Instinct](https://padelinstinct.com).** Padel decision trainer: real points freeze at the moment of decision. Built solo in TypeScript. Live.

### Before agents

A decade of automation and systems integration: Deloitte Consulting (IBM and SAP integrations), Kaspersky (on-premise threat detection and response), Logifuture (multi-tenant gaming backend). Then 30+ enterprise agent deployments at Agency AI Solutions.

**Stack:** Python · FastAPI · PostgreSQL · TypeScript · React · OpenAI Agents SDK · Docker · Kubernetes (CKAD)

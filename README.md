# Nick Bobrowski

AI engineer in Lisbon. I build agent systems that run in production, and I am the lead maintainer of Agency Swarm.

**[nicko.ai](https://nicko.ai)** · **[LinkedIn](https://www.linkedin.com/in/nicko-ai)**

### The Agency Swarm v1 rewrite

[VRSEN/agency-swarm](https://github.com/VRSEN/agency-swarm) · 4.5k stars · #1 contributor, 1,600+ commits, 260+ merged pull requests

- **Problem.** The framework ran on OpenAI's Assistants API, which OpenAI replaced with the Responses API and the Agents SDK.
- **Decision.** I rebuilt the core on the Agents SDK and the Responses API, async-first, and kept the orchestrator-and-workers model users already knew. I kept shipping fixes to the old v0.7 line while v1 was in beta, and we published a migration guide for the move.
- **Proof.** Six public betas ran from June to August 2025. v1.0.0 shipped on 3 September 2025, and 30 stable releases have followed. Every change to main runs lint, mypy and 1,600+ tests, including live OpenAI and Anthropic calls. Agencii.ai runs on it in production.

> "Since then there haven't been any significant bugs."
>
> Arseny Shatokhin, who started Agency Swarm

### My agent control plane

I built it for my own work and have not released it. Claude, Codex, Kimi and OpenCode all run under it.

- **Mandates.** Each task gets a mandate, and the operating system enforces it as file permissions scoped to that task.
- **Records.** One SQLite database holds every task, escalation and session summary.
- **Human decisions.** When an agent needs a decision or more access, it asks, and the question reaches my screen at the system level.
- **Scale.** Several hundred manager sessions and about 9,000 worker sessions in summer 2026.

### Also shipped

- **[AgentSwarm CLI](https://github.com/VRSEN/agentswarm-cli).** Terminal app for running and testing Agency Swarm projects, built as a fork of OpenCode wired to the Python core. 580+ commits, 188 merged pull requests.
- **[OpenSwarm](https://github.com/VRSEN/OpenSwarm).** Claude Code for everything except coding: complete deliverables from one prompt. 2.8k stars, core contributor.
- **[Afluento](https://afluento.com).** European Portuguese speaking trainer, built solo with a React and TypeScript front end and a FastAPI back end. Live.
- **[Padel Instinct](https://padelinstinct.com).** Padel decision trainer, built solo in TypeScript. Real points freeze at the moment of decision, and the player makes the call. Live.

### Before agents

I spent a decade on automation and systems integration at Deloitte Consulting (IBM and SAP integrations), Kaspersky (on-premise threat detection and response) and Logifuture (multi-tenant gaming backend). At Agency AI Solutions I then delivered 30+ enterprise agent projects.

**Stack:** Python · FastAPI · PostgreSQL · TypeScript · React · OpenAI Agents SDK · Docker · Kubernetes (CKAD)

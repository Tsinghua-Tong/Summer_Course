# 04 · Agent Systems & Multi-Agent

## Overview

An **agent** is a system that perceives, decides, and acts to achieve goals; a **multi-agent system
(MAS)** is many such agents interacting — cooperating, competing, or negotiating. This module bridges
two traditions. The classical one studies agents through **reinforcement learning and game theory**:
how a policy is learned, when cooperation emerges, what an equilibrium is. The new one studies
**LLM-based agents**: language models that reason, plan, use tools, and coordinate in teams. We
connect them through shared ideas — planning, theory of mind, and cooperation — and you will build a
tool-using agent yourself.

## Learning Path

**Reinforcement learning & game theory** *(Introductory → Advanced)*
1. [David Silver — Introduction to Reinforcement Learning (DeepMind/UCL)](https://www.davidsilver.uk/teaching/) — the classic RL lecture series. *(Introductory)*
2. [Sutton & Barto, *Reinforcement Learning: An Introduction* (2nd ed., free)](http://incompleteideas.net/book/the-book.html) — the standard text. *(Intermediate)*
3. [UC Berkeley CS285 — Deep RL](https://rail.eecs.berkeley.edu/deeprlcourse/) — deep & multi-agent RL (shared with module 03). *(Advanced)*
4. Game theory — a short course such as [Game Theory (Stanford/Coursera)](https://www.coursera.org/learn/game-theory-1) for Nash equilibria and mechanism design. *(Intermediate)*

**LLM agents** *(Intermediate → Advanced)*
5. Read the LLM-agent literature below (ReAct → WebArena / OSWorld → SWE-agent / tau-bench → Magentic-One) and a
   framework's docs ([AutoGen](https://microsoft.github.io/autogen/) or
   [LangGraph](https://langchain-ai.github.io/langgraph/)).

**Core topics** — study in this order:
- MDPs and single-agent RL recap · policy gradients
- **Multi-agent RL (MARL):** cooperation vs. competition, centralized training / decentralized execution
- **Game theory:** Nash equilibria, the evolution of cooperation
- **LLM agents:** ReAct (reason + act), reflection, planning, **tool/function calling**
- **Multi-agent LLM systems:** role-play, debate, generative agent societies
- **Theory of mind** and emergent communication

## Programming Exercises

1. **Benchmark task analysis.** Read one agent benchmark paper (AgentBench, WebArena, OSWorld, or
   tau-bench), choose 5 released tasks or task descriptions, and write down the goal, observation
   space, available actions/tools, success metric, and likely failure modes.
2. **PettingZoo baseline.** Run one cooperative and one competitive PettingZoo environment, implement
   a random or scripted baseline, log per-agent rewards, and compare cooperation, competition, and
   credit assignment.
3. **Course version: LLM agent and MAS tasks.** Build a ReAct-style single agent with at least two
   tools, then build a two- or three-role multi-agent variant such as planner/executor/critic.
   Evaluate both on the same 5 tasks, with at least 3 repeated trials per setting, and compare
   success rate, cost, number of turns, consistency, and failure modes.
4. **Optional extension.** Reproduce a small component from a recent paper, such as reflection,
   memory, planning/re-planning, debate, or tool-use reliability.

## Paper Reading

**Multi-agent RL & game theory**
1. **Yu et al. (2021), "The Surprising Effectiveness of PPO in Cooperative, Multi-Agent Games."** A practical MARL baseline and implementation guide.
2. **Lowe et al. (2017), "Multi-Agent Actor-Critic for Mixed Cooperative-Competitive Environments (MADDPG)."** Historical deep MARL baseline.

**LLM agents**
3. **Yao et al. (2023), "ReAct: Synergizing Reasoning and Acting in Language Models."** The core agent loop.
4. **Liu et al. (2023), "AgentBench: Evaluating LLMs as Agents."** Multi-environment agent benchmark.
5. **Zhou et al. (2023), "WebArena: A Realistic Web Environment for Building Autonomous Agents."** Web task benchmark.
6. **Xie et al. (2024), "OSWorld."** Desktop and GUI agent evaluation.
7. **Yang et al. (2024), "SWE-agent."** Agent-computer interfaces for code agents.
8. **Yao et al. (2024), "tau-bench."** Tool-agent-user interaction and repeated-trial reliability.

**Multi-agent LLM systems**
9. **Wu et al. (2023), "AutoGen."** Programmable multi-agent conversation framework.
10. **Hong et al. (2023), "MetaGPT."** Role specialization and SOP-style collaboration.
11. **Fourney et al. (2024), "Magentic-One."** Generalist orchestrated multi-agent system.
12. **Shinn et al. (2023), "Reflexion."** Reflection and episodic memory without weight updates.

> Conferences to follow: **AAMAS, NeurIPS, ICML, ICLR, AAAI**. For LLM agents, watch
> [arXiv (cs.AI / cs.MA)](https://arxiv.org/list/cs.MA/recent) closely — the field moves monthly.

## Tools & Setup

| Tool | Use | Link |
|---|---|---|
| Gymnasium | Single-agent RL environments | [docs](https://gymnasium.farama.org/) |
| PettingZoo | Multi-agent environments | [docs](https://pettingzoo.farama.org/) |
| Stable-Baselines3 | RL algorithm implementations | [docs](https://stable-baselines3.readthedocs.io/) |
| AutoGen | Multi-agent LLM conversations | [docs](https://microsoft.github.io/autogen/) |
| LangGraph | Stateful agent / tool orchestration | [docs](https://langchain-ai.github.io/langgraph/) |

> **Hardware note:** MARL toy environments and LLM-agent exercises run on a CPU laptop — the LLM calls
> can use a hosted API or a small local model. No large GPU is required for this module.

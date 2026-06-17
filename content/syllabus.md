# Syllabus (Tentative) · 通用人工智能系统平台I

> **Audience:** 清华通班 first-year (spring) students · **Dates:** 2026-07-13 → 2026-07-26 (two weeks)
> **Venue:** 通院 2201 大教室 · **Format:** Lectures + Programming Exercises + Practical Reports

This course gives a hands-on, foundation-model–era tour of modern AI. We start from coding and
deep-learning foundations, then move through the four pillars of today's general AI systems:
**language models, multimodal vision, embodied AI, and agent systems**. Each module pairs a
*Learning Path* (what to study) with *Programming Exercises* (what to build) and a *Paper Reading*
list (what to read). Future updates and announcements will be posted in this repository and on
Web Learning — feel free to open an issue with questions.

## At a glance

| Days | Module | Owner |
|---|---|---|
| Day 1–2 | 00 · Foundations & Coding | All TAs |
| Day 3–5 | 01 · Foundation Models & NLP | 林子雍 |
| Day 6–8 | 02 · Multimodal & Vision | 巫莹莹 |
| Day 9–11 | 03 · Embodied AI & Robotics | 李炯烨 + 巫莹莹 |
| Day 12–13 | 04 · Agent Systems & Multi-Agent | 陈子昂 |
| Day 14 | Project report + final presentation | All TAs |

> Exact day boundaries are tentative; TAs will confirm the per-day breakdown before the course starts.

## Week 1

- **Day 1 — Setup & tooling.** Linux command line, Git/GitHub, Python virtual environments
  (conda / `uv`), VS Code. *HW:* set up your environment and clone the course exercise repo.
- **Day 2 — Document prep & DL refresher.** LaTeX/Overleaf, scientific writing & email etiquette;
  deep-learning recap with PyTorch tensors and autograd. *HW:* prepare a one-page LaTeX CV.
- **Day 3 — From tokens to Transformers.** Language modeling intuition, tokenization, attention,
  the Transformer block. *HW:* read & run nanoGPT.
- **Day 4 — Training & adapting LLMs.** Pretraining, scaling laws, instruction tuning, RLHF/DPO.
  *HW:* LoRA fine-tune a small model.
- **Day 5 — Using LLMs.** Prompting, chain-of-thought, retrieval-augmented generation (RAG),
  evaluation. *HW:* build a small RAG question-answering pipeline.

## Week 2

- **Day 6 — Vision foundations.** Image classification, CNNs → Vision Transformers. *HW:* train an
  image classifier.
- **Day 7 — Representation & generation.** Self-supervised learning (CLIP, DINOv2), diffusion models.
  *HW:* zero-shot classification with CLIP; sample from a diffusion model.
- **Day 8 — Multimodal & 3D.** Vision-language models, segmentation (SAM 2), NeRF / 3D Gaussian
  Splatting. *HW:* run a VLM and SAM 2 on your own images.
- **Day 9 — Robot fundamentals.** Rigid bodies, degrees of freedom, configuration space, URDF.
  *HW:* model a robot in URDF and visualize it.
- **Day 10 — Simulation & control.** MuJoCo / Isaac Lab / Genesis, reinforcement learning for control.
  *HW:* train a control policy in a simulator.
- **Day 11 — Robot learning.** Imitation learning, diffusion policy, vision-language-action (VLA)
  models. *HW:* run a diffusion-policy or VLA demo.
- **Day 12 — Single- & multi-agent RL.** MARL, game theory, cooperation. *HW:* a PettingZoo
  multi-agent environment.
- **Day 13 — LLM agents.** ReAct, tool use, planning, multi-agent collaboration & theory of mind.
  *HW:* build a tool-using ReAct agent.
- **Day 14 — Capstone.** Submit your practical report (LaTeX) and present your project.

## Deliverables

1. **Programming exercises** — one per module (submitted to the course repo).
2. **Practical reports** — written in LaTeX/English; at least one paper-summary report and one
   project report (focus on method + your own analysis/improvement).
3. **Final presentation** — a short talk on your capstone project on Day 14.

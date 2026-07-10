# Paper Reading List · 通用人工智能系统平台I

## Multimodal and Vision

### Topic Description

This direction studies how AI systems perceive, represent, segment, generate, and reason about
visual data, and how visual models connect to language, 3D structure, and embodied tasks. A good
reading path starts from recognition backbones, moves to self-supervised and language-supervised
representations, then studies generative models, promptable perception, multimodal instruction
tuning, and 3D scene representation.

### Required

1. He et al., 2016, [**Deep Residual Learning for Image Recognition**](https://arxiv.org/abs/1512.03385). Residual connections made very deep convolutional networks trainable and became a default building block for modern visual recognition.
2. Dosovitskiy et al., 2021, [**An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale**](https://arxiv.org/abs/2010.11929). Vision Transformer shows that image patches can be treated as tokens and that Transformer scaling can compete with convolutional inductive bias.
3. Radford et al., 2021, [**Learning Transferable Visual Models From Natural Language Supervision**](https://arxiv.org/abs/2103.00020). CLIP demonstrates that large-scale image-text contrastive learning yields open-vocabulary visual representations.
4. He et al., 2022, [**Masked Autoencoders Are Scalable Vision Learners**](https://arxiv.org/abs/2111.06377). MAE adapts masked reconstruction to vision and explains why high masking ratios produce strong scalable visual pretraining.
5. Ho et al., 2020, [**Denoising Diffusion Probabilistic Models**](https://arxiv.org/abs/2006.11239). DDPM establishes the denoising diffusion formulation that underlies most modern image, video, and policy generation systems.
6. Rombach et al., 2022, [**High-Resolution Image Synthesis with Latent Diffusion Models**](https://arxiv.org/abs/2112.10752). Latent diffusion moves generation into an autoencoder latent space, making high-resolution text-to-image synthesis practical.
7. Kirillov et al., 2023, [**Segment Anything**](https://arxiv.org/abs/2304.02643). SAM turns segmentation into a promptable foundation-model task and introduces a data-engine loop for large-scale mask collection.
8. Liu et al., 2023, [**Visual Instruction Tuning**](https://arxiv.org/abs/2304.08485). LLaVA gives the canonical recipe for connecting a vision encoder to an LLM through instruction tuning.
9. Mildenhall et al., 2020, [**NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis**](https://arxiv.org/abs/2003.08934). NeRF represents a 3D scene as a continuous radiance field and made differentiable view synthesis a central 3D vision paradigm.

### Optional

#### General visual representation

1. Caron et al., 2021, [**Emerging Properties in Self-Supervised Vision Transformers**](https://arxiv.org/abs/2104.14294). DINO shows that self-distilled ViTs can learn semantic object structure without labels.
2. Oquab et al., 2023, [**DINOv2: Learning Robust Visual Features without Supervision**](https://arxiv.org/abs/2304.07193). DINOv2 scales curated self-supervised pretraining into a reusable dense visual feature backbone.
3. Meta AI, 2025, [**DINOv3**](https://arxiv.org/abs/2508.10104). DINOv3 pushes dense self-supervised features further and is useful for understanding the 2025-2026 vision foundation model landscape.
4. Zhai et al., 2023, [**Sigmoid Loss for Language Image Pre-Training**](https://arxiv.org/abs/2303.15343). SigLIP replaces contrastive softmax with a sigmoid objective and became a common visual encoder choice for multimodal LLMs.

#### Generation and segmentation

1. Dhariwal and Nichol, 2021, [**Diffusion Models Beat GANs on Image Synthesis**](https://arxiv.org/abs/2105.05233). This paper made diffusion models the leading high-fidelity image generation family.
2. Peebles and Xie, 2023, [**Scalable Diffusion Models with Transformers**](https://arxiv.org/abs/2212.09748). DiT shows how replacing U-Nets with Transformers improves diffusion scaling behavior.
3. Esser et al., 2024, [**Scaling Rectified Flow Transformers for High-Resolution Image Synthesis**](https://arxiv.org/abs/2403.03206). Stable Diffusion 3 combines rectified flow and Transformer design for stronger text-image alignment.
4. Ravi et al., 2024, [**SAM 2: Segment Anything in Images and Videos**](https://arxiv.org/abs/2408.00714). SAM 2 extends promptable segmentation from images to streaming video with memory.

#### Multimodal reasoning and 3D

1. Alayrac et al., 2022, [**Flamingo: A Visual Language Model for Few-Shot Learning**](https://arxiv.org/abs/2204.14198). Flamingo shows how frozen language models can absorb visual context through cross-attention and few-shot prompts.
2. Li et al., 2023, [**BLIP-2: Bootstrapping Language-Image Pre-training with Frozen Image Encoders and Large Language Models**](https://arxiv.org/abs/2301.12597). BLIP-2 introduces a lightweight querying bridge between frozen vision encoders and LLMs.
3. Kerbl et al., 2023, [**3D Gaussian Splatting for Real-Time Radiance Field Rendering**](https://arxiv.org/abs/2308.04079). 3D Gaussian Splatting makes high-quality novel-view rendering fast enough for real-time scene interaction.
4. Johnson et al., 2017, [**CLEVR: A Diagnostic Dataset for Compositional Language and Elementary Visual Reasoning**](https://arxiv.org/abs/1612.06890). CLEVR remains a clean diagnostic benchmark for separating perception from compositional visual reasoning.

---

## Cognition

### Topic Description

This direction asks what forms of representation, reasoning, learning, and social understanding are
needed for human-like intelligence. The key contrast is between statistical pattern recognition and
models that support causal explanation, intuitive physics, theory of mind, compositionality, and
systematic generalization.

### Required

1. Marr, 1982, [**Vision: A Computational Investigation into the Human Representation and Processing of Visual Information**](https://mitpress.mit.edu/9780262514620/vision/). Marr's three levels of analysis remain the clearest framework for separating computational goals, algorithms, and implementations.
2. Tenenbaum et al., 2011, [**How to Grow a Mind: Statistics, Structure, and Abstraction**](https://doi.org/10.1126/science.1192788). This paper explains how probabilistic programs and structured priors can support rapid concept learning.
3. Battaglia, Hamrick, and Tenenbaum, 2013, [**Simulation as an Engine of Physical Scene Understanding**](https://doi.org/10.1073/pnas.1306572110). The intuitive-physics-engine hypothesis models human physical reasoning as approximate probabilistic simulation.
4. Lake et al., 2017, [**Building Machines That Learn and Think Like People**](https://doi.org/10.1017/S0140525X16001837). This manifesto argues that human-like AI needs causal models, compositionality, intuitive physics, intuitive psychology, and learning-to-learn.
5. Baker et al., 2017, [**Rational Quantitative Attribution of Beliefs, Desires and Percepts in Human Mentalizing**](https://doi.org/10.1038/s41562-017-0064). Bayesian theory of mind explains how humans infer hidden mental states from observed actions.
6. Chollet, 2019, [**On the Measure of Intelligence**](https://arxiv.org/abs/1911.01547). ARC reframes intelligence evaluation around skill-acquisition efficiency and systematic generalization rather than task-specific performance.
7. Zhang et al., 2021, [**ACRE: Abstract Causal REasoning Beyond Covariation**](https://arxiv.org/abs/2103.14232). ACRE tests whether visual reasoning systems can infer causal structure beyond surface-level correlation.

### Optional

#### Language, concepts, and abstraction

1. Fodor, 1975, [**The Language of Thought**](https://www.hup.harvard.edu/books/9780674510302). The book gives the classical symbolic account of mental representation and compositional thought.
2. Carey, 2009, [**The Origin of Concepts**](https://doi.org/10.1093/acprof:oso/9780195367638.001.0001). This work explains conceptual change and why children can acquire new representational systems.
3. Lake, Salakhutdinov, and Tenenbaum, 2015, [**Human-Level Concept Learning Through Probabilistic Program Induction**](https://doi.org/10.1126/science.aab3050). The Bayesian Program Learning model explains one-shot character learning with compositional programs.
4. Marcus, 2018, [**Deep Learning: A Critical Appraisal**](https://arxiv.org/abs/1801.00631). This critique is useful for identifying what neural networks still struggle to learn systematically.

#### Causal, physical, and neuro-symbolic reasoning

1. Pearl, 2009, [**Causal Inference in Statistics: An Overview**](https://doi.org/10.1214/09-SS057). Pearl introduces the intervention-centered language needed to distinguish association from causation.
2. Ullman et al., 2017, [**Mind Games: Game Engines as an Architecture for Intuitive Physics**](https://doi.org/10.1016/j.tics.2017.05.012). This review connects human intuitive physics to approximate simulation engines.
3. Yi et al., 2018, [**Neural-Symbolic VQA: Disentangling Reasoning from Vision and Language Understanding**](https://arxiv.org/abs/1810.02338). The paper separates perception, program parsing, and symbolic execution in visual question answering.
4. Mao et al., 2019, [**The Neuro-Symbolic Concept Learner**](https://arxiv.org/abs/1904.12584). NS-CL learns visual concepts and symbolic programs jointly from language-supervised scenes.
5. Ellis et al., 2021, [**DreamCoder: Growing Generalizable, Interpretable Knowledge with Wake-Sleep Bayesian Program Learning**](https://arxiv.org/abs/2006.08381). DreamCoder shows how program synthesis can build reusable conceptual libraries.

#### Social cognition and human-AI thought partners

1. Premack and Woodruff, 1978, [**Does the Chimpanzee Have a Theory of Mind?**](https://doi.org/10.1017/S0140525X00076512). This classic paper introduced theory of mind as a concrete empirical question.
2. Ho, Saxe, and Cushman, 2022, [**Planning with Theory of Mind**](https://doi.org/10.1016/j.tics.2022.08.003). This review links social reasoning to planning under beliefs, goals, and recursive mental-state inference.
3. Fan et al., 2024, [**Building Machines that Learn and Think with People**](https://arxiv.org/abs/2408.03943). This perspective shifts the target from isolated intelligence to collaborative cognition with human partners.

---

## Embodied AI and Robotics

### Topic Description

This direction studies agents that perceive, plan, learn, and act in physical or simulated
environments. The core progression is simulation and control, reinforcement and imitation learning,
data-driven manipulation, diffusion policies, and finally vision-language-action models that connect
web-scale knowledge to robot control.

### Required

1. Todorov, Erez, and Tassa, 2012, [**MuJoCo: A Physics Engine for Model-Based Control**](https://homes.cs.washington.edu/~todorov/papers/TodorovIROS12.pdf). MuJoCo made fast, contact-rich continuous-control simulation a standard substrate for robot learning.
2. Schulman et al., 2017, [**Proximal Policy Optimization Algorithms**](https://arxiv.org/abs/1707.06347). PPO is the practical policy-gradient baseline students should know before reading modern embodied RL papers.
3. Haarnoja et al., 2018, [**Soft Actor-Critic Algorithms and Applications**](https://arxiv.org/abs/1812.05905). SAC explains entropy-regularized off-policy RL and remains a strong baseline for continuous control.
4. Ho and Ermon, 2016, [**Generative Adversarial Imitation Learning**](https://arxiv.org/abs/1606.03476). GAIL frames imitation as matching expert occupancy measures without requiring explicit reward design.
5. Brohan et al., 2022, [**RT-1: Robotics Transformer for Real-World Control at Scale**](https://arxiv.org/abs/2212.06817). RT-1 shows that Transformer policies can learn many real-robot manipulation tasks from large demonstration datasets.
6. Chi et al., 2023, [**Diffusion Policy: Visuomotor Policy Learning via Action Diffusion**](https://arxiv.org/abs/2303.04137). Diffusion Policy treats action generation as conditional denoising and became a central visuomotor imitation baseline.
7. Zhao et al., 2023, [**Learning Fine-Grained Bimanual Manipulation with Low-Cost Hardware**](https://arxiv.org/abs/2304.13705). ACT shows how action chunking and low-cost data collection can produce strong bimanual manipulation policies.
8. Brohan et al., 2023, [**RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control**](https://arxiv.org/abs/2307.15818). RT-2 demonstrates that VLM pretraining can improve semantic generalization in robot actions.
9. Kim et al., 2024, [**OpenVLA: An Open-Source Vision-Language-Action Model**](https://arxiv.org/abs/2406.09246). OpenVLA provides an open VLA recipe and checkpoint family for fine-tuning generalist robot policies.

### Optional

#### Simulation, environments, and data

1. Savva et al., 2019, [**Habitat: A Platform for Embodied AI Research**](https://arxiv.org/abs/1904.01201). Habitat offers fast photorealistic simulation for navigation and embodied perception.
2. Li et al., 2021, [**iGibson 2.0: Object-Centric Simulation for Robot Learning of Everyday Household Tasks**](https://arxiv.org/abs/2108.03272). iGibson emphasizes interactive household scenes with physics and articulated objects.
3. Srivastava et al., 2022, [**BEHAVIOR: Benchmark for Everyday Household Activities in Virtual, Interactive, and Ecological Environments**](https://arxiv.org/abs/2108.03332). BEHAVIOR evaluates embodied agents on long-horizon household activities rather than isolated skills.
4. O'Neill et al., 2023, [**Open X-Embodiment: Robotic Learning Datasets and RT-X Models**](https://arxiv.org/abs/2310.08864). Open X-Embodiment aggregates cross-robot datasets and studies transfer across embodiments.

#### World models, real-world RL, and generalist policies

1. Hafner et al., 2023, [**Mastering Diverse Domains through World Models**](https://arxiv.org/abs/2301.04104). DreamerV3 shows how latent world models can solve diverse RL domains with one algorithm.
2. Ahn et al., 2022, [**Do As I Can, Not As I Say: Grounding Language in Robotic Affordances**](https://arxiv.org/abs/2204.01691). SayCan combines language-model planning with value functions that estimate what the robot can actually do.
3. Octo Model Team et al., 2024, [**Octo: An Open-Source Generalist Robot Policy**](https://arxiv.org/abs/2405.12213). Octo provides an open, transformer-based policy trained across multiple robots and tasks.
4. Luo et al., 2024, [**SERL: A Software Suite for Sample-Efficient Robotic Reinforcement Learning**](https://arxiv.org/abs/2401.16013). SERL is a practical recipe for real-world visual RL with limited robot interaction.
5. Black et al., 2024, [**pi0: A Vision-Language-Action Flow Model for General Robot Control**](https://arxiv.org/abs/2410.24164). pi0 uses flow matching for generalist robot action generation and is a useful bridge between diffusion policies and VLAs.

---

## Foundation Models and NLP

### Topic Description

This direction studies language models as general-purpose sequence models: pretraining objectives,
scaling, adaptation, alignment, retrieval, reasoning, tool use, and evaluation. The reading path should
make clear which capability comes from architecture, which comes from data and scale, and which
comes from post-training or external tools.

### Required

1. Vaswani et al., 2017, [**Attention Is All You Need**](https://arxiv.org/abs/1706.03762). The Transformer replaces recurrence with attention and supplies the architecture behind modern language and multimodal models.
2. Devlin et al., 2019, [**BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding**](https://aclanthology.org/N19-1423/). BERT establishes encoder-only masked language modeling as a reusable representation-learning paradigm.
3. Brown et al., 2020, [**Language Models are Few-Shot Learners**](https://arxiv.org/abs/2005.14165). GPT-3 demonstrates in-context learning and made scale a central experimental variable in NLP.
4. Raffel et al., 2020, [**Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer**](https://www.jmlr.org/papers/v21/20-074.html). T5 unifies NLU and NLG tasks under a text-to-text interface and motivates careful pretraining ablations.
5. Lewis et al., 2020, [**Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks**](https://arxiv.org/abs/2005.11401). RAG separates parametric memory from non-parametric retrieval and remains the basic architecture for knowledge-grounded generation.
6. Hoffmann et al., 2022, [**Training Compute-Optimal Large Language Models**](https://arxiv.org/abs/2203.15556). Chinchilla scaling laws show that data scale is as important as parameter scale under fixed compute.
7. Ouyang et al., 2022, [**Training Language Models to Follow Instructions with Human Feedback**](https://arxiv.org/abs/2203.02155). InstructGPT defines the supervised fine-tuning plus RLHF pipeline that shaped instruction-following assistants.
8. DeepSeek-AI, 2025, [**DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning**](https://arxiv.org/abs/2501.12948). DeepSeek-R1 shows how large-scale RL and distillation can produce strong open reasoning models.

### Optional

#### Representations and task adaptation

1. Peters et al., 2018, [**Deep Contextualized Word Representations**](https://aclanthology.org/N18-1202/). ELMo is the clean historical bridge from static word vectors to contextual token representations.
2. Liu et al., 2019, [**RoBERTa: A Robustly Optimized BERT Pretraining Approach**](https://arxiv.org/abs/1907.11692). RoBERTa shows that many BERT gains come from data, training duration, and objective details.
3. Reimers and Gurevych, 2019, [**Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks**](https://aclanthology.org/D19-1410/). SBERT adapts Transformers into efficient sentence embeddings for retrieval and similarity.
4. Gao et al., 2021, [**SimCSE: Simple Contrastive Learning of Sentence Embeddings**](https://aclanthology.org/2021.emnlp-main.552/). SimCSE gives a minimal contrastive recipe for strong sentence representations.
5. Hu et al., 2021, [**LoRA: Low-Rank Adaptation of Large Language Models**](https://arxiv.org/abs/2106.09685). LoRA makes adaptation cheaper by training low-rank update matrices rather than all model weights.

#### Scaling, architectures, and preference learning

1. Fedus, Zoph, and Shazeer, 2022, [**Switch Transformers: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity**](https://www.jmlr.org/papers/v23/21-0998.html). Switch Transformer explains sparse mixture-of-experts scaling with conditional computation.
2. Touvron et al., 2023, [**Llama 2: Open Foundation and Fine-Tuned Chat Models**](https://arxiv.org/abs/2307.09288). Llama 2 is a key open model report for understanding data filtering, scaling, and chat post-training.
3. Gu and Dao, 2023, [**Mamba: Linear-Time Sequence Modeling with Selective State Spaces**](https://arxiv.org/abs/2312.00752). Mamba is the main state-space alternative students should know when comparing attention with linear-time sequence models.
4. Rafailov et al., 2023, [**Direct Preference Optimization: Your Language Model is Secretly a Reward Model**](https://arxiv.org/abs/2305.18290). DPO turns preference optimization into a supervised-style objective without an explicit reward model.

#### Reasoning, retrieval, and tool use

1. Wei et al., 2022, [**Chain-of-Thought Prompting Elicits Reasoning in Large Language Models**](https://arxiv.org/abs/2201.11903). Chain-of-thought prompting shows that exemplars with intermediate reasoning can unlock multi-step problem solving.
2. Wang et al., 2022, [**Self-Consistency Improves Chain of Thought Reasoning in Language Models**](https://arxiv.org/abs/2203.11171). Self-consistency improves reasoning by sampling multiple solution paths and voting over answers.
3. Schick et al., 2023, [**Toolformer: Language Models Can Teach Themselves to Use Tools**](https://arxiv.org/abs/2302.04761). Toolformer studies how a language model can learn API use from self-supervised tool-call data.
4. Gao et al., 2023, [**PAL: Program-Aided Language Models**](https://arxiv.org/abs/2211.10435). PAL delegates symbolic calculation to generated programs, making the division between language reasoning and execution explicit.

---

## Social Simulation

### Topic Description

This direction studies how macro-level social patterns can emerge from interacting agents, and how
simulation can be used responsibly as a scientific instrument. Students should distinguish model
rules from empirical claims, validate simulations against data when possible, and treat LLM-based
agents as an experimental tool rather than a substitute for social science.

### Required

1. Schelling, 1971, [**Dynamic Models of Segregation**](https://doi.org/10.1080/0022250X.1971.9989794). Schelling shows how mild local preferences can generate strong global segregation, making it the canonical emergent-social-pattern model.
2. Epstein and Axtell, 1996, [**Growing Artificial Societies: Social Science from the Bottom Up**](https://mitpress.mit.edu/9780262050531/growing-artificial-societies/). Sugarscape demonstrates how heterogeneous agents and simple local rules can generate macro-level social phenomena.
3. Bonabeau, 2002, [**Agent-Based Modeling: Methods and Techniques for Simulating Human Systems**](https://doi.org/10.1073/pnas.082080899). This article gives a compact methodological introduction to when and why agent-based simulation is useful.
4. ter Hoeven et al., 2025, [**Mesa 3: Agent-Based Modeling with Python in 2025**](https://doi.org/10.21105/joss.07668). Mesa 3 is the practical Python framework behind the course social-simulation assignment.
5. Park et al., 2023, [**Generative Agents: Interactive Simulacra of Human Behavior**](https://arxiv.org/abs/2304.03442). Generative Agents introduces memory, reflection, and planning as the standard architecture for believable LLM-driven social agents.
6. Vezhnevets et al., 2023, [**Generative Agent-Based Modeling with Actions Grounded in Physical, Social, or Digital Space Using Concordia**](https://arxiv.org/abs/2312.03664). Concordia provides a reusable framework for LLM-based social simulations with explicit environments and game-master mediation.
7. Piao et al., 2025, [**AgentSociety: Large-Scale Simulation of LLM-Driven Generative Agents Advances Understanding of Human Behaviors and Society**](https://arxiv.org/abs/2502.08691). AgentSociety scales LLM-agent simulation to urban-scale social experiments while raising questions about validity and ethics.

### Optional

#### Classical social simulation

1. Granovetter, 1978, [**Threshold Models of Collective Behavior**](https://doi.org/10.1086/226707). Threshold models explain how individual activation thresholds can create cascades and collective action.
2. Axelrod, 1997, [**The Dissemination of Culture: A Model with Local Convergence and Global Polarization**](https://doi.org/10.1177/0022002797041002001). Axelrod's model is a classic account of how local influence can produce both cultural convergence and persistent polarization.
3. Epstein, 1999, [**Agent-Based Computational Models and Generative Social Science**](https://doi.org/10.1002/%28SICI%291099-0526%28199905/06%294:5%3C41::AID-CPLX9%3E3.0.CO;2-F). Epstein clarifies the generative explanation standard: grow the target phenomenon from explicit micro-rules.
4. Macy and Willer, 2002, [**From Factors to Actors: Computational Sociology and Agent-Based Modeling**](https://doi.org/10.1146/annurev.soc.28.110601.141117). This review explains how ABM changes sociological explanation from variable correlations to interacting actors.

#### LLM-based social agents and validation

1. Park et al., 2024, [**LLM Agents Grounded in Self-Reports Enable General-Purpose Simulation of Individuals**](https://arxiv.org/abs/2411.10109). This work explores whether interview-grounded LLM agents can reproduce individual survey and behavioral patterns.
2. Zhang et al., 2024, [**Designing Reliable Experiments with Generative Agent-Based Modeling**](https://arxiv.org/abs/2411.07038). The paper focuses on experimental controls and reliability for LLM-based agent simulations.
3. Moghaddam and Honey, 2026, [**AI Agents Alone Are Not (Yet) Sufficient for Social Simulation**](https://arxiv.org/abs/2603.00113). This critique is useful for discussing why LLM realism, calibration, and validation remain unresolved.

---

## Agent Systems and Multi-Agent Systems

### Topic Description

This direction studies systems that use language models as interactive decision makers: they plan,
call tools, browse websites, operate computers, write code, collaborate with other agents, and are
evaluated by executable task success. The core question is not just whether a model can answer a
prompt, but whether an agent loop remains reliable under long-horizon interaction, partial
observability, tool errors, and multi-agent coordination.

### Required

1. Yao et al., 2023, [**ReAct: Synergizing Reasoning and Acting in Language Models**](https://arxiv.org/abs/2210.03629). ReAct defines the reason-act-observe loop that underlies many tool-using LLM agents.
2. Schick et al., 2023, [**Toolformer: Language Models Can Teach Themselves to Use Tools**](https://arxiv.org/abs/2302.04761). Toolformer shows how tool calls can be learned from self-supervised annotations rather than fully hand-written traces.
3. Liu et al., 2023, [**AgentBench: Evaluating LLMs as Agents**](https://arxiv.org/abs/2308.03688). AgentBench evaluates LLMs across multiple interactive environments and makes agent evaluation broader than question answering.
4. Zhou et al., 2023, [**WebArena: A Realistic Web Environment for Building Autonomous Agents**](https://arxiv.org/abs/2307.13854). WebArena provides executable web tasks with realistic websites and success criteria.
5. Xie et al., 2024, [**OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments**](https://arxiv.org/abs/2404.07972). OSWorld measures whether agents can operate real desktop applications from visual observations and actions.
6. Yang et al., 2024, [**SWE-agent: Agent-Computer Interfaces Enable Automated Software Engineering**](https://arxiv.org/abs/2405.15793). SWE-agent shows that the interface between model and computer strongly affects software-engineering performance.
7. Yao et al., 2024, [**tau-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains**](https://arxiv.org/abs/2406.12045). tau-bench evaluates policy-following and tool reliability across repeated user-agent interactions.
8. Fourney et al., 2024, [**Magentic-One: A Generalist Multi-Agent System for Solving Complex Tasks**](https://arxiv.org/abs/2411.04468). Magentic-One is a clear example of orchestrated multi-agent planning, delegation, and re-planning.
9. Yu et al., 2021, [**The Surprising Effectiveness of PPO in Cooperative Multi-Agent Games**](https://arxiv.org/abs/2103.01955). MAPPO is the practical deep-MARL baseline for comparing LLM-agent coordination with reinforcement-learning multi-agent systems.

### Optional

#### Agent memory, reflection, and embodied interaction

1. Shinn et al., 2023, [**Reflexion: Language Agents with Verbal Reinforcement Learning**](https://arxiv.org/abs/2303.11366). Reflexion studies how verbal feedback and episodic memory can improve future agent attempts without weight updates.
2. Wang et al., 2023, [**Voyager: An Open-Ended Embodied Agent with Large Language Models**](https://arxiv.org/abs/2305.16291). Voyager combines code-as-action, curriculum discovery, and skill libraries in an open-ended embodied environment.
3. Sumers et al., 2024, [**Cognitive Architectures for Language Agents**](https://arxiv.org/abs/2309.02427). This survey gives a useful taxonomy of memory, planning, action, and reflection modules in language agents.

#### Multi-agent frameworks and collaboration

1. Wu et al., 2023, [**AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation**](https://arxiv.org/abs/2308.08155). AutoGen provides a programmable framework for multi-agent conversation and tool use.
2. Hong et al., 2023, [**MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework**](https://arxiv.org/abs/2308.00352). MetaGPT tests role specialization and standard operating procedures for collaborative software tasks.
3. Qian et al., 2023, [**ChatDev: Communicative Agents for Software Development**](https://arxiv.org/abs/2307.07924). ChatDev is useful for studying the strengths and brittleness of role-play-based software-development agents.
4. Lowe et al., 2017, [**Multi-Agent Actor-Critic for Mixed Cooperative-Competitive Environments**](https://arxiv.org/abs/1706.02275). MADDPG is a historical deep-MARL baseline for centralized training with decentralized execution.

#### Harder evaluation settings

1. Jimenez et al., 2024, [**SWE-bench: Can Language Models Resolve Real-World GitHub Issues?**](https://arxiv.org/abs/2310.06770). SWE-bench evaluates coding agents on real repository issues with test-based grading.
2. Siegel et al., 2024, [**CORE-Bench: Fostering the Credibility of Published Research Through a Computational Reproducibility Agent Benchmark**](https://arxiv.org/abs/2409.11363). CORE-Bench tests whether agents can reproduce scientific results from papers, code, and data.
3. Watkins et al., 2026, [**Terminal-Bench: Benchmarking Agents on Hard, Realistic Tasks in Terminal Environments**](https://arxiv.org/abs/2601.11868). Terminal-Bench is a recent benchmark for shell-based agents with testable, environment-specific tasks.

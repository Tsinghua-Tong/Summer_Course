# Homework · 通用人工智能系统平台 I

Except for a short in-person session in Room 2201 on the afternoon of July 14, students should arrange their own time in the afternoons and evenings to read the assigned materials and complete the homework. The assignments are designed to help you become familiar with common research tools and gain an introductory understanding of different AI research areas. You are encouraged to make good use of online resources, AI tools, and discussions with classmates. If a problem remains unresolved, please contact the teaching assistants, who will be available online every workday from 13:00 to 16:00. Please plan ahead and submit all assignments on time, as late submissions may receive a grade deduction.

---

## Day 1–2 · Preparatory Work (July 13–14)

#### Learning Path

- Basic Linux command-line skills: [MIT The Missing Semester of Your CS Education](https://missing.csail.mit.edu/).
- Git and GitHub: [GitHub Skills](https://skills.github.com/) and [Git and GitHub Tutorial for Beginners](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners).
- Python environments and Jupyter: [CS231n Software Setup](https://cs231n.github.io/setup-instructions/).
- PyTorch basics: [PyTorch Learn the Basics](https://pytorch.org/tutorials/beginner/basics/intro.html).
- LaTeX:
  - Editors: [Overleaf](https://www.overleaf.com/) and [LaTeX Workshop in VS Code](https://dev.to/ucscmozilla/how-to-create-and-compile-latex-documents-on-visual-studio-code-3jbk).
  - Documentation: [Overleaf Learn](https://www.overleaf.com/learn) and [LaTeX Quick Start](https://www.overleaf.com/learn/latex/Free_online_introduction_to_LaTeX_(part_1)).

### Homework

1. **Archive homework: LaTeX CV**
   - **Requirements:** Export your personal CV as a PDF named `<your_name>_CV.pdf` and upload it to [`Tsinghua-Tong/2025-CV`](https://github.com/Tsinghua-Tong/2025-CV). Keep the CV within three pages. It may be written in Chinese or English, with flexible layout and typography. It must include at least a self-introduction, education background, honors and awards, personal skills, and research interests. The emphasis is on mastering LaTeX; grading will focus on completeness, correctness, and visual quality rather than the specific CV content.
   - **Template references:** [Overleaf CV templates](https://www.overleaf.com/gallery/tagged/cv). You may also use open-source CV templates from GitHub as references and replace publication-heavy sections with course projects or other relevant experience.
   - **Submission:** Upload `<your_name>_CV.pdf` to the designated GitHub repository.
   - **Deadline:** July 14, 23:59.
   - **Optional bonus:** Create a publicly accessible personal website by July 17, 23:59, preferably using GitHub Pages with a `.github.io` address. Up to 2 bonus points may be awarded.

2. **Python Environment Setup**
   - **Requirements:** Follow the [CS131 homework guideline](http://vision.stanford.edu/teaching/cs131_fall2021/assignments.html) to create a Python virtual environment and run Jupyter Notebook both locally, using Anaconda, VS Code, or JupyterLab, and online using Google Colab. Clone the CS131 homework repository and install the required packages. The Python and NumPy review notebooks listed in the syllabus are recommended for optional self-practice.
   - **The notebook must include:**
     - Your operating system, Python version, and environment-management tool;
     - The commands used to create and activate the virtual environment;
     - The command used to clone the CS131 repository;
     - The commands used to install the required packages;
     - Code that imports the main required packages and prints their versions;
     - A simple NumPy operation and a Matplotlib figure;
     - Screenshots showing that the notebook runs successfully both locally and on Google Colab;
     - A brief description of any setup problem encountered and how it was resolved.
   - **Submission:** Submit one notebook named `EnvironmentSetup_StudentID_Name.ipynb` to **Tsinghua University Web Learning（清华网络学堂）**. The notebook must run from beginning to end without errors. Do not submit the cloned repository or the virtual-environment directory.
   - **Deadline:** July 14, 23:59.

---

## Day 3–4 · Multimodal and Vision (July 15–16)

### Learning Path

- Classical vision and assignment style: [Stanford CS131](https://cs131.stanford.edu/) and [StanfordVL CS131 released assignments](https://github.com/stanfordvl/cs131_release).
- Modern deep vision: [Stanford CS231n 2025](https://cs231n.stanford.edu/2025/), [CS231n assignments](https://cs231n.stanford.edu/assignments.html), and the [PyTorch CIFAR-10 tutorial](https://docs.pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html).
- Transfer learning and pretrained models: [PyTorch transfer-learning tutorial](https://docs.pytorch.org/tutorials/beginner/transfer_learning_tutorial.html) and [torchvision model weights](https://docs.pytorch.org/vision/main/models.html).
- Multimodal extension: [OpenCLIP](https://github.com/mlfoundations/open_clip) and [Hugging Face zero-shot image classification](https://huggingface.co/docs/transformers/tasks/zero_shot_image_classification).

### Homework

1. **CIFAR-10 Classification and Transfer Learning**
   - **Requirements:** Complete the assignment in one reproducible Jupyter or Colab notebook.
     - Load CIFAR-10 with `torchvision.datasets.CIFAR10` and report the number of training and test examples and the ten class names.
     - Display at least 20 labeled training images in a grid.
     - Train a small CNN from scratch for at least 5 epochs. The network must contain at least two convolutional layers, one pooling operation, and one fully connected classification layer.
     - Fine-tune a pretrained `ResNet18` from `torchvision`. Replace its final classification layer for CIFAR-10 and clearly state whether the backbone is frozen or jointly fine-tuned.
     - Use the same data split for both models. Record the random seed, batch size, optimizer, learning rate, number of epochs, device, and total training time.
     - Report test accuracy for both models in one table and provide per-class accuracy for the better model.
     - Plot the training loss and evaluation accuracy curves.
     - Show at least 8 misclassified test images from the better model, including ground-truth and predicted labels, and write a 100–150 word failure analysis.
     - The notebook must run from beginning to end without manual code changes. Do not submit downloaded datasets or model checkpoints.
   - **Submission:** Submit one notebook named `Vision_StudentID_Name.ipynb` to **Tsinghua University Web Learning（清华网络学堂）**. Before submission, restart the runtime and run all cells so that outputs, figures, and final metrics are saved.
   - **Deadline:** July 16, 23:59.
   - **Optional bonus:** Use OpenCLIP or another CLIP implementation for zero-shot CIFAR-10 classification. Compare at least three prompt templates and report the best accuracy and five representative failure cases. Up to 1 bonus point.

---

## Day 5–6 · Cognition (July 17–18)

### Learning Path

- Read at least **one classic paper** and **one modern paper** from the lists provided by the instructors.
- You may connect the papers to one contemporary theme:
  - Self-supervised and foundation models;
  - Agentic AI;
  - Multimodal and embodied intelligence;
  - Neuroscience-inspired AI;
  - Causal and compositional learning;
  - Interpretability and alignment.

### Homework

1. **Short Cognition Report**
   - **Requirements:** Write a short report in English using LaTeX. Address the following questions:
     1. Choose one classic paper and identify a corresponding modern machine-learning technique or research direction. Explain the connection and the main differences between the original interpretation and the modern version.
     2. Based on at least one modern paper, summarize the authors’ hypothesis, method, evidence, and conclusion. Comment on whether the experimental design and results adequately support the conclusion.
     3. Extend the discussion to one current AI theme. Explain what concrete progress has been made and what remains unsolved.
     4. Discuss whether modern or future AI should have a biological or cognitive basis. State your own position and support it with clear reasoning.
     5. Add one further observation or question that you consider important.
   - **Report format:**
     - 2–3 pages, excluding references;
     - Approximately 1,000–1,500 English words;
     - At least one classic paper and one modern paper must be cited;
     - Include a title, main text, and references; an abstract is not required;
     - Figures and tables are optional.
   - **Submission:** Submit one compiled PDF named `Cognition_StudentID_Name.pdf` to **Tsinghua University Web Learning（清华网络学堂）**. Check that equations, fonts, figures, and references render correctly.
   - **Deadline:** July 18, 23:59.

---

## Day 7–8 · Embodied AI and Robotics (July 19–20)

### Learning Path

- Robotics foundations: [Modern Robotics](https://hades.mech.northwestern.edu/index.php/Modern_Robotics), especially the chapters on configuration space and rigid-body motion.
- Robot description: [ROS 2 URDF tutorials](https://docs.ros.org/en/foxy/Tutorials/Intermediate/URDF/Using-URDF-with-Robot-State-Publisher.html).
- Simulation: [PyBullet Quickstart Guide](https://github.com/bulletphysics/bullet3/blob/master/docs/pybullet_quickstartguide.pdf), [MuJoCo documentation](https://mujoco.readthedocs.io/), and [Gymnasium-Robotics](https://robotics.farama.org/).
- Robot learning: [CMU 16-831 Introduction to Robot Learning](https://16-831.github.io/fall25/) and [Stable-Baselines3 examples](https://stable-baselines3.readthedocs.io/en/master/guide/examples.html).

### Homework

1. **URDF Robot Modeling and Joint Control**
   - **Requirements:** Build and simulate one articulated robot. PyBullet is recommended; MuJoCo, Gazebo, Isaac Sim, or another simulator may be used if the same outputs are provided.
     - Create or substantially modify a URDF model containing at least three links, two movable joints, visual geometry, collision geometry, and inertial parameters.
     - At least two joints must be commandable. The model may additionally contain fixed joints.
     - Write a Python program that loads the robot, sets gravity and the simulation time step, prints joint names, types, and limits, and commands the movable joints using position or velocity control.
     - Execute a scripted motion lasting at least 10 simulated seconds.
     - Save the joint-position trajectory to `joint_trajectory.csv` and plot joint position against simulation time.
     - Record one 10–30 second MP4 or GIF showing the motion clearly.
     - In `README.md`, include installation commands, the command used to run the simulation, a short description of the robot structure, and a brief explanation of the difference among kinematic description, dynamics parameters, and control commands.
   - **Submission:** Submit one ZIP file named `Robotics_StudentID_Name.zip`. It should contain all files needed to reproduce the result, including a README, the robot description file, the control script, the saved joint trajectory, the trajectory plot, and one rollout video or GIF. Suggested filenames are `README.md`, `robot.urdf`, `control.py`, `joint_trajectory.csv`, `joint_trajectory.png`, and `rollout.mp4` or `rollout.gif`, but small naming or folder-organization differences are acceptable as long as the README clearly explains each file and the staff can run the project without editing file paths. Upload the ZIP file to **Tsinghua University Web Learning（清华网络学堂）**.
   - **Deadline:** July 20, 23:59.
   - **Optional bonus:** Train PPO on `CartPole-v1` or one small Gymnasium/MuJoCo task for at least three random seeds. Submit the learning curve and the mean and standard deviation of final returns. Up to 1 bonus point.

---

## Day 9–10 · Foundation Models and NLP (July 21–22)

### Learning Path

- NLP API reference: [Hugging Face Transformers documentation](https://huggingface.co/docs/transformers).
- Practical library path: [Hugging Face LLM Course](https://huggingface.co/learn/llm-course).
- University course path: [Stanford CS224N](https://web.stanford.edu/class/cs224n/) and [Stanford CS336: Language Modeling from Scratch](https://stanford-cs336.github.io/spring2024/).
- Code-first tutorial: [The Annotated Transformer](https://nlp.seas.harvard.edu/annotated-transformer/).

### Homework

1. **Archive homework: CS224N Assignment 1**
   - **Requirements:** Play with Jupyter Notebook and complete the word-vector assignment. Reference: [CS224N Assignment 1: Exploring Word Vectors](https://web.stanford.edu/class/archive/cs/cs224n/cs224n.1246/assignments/a1_preview/exploring_word_vectors.html).

2. **Reference assignment: CS336 Assignment 1 style**
   - **Requirements:** Use [CS336 Assignment 1: Basics](https://github.com/stanford-cs336/spring2024-assignment1-basics) as a reference for inspecting or implementing the core parts of a small language-model pipeline, including the tokenizer, model, optimizer, sampling procedure, and training/evaluation loop.

3. **Course version: NLP Tasks with Transformers**
   - **Requirements:** Use the Hugging Face `transformers` library to complete the following three practices in one or more reproducible notebooks:
     - **Token classification:** Fine-tune a Transformer for part-of-speech tagging or named-entity recognition, following the [token-classification tutorial](https://huggingface.co/docs/transformers/tasks/token_classification).
     - **Text classification:** Fine-tune a Transformer for a sentence- or document-level classification task, following the [text-classification tutorial](https://huggingface.co/docs/transformers/tasks/sequence_classification).
     - **Text generation:** Load a small causal language model and compare greedy decoding, sampling, top-k, top-p, and temperature-based decoding using the [text-generation tutorial](https://huggingface.co/docs/transformers/generation_strategies).
   - **Submission:** Submit one or more reproducible notebooks to **Tsinghua University Web Learning（清华网络学堂）**. Name the main file `NLP_StudentID_Name.ipynb`. Before submission, restart the runtime and run all cells so that outputs, figures, and final metrics are saved.
   - **Deadline:** July 23, 23:59.
   - **Optional bonus**: Choose one topic related to foundation models and NLP, implement a small-scale experiment, and present the problem, method, experimental setup, results, limitations, and possible improvements. Up to 1 bonus point.

---

## Day 11–12 · Social Simulation (July 23–24)

### Learning Path

- Agent-based modeling: [Mesa documentation](https://mesa.readthedocs.io/) and [Mesa first-model tutorial](https://mesa.readthedocs.io/latest/tutorials/0_first_model.html).
- LLM-based social simulation: [AgentSociety](https://github.com/tsinghua-fib-lab/agentsociety/), [AgentSociety documentation](https://agentsociety.readthedocs.io/), and [Google DeepMind Concordia](https://github.com/google-deepmind/concordia).
- Embodied and social environments: [TongSIM](https://tongsim-platform.github.io/tongsim/).

### Homework

1. **Reproducible Agent-Based Social Simulation**
   - **Requirements:** Implement a Schelling-style segregation model using Mesa or plain Python and study how one behavioral parameter changes the population-level outcome.
     - Use a `20 × 20` grid with occupancy density `0.8` and two agent groups of approximately equal size.
     - An agent is satisfied when at least a specified fraction `τ` of its occupied neighbors belongs to the same group; dissatisfied agents move to an empty cell.
     - Run the model for `τ ∈ {0.3, 0.5, 0.7}` with three random seeds per setting. Stop each run when all agents are satisfied or after 100 steps.
     - Save one row per run to `results.csv` with at least `tau`, `seed`, `steps`, `final_satisfied_fraction`, and `final_same_group_neighbor_fraction`.
     - Plot the initial and final grid for one representative run, final same-group-neighbor fraction versus `τ`, and steps to convergence versus `τ`.
     - Add one intervention, such as restricted movement, heterogeneous thresholds, tolerant agents, or noisy decisions. Compare it with the baseline under one fixed `τ` using at least three seeds.
     - Write a 300–400 word discussion distinguishing model rules, observed emergent patterns, and claims that cannot be inferred about real societies. State at least two limitations or ethical risks.
     - Use fixed and clearly reported random seeds. The notebook must regenerate `results.csv` and all figures from a clean runtime.
   - **Submission:** Submit `SocialSimulation_StudentID_Name.zip` containing:

```text
SocialSimulation_StudentID_Name/
├── social_simulation.ipynb
├── results.csv
└── README.md
```

   `README.md` must contain the environment setup and the steps needed to reproduce the notebook. Upload the ZIP file to **Tsinghua University Web Learning（清华网络学堂）**.
   - **Deadline:** July 24, 23:59.
   - **Optional bonus:** Reimplement a small version using an LLM-based framework such as AgentSociety or Concordia with no more than 20 agents. Compare it with the rule-based baseline and discuss reproducibility and cost. Up to 1 bonus point.

---

## Day 13–14 · Agent Systems and Multi-Agent Systems (July 25–26)

### Learning Path

- Tool-using agents: [LangChain agent documentation](https://docs.langchain.com/oss/python/langchain/agents) and [LangGraph quickstart](https://docs.langchain.com/oss/python/langgraph/quickstart).
- Multi-agent systems: [AutoGen AgentChat](https://microsoft.github.io/autogen/stable/user-guide/agentchat-user-guide/index.html).
- Tool interoperability: [Model Context Protocol introduction](https://modelcontextprotocol.io/docs/getting-started/intro).
- Agent evaluation references: [AgentBench](https://arxiv.org/abs/2308.03688), [WebArena](https://arxiv.org/abs/2307.13854), [OSWorld](https://arxiv.org/abs/2404.07972), and [SWE-agent](https://arxiv.org/abs/2405.15793).

### Homework

1. **Small Tool-Using Agent and Evaluation**
   - **Requirements:** Build one agent that answers a fixed task set using tools, then add a reviewer stage and test whether it improves reliability. LangGraph, AutoGen AgentChat, or a self-written loop may be used.
     - Create `tasks.jsonl` containing exactly six tasks: two arithmetic tasks, two questions answerable from a provided local Markdown file, and two mixed tasks requiring both document lookup and calculation. Each line must contain `id`, `question`, and `reference_answer`.
     - Implement at least two tools: `calculator(expression: str) -> str` and `local_search(query: str) -> str`. The calculator must not use unrestricted `eval`. `local_search` must search only the supplied local course Markdown file.
     - Implement a single-agent workflow that decides when to call the tools. Use a maximum of six model turns and four tool calls per task.
     - Implement a reviewer-enhanced workflow. The reviewer receives the question, visible action log, and draft answer, then either accepts the draft or returns one corrected answer.
     - Run both workflows on all six tasks once, giving 12 runs in total. Use the same model settings for both workflows and record the model name and temperature.
     - Save `results.csv` with columns `task_id`, `system`, `success`, `num_model_turns`, `num_tool_calls`, `latency_seconds`, and `error_type`.
     - Save one JSON log per run under `logs/`. Logs should contain messages, tool names, arguments, outputs, reviewer decisions, and final answers. Do not request or store hidden chain-of-thought.
     - Write `report.md` of 400–600 English words containing the setup, success rate of both systems, average tool calls and latency, one successful example, one failed example, and a conclusion on whether the reviewer was useful.
     - `python run_eval.py` must reproduce all 12 runs and regenerate `results.csv`. API keys must be read from environment variables and must not appear in submitted files or logs.
   - **Submission:** Submit `AgentSystem_StudentID_Name.zip` containing only:

```text
AgentSystem_StudentID_Name/
├── README.md
├── requirements.txt
├── course_material.md
├── tasks.jsonl
├── tools.py
├── agent.py
├── reviewer.py
├── run_eval.py
├── results.csv
├── report.md
└── logs/
```

   `README.md` must state the Python version, installation command, required environment-variable names, and exact evaluation command. Upload the ZIP file to **Tsinghua University Web Learning（清华网络学堂）**.
   - **Deadline:** July 27, 23:59.
   - **Optional bonus:** Expose either `calculator` or `local_search` as a local MCP server and call it from the agent without changing the task set. Include the server code and one successful protocol trace. Up to 1 bonus point.

---

## Final Assignment · Literature Review

It is important and necessary to write a literature review before the start of a research project.
Without comprehensive understanding of the related research areas, one may not be able to draw
inspirations from previous work and bring novel ideas. After completing this assignment, you should
be able to answer: **What is your motivation to study this subfield? What has already been done?
What is still missing?**

### Requirements

- Choose one subdirection from the course, such as vision-language models, diffusion models, 3D vision, cognitive reasoning, embodied manipulation, robot foundation models, language-model alignment, retrieval-augmented generation, LLM agents, multi-agent systems, or social simulation.
- Read at least **5 closely related papers** in that subdirection. You may use the course paper-reading list as a starting point, and you are strongly encouraged to read more papers when the topic requires it.
- Write a literature review in **LaTeX** and submit the compiled PDF together with the source `.tex` file and bibliography file.
- **Template:** [Download the LaTeX literature-review template](https://github.com/Tsinghua-Tong/Summer_Course/raw/main/archive/Report_Template_for_Tong_Summer_Course.zip).
- The review should be **4-6 pages**, excluding references and appendices. Use a standard conference-style template such as NeurIPS, ICML, ICLR, CVPR, ACL, or a clean article template with 10-11 pt font.
- The review may be written in English or Chinese, but the writing must be coherent, citation-grounded, and not a collection of paper summaries.
- Include a complete reference list. Every paper discussed in the text must be cited, and every reference should be cited in the text.
- AI writing tools may be used for polishing, but you are responsible for correctness, citations, and final wording. Do not fabricate papers, results, datasets, or citations.

### Suggested Structure

One common structure is to organize the review around **Introduction** and **Related Works**.
A stronger review may add sections such as taxonomy, methods, datasets, evaluation, limitations,
and future directions, but the logic should remain easy to follow.

In the **Introduction**, tell the big story of the subfield. A good introduction usually answers:

1. Why is the problem important?
2. Why is the problem hard?
3. Why has it not been solved before?
4. What are the main research lines or representative methods?
5. What criteria will you use to compare the papers?
6. What is significant or worthy about recent progress?
7. How does this subfield fit into the broader picture of general AI systems?

The final paragraph or subsection of the Introduction is usually a short summary of the review's
organization and main observations.

In the **Related Works** section, do not simply list papers one by one. Organize papers by problem,
method, assumption, dataset, evaluation protocol, or historical development. The reader should
learn how the methods differ from previous work, what assumptions they share, and what each line
of work contributes to the field.

### Comparison and Analysis

Your review should include at least one table or figure that helps the reader compare the papers.
Possible choices include:

- A chronology of important papers and milestones;
- A taxonomy table comparing problem settings, input-output formats, model architecture, supervision, data scale, and evaluation tasks;
- A method diagram redrawn in your own style;
- A comparison of datasets, metrics, or experimental protocols;
- A summary of open problems and which papers address them.

After the summary, include your own analysis. Discuss limitations, unresolved questions, and at
least two concrete future research directions. It is acceptable to raise questions that you cannot
fully answer yet, but they should be specific and grounded in the papers you read.

### Tips for Finding Related Works

1. Given a paper, read its cited papers to expand your paper library.
2. Given a paper, read papers that cite it using Google Scholar, Semantic Scholar, or arXiv.
3. For the first authors, senior authors, or labs in your paper library, check their homepages, Google Scholar pages, and lab websites for recent follow-up work.
4. Prefer papers from top venues, influential workshops, widely used benchmarks, or systems with released code/data, but do not rely on popularity alone.
5. Keep notes on each paper's problem, key idea, evidence, limitation, and relation to the other papers before writing the final review.

### Sample Surveys and Reading Aids

These examples are not templates to copy, but they show how a survey can organize a field and
compare lines of work:

1. [Dark, Beyond Deep: A Paradigm Shift to Cognitive AI with Humanlike Common Sense](https://doi.org/10.1016/j.eng.2020.08.013)
2. [Transformers in Vision: A Survey](https://arxiv.org/abs/2101.01169)
3. [Deep Learning for 3D Point Clouds: A Survey](https://arxiv.org/abs/1912.12033)
4. [A Survey of Large Language Models](https://arxiv.org/abs/2303.18223)
5. [A Survey on Large Language Model based Autonomous Agents](https://arxiv.org/abs/2308.11432)

### Submission

- **Files:** Submit `LiteratureReview_StudentID_Name.pdf`, the source `.tex` file, and the `.bib` file. If figures are not embedded in the `.tex`, include the figure files as well.
- **Deadline:** August 2, 23:59.
- **Platform:** Submit through **Tsinghua University Web Learning（清华网络学堂）**.

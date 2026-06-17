# 通用人工智能系统平台 I — Course Resource Hub

Resource repository for **通用人工智能系统平台 I** (*General Artificial Intelligence Systems
Platform I*), the two-week summer course for 清华通班 first-year (spring) students.

| | |
|---|---|
| **Audience** | 清华通班 大一下学生 |
| **Dates** | 2026-07-13 → 2026-07-26 (two weeks) |
| **Venue** | 通院 2201 大教室 |
| **Format** | 课堂讲授 + 编程练习 + 实践报告 (Lectures + Programming Exercises + Practical Reports) |

This repo holds the **Learning List** (courses, tutorials, programming exercises, tools) and the
**Paper Reading List** for the course. It replaces the older BIGAI PDFs (archived in
[`archive/`](archive/)), which predate the LLM / foundation-model era. The curriculum is now
organized around a **foundation-model mainline**: shared coding & deep-learning foundations, then the
four pillars of modern general-AI systems.

## Curriculum & ownership

Each module is one Markdown file in [`content/`](content/), owned by one (or two) TAs who keep it
up to date.

| Module | File | Owner |
|---|---|---|
| 📅 Syllabus (2-week plan) | [`content/syllabus.md`](content/syllabus.md) | All TAs |
| 00 · Foundations & Coding | [`content/00-foundations.md`](content/00-foundations.md) | All TAs (shared) |
| 01 · Foundation Models & NLP | [`content/01-foundation-models-nlp.md`](content/01-foundation-models-nlp.md) | **林子雍** |
| 02 · Multimodal & Vision | [`content/02-multimodal-vision.md`](content/02-multimodal-vision.md) | **巫莹莹** |
| 03 · Embodied AI & Robotics | [`content/03-embodied-ai.md`](content/03-embodied-ai.md) | **李炯烨 + 巫莹莹** |
| 04 · Agent Systems & Multi-Agent | [`content/04-agent-systems-mas.md`](content/04-agent-systems-mas.md) | **陈子昂** |

> Module 03 (Embodied AI) is the explicit **CV × Robotics crossover**, jointly owned by 巫莹莹 and
> 李炯烨.

## What students see

The Markdown is rendered into a single, self-contained **`site/index.html`** — an English-primary,
tabbed page that works offline (open the file directly in a browser, no server needed). This is the
version to share with students.

## Publishing via GitHub Pages

The page can be served straight from GitHub Pages — it is plain static HTML with relative asset
paths, so it works under a project sub-path (`https://<user>.github.io/<repo>/`) with no changes.

A workflow at [`.github/workflows/pages.yml`](.github/workflows/pages.yml) **rebuilds and deploys
automatically** on every push that touches `content/` or `site/`. To turn it on once:

1. Push this repo to GitHub.
2. **Settings → Pages → Build and deployment → Source: `GitHub Actions`.**
3. Done. From then on, TAs just edit `content/*.md` and push — the Action runs `build.py` and
   publishes the result. (You don't even need to commit `site/index.html`; the Action regenerates it.)

> Prefer no Actions? You can instead set **Pages → Source: Deploy from a branch**, but branch-deploy
> only serves the repo root or a `/docs` folder — so you'd rename `site/` to `docs/` and commit the
> built `index.html`. The Actions route above avoids that and keeps the `site/` layout.

## Repository layout

```
README.md
.github/workflows/pages.yml   # auto-build + deploy to GitHub Pages on push
content/                      # ← single source of truth (edit these Markdown files)
  syllabus.md
  00-foundations.md           # all TAs
  01-foundation-models-nlp.md # 林子雍
  02-multimodal-vision.md     # 巫莹莹
  03-embodied-ai.md           # 李炯烨 + 巫莹莹
  04-agent-systems-mas.md     # 陈子昂
site/
  build.py                    # Markdown -> site/index.html
  template.html               # layout + styling shell
  assets/marked.min.js        # vendored Markdown renderer (offline)
  index.html                  # GENERATED — do not edit by hand
archive/                      # original BIGAI PDFs (2023 / 2025), kept for reference
```

## How TAs update content (no web skills needed)

1. **Edit your Markdown file** in `content/` (see the section template below). Plain Markdown —
   headings, lists, tables, links.
2. **Rebuild the page** from the repo root:
   ```bash
   python site/build.py
   ```
   This regenerates `site/index.html`.
3. **Preview** by opening `site/index.html` in any browser.
4. **Commit** your `content/*.md` change (and the regenerated `site/index.html` if you want the
   shareable page tracked).

### Section template (keep this shape in every module)

```markdown
# <Module title>

> **Owner:** <name> · **Days:** <n–m> · **Old mapping:** <old section>

## Overview
One paragraph: what this field is in 2026 and why it matters.

## Learning Path
Ordered courses / lectures / tutorials, tagged Introductory → Intermediate → Advanced.

## Programming Exercises
Concrete hands-on tasks (the old "Homework"), with starter repos/links.

## Paper Reading
Curated, dated papers grouped by sub-topic; one line of context each.

## Tools & Setup
Libraries, install links, and a hardware note.
```

The owner badge on the page is read automatically from the `**Owner:**` line, so keep that line in
your file.

## Adding a new tab

Add the Markdown file to `content/`, then add one row to the `DOCS` list in
[`site/build.py`](site/build.py) and rebuild.

## Requirements

- Python 3 (standard library only — no packages to install) for `build.py`.
- A modern web browser to view `site/index.html`.

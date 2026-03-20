<!-- Why: Reposition the repository around Agentic AI for intelligent software engineering while preserving SATD repair as the flagship benchmark and validation scenario. Scope: Adds the main repository entrypoint and aligns onboarding with the mirrored skill directories and collaboration contracts. Verify: Confirm every referenced path exists, the prose is English-only, and the framing matches AGENTS.md and CLAUDE.md. -->

# PaperSkills

PaperSkills is an English-first research workspace for Agentic AI in intelligent software engineering. The repository studies how large-model systems can understand, localize, repair, and verify software engineering problems with explicit evidence, reproducible workflows, and realistic evaluation. Self-Admitted Technical Debt (SATD) repair remains the flagship benchmark and validation scenario because it forces an agent to connect intent understanding, code change generation, and independent repair verification.

## What This Repository Is For

- Designing and evaluating Agentic AI systems for intelligent software engineering.
- Studying repair-oriented workflows where models must reason over comments, code, tools, and verification signals.
- Building reproducible research artifacts such as prompts, tool-use protocols, evaluation plans, and writing packages.
- Supporting paper writing and presentation generation through reusable skill packs.

This repository currently functions as a collaboration contract plus mirrored skill distribution for `Codex`-style and `Claude`-style environments. It is intentionally lightweight: the most important assets are the rules, workflows, and skill packs that keep research claims grounded.

## Research Focus Areas

- Agentic repair workflows for software engineering tasks.
- SATD detection, alignment, repair, and post-repair verification.
- Benchmark and evaluation design for model-driven software engineering systems.
- Prompt, tool, retrieval, and workflow versioning for reproducible studies.
- Writing support for papers, reports, and slides backed by explicit evidence.

## Why SATD Remains the Flagship Use Case

SATD repair is the flagship track in PaperSkills because it is a compact but demanding testbed for Agentic AI:

- The agent must understand developer intent rather than react to a shallow keyword.
- The agent must localize the relevant code, not only restate the comment.
- The agent must produce a real patch instead of deleting the debt comment.
- The agent must verify that the debt is actually reduced or removed.
- The workflow naturally exposes failure modes such as under-repair, over-repair, and regression.

SATD is therefore the default concrete benchmark in this repository, but it is not the only acceptable topic. Broader intelligent software engineering work is welcome when it still follows the same evidence, reproducibility, and validation standards.

## Repository Structure

- `AGENTS.md` — the main collaboration contract for agent behavior in this repository.
- `CLAUDE.md` — a mirrored copy of the same contract for environments that load Claude-specific project instructions.
- `.agents/skills/` — skill packs and supporting assets for Codex-style agent environments.
- `.claude/skills/` — mirrored skill packs for Claude-style agent environments.
- `.agents/skills/superpowers/` — workflow skills for planning, debugging, execution, review, and verification.
- `.agents/skills/research-paper-writer/` — assets and instructions for paper drafting.
- `.agents/skills/ppt-generator/` — assets and instructions for slide generation.

## How Agents Should Work in This Repository

Agents working here should follow a strict research discipline:

- Start every task by declaring the current work mode: `[PLANNING]`, `[EXECUTING]`, `[VERIFYING]`, `[WRITING]`, or `[REVIEWING]`.
- Check available skills first and trigger `using-superpowers` when it is available.
- Begin with read-only exploration before asking questions or making changes.
- Use `[FACT]`, `[HYPOTHESIS]`, and `[PLAN]` labels whenever a conclusion might otherwise sound stronger than the evidence.
- Add `Why / Scope / Verify` annotations for non-trivial changes to code, prompts, evaluation settings, or research documentation.
- Do not claim that something is fixed, complete, passing, or valid without fresh verification evidence.

## Evidence and Reproducibility Principles

PaperSkills treats reproducibility as a first-class research requirement.

- Record the model, configuration, prompt version, tool version, and workflow version behind every important result.
- Keep evaluation commands, aggregation methods, and verification commands traceable.
- Distinguish validated results from working assumptions and future plans.
- Never fabricate citations, metrics, baselines, or human-review outcomes.
- Never present an unverified patch, demo output, or generated narrative as a confirmed repair.
- Keep failure cases, limitations, and remaining risks visible in reports and papers.

## Available Skill Families

- `superpowers/*` — workflow skills for brainstorming, plan execution, debugging, review, verification, and branch handoff.
- `research-paper-writer` — structured support for research paper drafting.
- `ppt-generator` — structured support for slide and presentation generation.

The skill families complement the repository contract; they do not override the evidence, reproducibility, or validation rules defined in `AGENTS.md` and `CLAUDE.md`.

## Typical Workflows and Deliverables

Common repository outputs include:

- `Research Brief` — the scoped problem statement, contribution target, and success criteria.
- `Experiment Plan` — datasets or project sources, baselines, metrics, ablations, and verification commands.
- `Agent Workflow Spec` — system boundary, modules, tools, retrieval sources, and failure guards.
- `Run Record` — the concrete execution trace for a specific model, prompt, tool, and task instance.
- `Evaluation Summary` — main results, ablations, failure counts, limitations, and next steps.
- `Writing Pack` — paper, report, or slide draft plus evidence links and placeholders.
- `SATD Repair Record` — debt hypothesis, target location, repair summary, and verification status for SATD-specific work.

## Common Use Cases

- Reviewing literature on SATD repair, agentic repair, or intelligent software engineering.
- Designing an Agentic AI workflow for code understanding, repair, or validation.
- Creating an evaluation protocol for SATD repair or a related benchmark.
- Generating paper or slide drafts backed by explicit experiment records.
- Auditing prompts, tools, or workflow changes for reproducibility gaps.

## Working Rule of Thumb

If a task touches intelligent software engineering and the user does not redefine the scope, treat it as part of an Agentic AI research program with SATD repair as the flagship validation path. If the task falls outside that flagship track, say so clearly and keep the same standards for evidence, reproducibility, and reporting honesty.

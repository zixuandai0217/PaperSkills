# PaperSkills Collaboration Contract (Agentic AI-first)

> **Read and follow project rules.**

<!-- Why: Reposition the repository collaboration contract from SATD-first to Agentic AI-first while preserving SATD repair as the flagship benchmark and validation scenario. Scope: Rewrites the repository mission, workflow, evaluation rules, artifact templates, and acceptance cases in English for both AGENTS.md and CLAUDE.md. Verify: Confirm the file is English-only, retains the hard constraints on evidence and validation, and stays identical to the mirrored contract file after the rewrite. -->

This document governs how AI agents and human researchers collaborate in PaperSkills on research design, prototyping, evaluation, writing, and review.

PaperSkills is primarily a repository for **Agentic AI in Intelligent Software Engineering**. Its flagship benchmark and default concrete validation scenario is **Self-Admitted Technical Debt (SATD) repair**, but the repository also supports broader intelligent software engineering work when the same evidence, reproducibility, and evaluation standards are preserved.

---

## Required Startup Behavior

Before starting any task, the agent must explicitly declare the current work mode:

- **`[PLANNING]`** - problem framing, literature review, and study design
- **`[EXECUTING]`** - implementation, experimentation, and data collection
- **`[VERIFYING]`** - result checking, ablation review, and error analysis
- **`[WRITING]`** - paper drafting, slide writing, and reporting
- **`[REVIEWING]`** - code review, document review, and result audit

Default collaboration rules:

- At task start, inspect the currently available skills and prioritize `using-superpowers`.
- If `using-superpowers` or another expected skill is unavailable, say so explicitly and fall back to the repository contract in this file.
- Every task-start summary must state:
  - the current work mode
  - whether `using-superpowers` was triggered
  - whether any additional skills were used or a fallback workflow was chosen
- Start with read-only exploration before asking follow-up questions or making changes.
- Do not claim that something is complete, fixed, passing, or validated without fresh verification evidence.
- Any non-trivial change to code, prompts, evaluation settings, or research documents must include `Why / Scope / Verify` annotations and matching validation.

---

## Repository Mission and Default Interpretation

PaperSkills focuses on the following default research questions:

- How can Agentic AI systems reliably understand, localize, repair, and verify software engineering problems?
- How should prompts, tools, retrieval, memory, and workflow structure be combined in intelligent software engineering systems?
- How can repair-oriented workflows be evaluated with realistic, reproducible, and regression-aware protocols?
- How can research artifacts remain traceable from system design to experiment record to paper claim?

The default repository question can be summarized as:

> In real software projects, how can Agentic AI systems perform understanding, localization, repair, and verification work more reliably, and how can those behaviors be turned into defensible research contributions?

Default interpretation rule:

> Unless the user explicitly redefines the scope, treat each task as contributing to Agentic AI for intelligent software engineering, with SATD repair as the flagship benchmark and validation path.

### In-Scope Extensions

The following are still within the main repository direction:

- SATD detection, classification, alignment, repair, and verification
- agentic code repair beyond SATD
- tool-using software engineering workflows
- benchmark design for repair, regression prevention, or agent evaluation
- reproducibility, error taxonomy, and workflow instrumentation for intelligent software engineering

### Out-of-Main-Line Work

If the user asks for a broader LLM application that is not really an intelligent software engineering problem, the repository may still be used, but the agent should state clearly that the task is outside the main line. Evidence, reproducibility, failure reporting, and writing honesty rules still apply.

---

## Agentic AI Research Workflow

Follow this workflow in order. Do not skip critical decisions even when the output format is lightweight.

### Step 1: Problem Framing (`Research Brief`)

Must define:

- problem statement
- task type: `detection | classification | alignment | repair | verification | workflow | benchmark | agent_evaluation`
- target artifact: `comment | function | file | patch | benchmark | workflow | agent`
- intended contribution: `new_task | new_method | new_benchmark | new_system | empirical_finding`
- success criteria
- validation constraints

### Step 2: Related Work and Research Gap

Must define:

- 3 to 5 core related works
- how prior software engineering work and Agentic AI work intersect
- the concrete research gap
- the differentiating position of the proposed work

### Step 3: Task and Benchmark Design

Must define:

- dataset or project sources
- project scope and language scope
- split protocol
- task granularity and input-output format
- baseline families
- whether human annotation, human review, or expert judgment is required

### Step 4: System, Prompt, and Agent Design

Must define:

- system boundary
- module responsibilities
- input context
- retrieval sources, if any
- tool permissions and action space
- whether multi-turn interaction is allowed
- memory or context retention policy
- safety constraints and failure guards
- logging and version tracking strategy

### Step 5: Implementation and Verification

Must define:

- build, compile, test, or static-check requirements
- success conditions for the task
- regression-check strategy
- debt-resolution checks when the task is repair-oriented
- human review trigger conditions
- failure-case and error-analysis logging strategy

### Step 6: Evaluation Summary

Must capture:

- main result comparison
- ablations
- representative failures
- regression risks
- limitations

### Step 7: Writing Pack

Must capture:

- paper, report, or slide draft
- key figures or tables
- links from claims back to experiment evidence
- explicit `[PENDING]` or `[PLACEHOLDER]` items for anything not yet verified

---

## Agentic AI System Requirements

Every serious study in this repository should make the following visible:

- [ ] **System boundary** - what the system includes, excludes, and depends on externally
- [ ] **Module responsibilities** - clear inputs, outputs, and boundaries for each module
- [ ] **Prompt / Tool / Agent versioning** - exact versions for each evaluated configuration
- [ ] **Retrieval and memory policy** - what context is fetched, retained, or discarded
- [ ] **Action space** - what edits, tool calls, tests, or interactions the system may perform
- [ ] **Evaluation protocol** - scripts, commands, metrics, and aggregation rules
- [ ] **Regression set** - a stable set of checks or cases used to prevent behavior drift
- [ ] **Error taxonomy** - how failures are grouped, counted, and tracked
- [ ] **Reproduction conditions** - model, environment, data, dependencies, and configuration

### Prohibited Practices

- ❌ changing a prompt, tool flow, or agent workflow without version tracking
- ❌ claiming a repair or improvement without regression-aware verification
- ❌ letting paper descriptions drift away from the actual evaluation scripts
- ❌ packaging unexplained behavior as a research contribution or model capability
- ❌ using undocumented magic parameters to influence results
- ❌ hiding failure cases that materially change the interpretation of the work

---

## SATD Flagship Track

SATD is the flagship domain in this repository because it tightly couples understanding, localization, repair, and verification in one realistic workflow.

### What Counts as SATD

SATD refers to comments where developers explicitly admit that the current implementation is temporary, incomplete, compromised, or in need of future repair or refactoring.

Typical SATD expressions include:

- explicit debt comments such as `TODO`, `FIXME`, `HACK`, or `XXX`
- natural-language comments that admit a temporary workaround or deferred repair
- comments that acknowledge design compromise, performance compromise, compatibility compromise, missing tests, or incomplete implementation

### What Does Not Automatically Count as SATD

The following should not be treated as SATD unless the surrounding context clearly turns them into debt admission:

- ordinary reminders or task assignments
- feature wish lists
- purely descriptive comments with no admission of compromise
- documentation comments unrelated to implementation quality

### Core SATD Subtasks

- SATD detection and classification
- SATD comment-to-code alignment
- SATD repair generation
- post-repair verification
- deciding whether the debt was actually reduced or removed

### SATD Repair Realism Constraints

- Removing the SATD comment alone does **not** count as debt resolution.
- Producing a plausible-looking patch without build, test, or behavior evidence does **not** count as a verified repair.
- Silencing errors or suppressing warnings does **not** automatically count as fixing the debt.
- If the patch only reduces the debt partially, label it as a partial resolution and explain the remaining risk.

---

## Evaluation and Reproducibility Protocol

All conclusions must be explicitly labeled as one of:

- **`[FACT]`** - verified by experiment results, execution logs, or reliable sources
- **`[HYPOTHESIS]`** - a working assumption that still requires falsifiable validation
- **`[PLAN]`** - future work that has not been executed yet

### Required Recordkeeping

You must record:

- model name, version, and configuration such as `temperature`, `top-p`, and `seed`
- prompt, tool, and agent workflow versions
- dataset or project source
- retrieval configuration and context-selection strategy
- alignment strategy between comments and code when relevant
- data split protocol
- evaluation scripts, commands, and aggregation method
- repair-verification commands or scripts
- human annotation or review protocol when used
- compute budget and resource constraints
- failure cases and error-analysis notes

### Forbidden Evidence Practices

- ❌ fabricating citations, experiment results, baselines, or human-review outcomes
- ❌ presenting undocumented common knowledge as sourced fact
- ❌ using figures that cannot be traced to raw logs, scripts, or primary records
- ❌ showing only successful examples while hiding representative failures

### SATD Flagship Evaluation Protocol

When the task is SATD repair, document whether the study covers the relevant baseline families:

- rule-based or heuristic methods
- plain prompting
- retrieval-augmented prompting
- agentic repair or multi-turn repair
- the closest published SATD or repair method

Report the metrics that make sense for the task, typically including:

- repair success rate
- compile or build pass rate
- test pass rate
- debt-resolution accuracy
- edit cost or patch size
- latency and cost
- human-review agreement or acceptance rate when human evaluation is used

Preferred ablations:

- comment only
- comment plus code context
- comment plus code context plus historical context
- single-turn repair versus multi-turn repair
- different tool or agent configurations

Minimum SATD error taxonomy:

- debt-understanding failure
- repair-location failure
- behavioral regression
- comment deletion without real repair
- under-repair
- over-repair

Minimum acceptance bar for discussing a SATD repair as effective:

- the target project passes the relevant build or compile checks, or
- the relevant tests or regression suite pass, or
- independent evidence shows that the debt constraint was actually removed

If none of these conditions is met, the result is at most a candidate output or prototype patch, not a successful repair.

---

## Writing and Reporting Rules

### Papers, Reports, and Slides

- Every conclusion must trace back to experiment records, script output, or reliable sources.
- Any unverified item must be labeled as `[PENDING]` or `[PLACEHOLDER]`.
- Figures and tables must state their data source.
- Do not exaggerate incomplete work.
- Distinguish clearly between validated results, work in progress, and hypotheses.

### Citation Rules

- Every citation must be real.
- The cited claim must match the source.
- Prefer recent work when it is relevant, while retaining necessary classic references.
- Related work must support the stated research gap rather than act as citation padding.

### Claim Language Rules

- Use `[FACT]` only when the statement is grounded in verified evidence.
- Use `[HYPOTHESIS]` only when a concrete validation path exists.
- Use `[PLAN]` only for work that has not yet been executed.

---

## Skills, Change Annotations, and Validation

Available skill families in this repository include:

- `superpowers/*` for workflow support such as planning, execution, verification, debugging, and review
- `research-paper-writer` for paper drafting
- `ppt-generator` for slide generation

Priority order:

1. direct user requests and repository rules
2. the evidence, reproducibility, and validation contract in this document
3. default skill suggestions

Usage rules:

- Skills supplement the workflow; they do not override research honesty or reproducibility requirements.
- If a skill suggestion conflicts with this contract, follow this contract.
- If the user names a skill that is unavailable in the environment, state that clearly and choose the nearest valid fallback.

### Required `Why / Scope / Verify` Annotations

Any non-trivial change to the following must include `Why / Scope / Verify`:

- code implementation
- prompt design
- evaluation configuration
- research document structure

Use this format in code, scripts, or config files:

```text
# Why: What problem does this change solve?
# Scope: What is affected?
# Verify: How should this be validated?
```

Use this format in documentation:

```html
<!-- Why: What problem does this change solve? Scope: What is affected? Verify: How should this be validated? -->
```

After modifying the work:

- run the relevant validation
- report the validation result
- update the related documents or experiment records
- add a `SATD Repair Record` when the task is SATD repair

---

## Anti-Patterns

### Hard No

- 🚫 demo-driven conclusions from a few handpicked successes
- 🚫 missing baselines when claiming improvement
- 🚫 selective reporting that hides failures
- 🚫 uncontrolled variables across compared methods
- 🚫 engineering complexity packaged as a research contribution without analysis
- 🚫 fabricated metrics, citations, or human-review judgments
- 🚫 untracked prompt, tool, or agent changes
- 🚫 irreproducible results with no path back to scripts or configuration
- 🚫 fake repair claims based only on deleting a SATD comment

### Warning Signs

- ⚠️ system behavior cannot be explained but is still presented as capability
- ⚠️ evaluation metrics do not match the research goal
- ⚠️ experiment setup and paper description drift apart
- ⚠️ ablations are missing or superficial
- ⚠️ error analysis stays at a slogan level
- ⚠️ debt removal has no independent verification evidence

---

## Minimal Research Artifacts

### `Research Brief`

```yaml
problem_statement: str
research_track: Agentic AI for Intelligent Software Engineering
task_type: detection | classification | alignment | repair | verification | workflow | benchmark | agent_evaluation
target_artifact: comment | function | file | patch | benchmark | workflow | agent
intended_contribution: new_task | new_method | new_benchmark | new_system | empirical_finding
success_criteria: List[str]
validation_constraints: List[str]
time_estimate: str
```

### `Experiment Plan`

```yaml
data_or_project_sources: List[str]
project_scope: str
language_scope: List[str]
baseline_families: List[str]
evaluation_metrics: List[str]
action_space: str
verification_commands: List[str]
human_review_strategy: str
ablation_design: List[str]
resource_requirements: str
```

### `Agent Workflow Spec`

```yaml
system_boundary: str
modules: List[str]
input_context: List[str]
retrieval_sources: List[str]
tools: List[str]
action_space: str
memory_policy: str
safety_guards: List[str]
logging_and_versioning: List[str]
```

### `Run Record`

```yaml
date: str
model_and_config: Dict[str, Any]
prompt_version: str
tool_or_agent_version: str
dataset_or_project: str
task_instance: str
commands_run: List[str]
outputs_or_artifacts: List[str]
verification_status: str
notes: List[str]
```

### `Evaluation Summary`

```yaml
main_results: Dict[str, float]
ablation_results: Dict[str, Any]
failure_counts: Dict[str, int]
representative_failures: List[str]
regression_risks: List[str]
resolution_status: str
limitations: List[str]
next_steps: List[str]
```

### `Writing Pack`

```yaml
document_type: paper | ppt | report
core_claims: List[str]
key_figures: List[str]
data_sources: Dict[str, str]
claim_to_evidence_links: Dict[str, str]
pending_evidence_items: List[str]
```

### `SATD Repair Record`

```yaml
satd_comment: str
debt_hypothesis: str
target_location: str
repair_summary: str
verification_status: str
remaining_risk: str
```

---

## Acceptance Scenarios

- Scenario: the user asks for SATD literature review.
  Expectation: the agent follows the Agentic AI research workflow, identifies a real gap, and cites real papers only.
- Scenario: the user asks to design a SATD repair experiment.
  Expectation: the agent specifies data sources, baselines, metrics, ablations, and reproducibility conditions rather than giving a demo-only sketch.
- Scenario: the user asks to repair a SATD instance.
  Expectation: the agent produces a `SATD Repair Record`, runs verification, and does not claim success without evidence.
- Scenario: the user asks to design an agent workflow for intelligent software engineering.
  Expectation: the agent defines system boundary, tools, retrieval, safety guards, versioning, and evaluation before making strong claims.
- Scenario: the user asks to write a paper or slides.
  Expectation: the agent preserves `[FACT] / [HYPOTHESIS] / [PLAN]`, marks unknowns as `[PENDING]` or `[PLACEHOLDER]`, and keeps claims traceable to evidence.
- Scenario: the user asks a broader intelligent software engineering question outside SATD.
  Expectation: the agent may proceed, but should state that the task is outside the flagship SATD track while keeping the same validation discipline.

---

## Collaboration Commitments

### Agent Commitments

- follow the rules in this contract
- declare the current work mode explicitly
- avoid fabricating data, citations, or evidence
- distinguish facts, hypotheses, and plans
- run validation and report the outcome after meaningful changes

### User Commitments

- provide the necessary context and feedback
- verify important conclusions when human judgment is required
- review the resulting artifacts
- correct drift when the work moves away from the intended research goal

---

## Version History

- **v1.0** (2026-03-20): Initial version covering research workflow, repository governance, and collaboration rules.
- **v1.1** (2026-03-20): SATD-first rewrite with stronger LLM-based software engineering and SATD repair evaluation rules.
- **v1.2** (2026-03-21): English rewrite with Agentic AI-first positioning while keeping SATD repair as the flagship benchmark and validation scenario.

---

*This contract applies to both AI agents and human researchers. The goal is to produce research artifacts that are useful, reproducible, evidence-backed, and honest about their limits.*

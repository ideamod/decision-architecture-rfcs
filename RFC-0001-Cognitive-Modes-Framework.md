# RFC 0001: Cognitive Modes Framework for Engineering Work

*This document defines the specification of CMF (Cognitive Modes Framework).
It is an informational engineering RFC with normative sections defining internal consistency of the model.*

| Field | Value |
| --- | --- |
| Author | Dmitriy Kirenkin |
| Status | In review |
| Created | 2025–11–27 (CET) |
| Last Updated | 2025–12–26 (CET) |
| Category | Communication, Collaboration, Task Structuring, Engineering Alignment |
| Intended Audience | Software Engineers, Engineering Managers, Product Managers, Designers |


## 1. Purpose

This RFC introduces **Cognitive Modes Framework (CMF)** — an engineering model describing how individuals process information during work.

CMF is **not** a psychological typology and does not describe immutable traits.
It describes **task-dependent information-processing states** (“modes”) that influence communication, task performance, and collaboration.

## 2. Scope and Boundaries (Safety by Architecture)

CMF describes **temporary information-processing states** that appear only during task execution.

CMF does not model:
- ability
- performance
- potential
- personality
- stable traits
- preference consistency
- role fit
- seniority
- long-term cognitive profile

Because CMF does not model any of these constructs, it is naturally outside the scope of hiring, promotion evaluation, HR assessment, or decisions involving capability or potential.

CMF is a tool for **Collaboration Engineering**: improving communication, reducing friction, and structuring work.

## 3. Non-Applicability Clause (Normative)

CMF **cannot** be used to infer personal traits or abilities, because it does not model them.

The framework applies **only** to how information is processed during a specific task — not to who someone is, what they are capable of, or how they should be evaluated.

## 4. Definition: Cognitive Mode (Normative)

A **Cognitive Mode** is defined as: A temporary information-processing configuration activated by the structure of a task. It is observable in behavior (how information is requested, structured, or produced) and carries a different cognitive cost for different individuals.

Key properties:
- Modes are **context-dependent**.
- Modes are **not biological claims**.
- Modes are **not personality categories**.

Modes **change dynamically** during work.

## 5. The Four Dimensions (Normative)

CMF defines four independent dimensions that describe how information is represented, reasoned about, structured in attention, and framed during a task.

Each dimension has two opposite poles.
Modes are simply temporary positions along these axes.

### 5.1. Representation: Abstract ↔ Concrete

**Abstract modes** work with:
- models, schemas, invariants
- generalized structures
- relationships between concepts

**Concrete modes** work with:
- examples, cases, specific objects
- step-by-step details
- factual information

Abstract-first thinking starts from structure → moves to examples.
Concrete-first thinking starts from examples → derives structure.

### 5.2. Reasoning: Logical ↔ Intuitive

**Logical modes** rely on:
- explicit causal chains
- stepwise arguments
- verification and explanation

**Intuitive modes** rely on:
- pattern recognition
- semantic impressions
- “feels right / feels wrong” reasoning

Logical-first approaches justify decisions using explicit steps.
Intuitive-first approaches jump to conclusions quickly, then rationalize.

### 5.3. Attention Management: Sequential ↔ Parallel

**Sequential modes** operate with:
- one active context at a time
- deep focus
- ordered processing

**Parallel modes** operate with:
- multiple contexts kept active
- fast switching
- distributed attention

Sequential-first processing favors structure and linear narratives.
Parallel-first processing favors context-rich discussions and non-linear thinking.

### 5.4. Framing: Analytic ↔ Holistic

**Analytic modes**:
- decompose systems
- define boundaries
- identify invariants and constraints

**Holistic modes**:
- see global patterns
- connect distant concepts
- start from the overall intent or vision

Analytic-first thinking moves from parts → to whole.
Holistic-first thinking moves from whole → to parts.

## 6. Mode Switching (Normative)
Humans can operate in many modes.

CMF defines **Mode Switching** as: The process of transitioning from one information-processing configuration to another in response to task demands.

### 6.1. Properties of Mode Switching

- Mode switching **is supported and expected**.
- The **cost of switching varies** across individuals and tasks.
- Cost ≠ **ability**.
- No mode is “fixed”; all modes are potentially accessible.
- People often switch **several modes during the same task**.

### 6.2. Restrictions
CMF does not infer:
- brain structure
- cognitive ability
- innate traits
- “natural talent”

It focuses exclusively on **observable behavior during work**.

## 7. Low-Cost Modes (Informational)
A **Low-Cost Mode** is: The mode in which an individual can operate with the lowest cognitive load during typical engineering tasks.

Important clarifications:
- Low-cost ≠ high-ability
- High-cost ≠ low-ability
- People may have **several low-cost modes**, not one
- Low-cost modes can shift over years with experience

The switching cost difference may be small.

High-cost does not mean “difficult” or “lower ability” — it only indicates that the task requires more cognitive energy in that moment.

CMF does not predict or classify someone’s low-cost mode.
It only helps interpret observed communication patterns.

## 8. Task-Driven Activation (Normative)
Modes **activate** based on **task structure**, not preference.

Examples:

- Debugging a live outage → tends to activate **Concrete + Parallel** modes
- Writing a Technical Assessment → tends to activate **Abstract + Logical + Sequential**
- Brainstorming early product vision → tends to activate **Holistic + Intuitive + Parallel**
- A mode describes **how the information is being processed at a given moment**.

## 9. Why Mode Cost Matters (Informational)
People feel:
- **comfortable** when the task matches a low-cost mode
- **fatigued** when the task requires a high-cost mode
- **stressed** when forced to switch frequently between distant modes

Operating in a high-cost mode imposes continuous cognitive load even without switching. Mode switching adds additional cost on top of this baseline.

This explains many everyday engineering frictions without pathologizing anyone.

## 10. Communication Alignment
CMF provides a lightweight protocol for reducing misalignment:

### 10.1. When speaking to Concrete Modes

Use:
- examples
- screenshots
- step-by-step sequences

Avoid raw abstractions.

### 10.2. When speaking to Abstract Modes

Use:
- models
- diagrams
- invariants

Avoid unstructured detail dumps.

### 10.3. When speaking to Sequential Modes

Use:
- ordered steps
- clear beginnings and endings

Avoid context-switching mid-conversation.

### 10.4. When speaking to Parallel Modes

Use:
- summary of all relevant contexts
- high-context descriptions

Avoid hiding constraints or dependencies.

### 10.5. When speaking to Holistic Modes

Use:
- big picture first
- goals and outcomes

Avoid early deep-dive into constraints.

### 10.6. When speaking to Analytic Modes

Use:
- definitions
- boundaries
- invariants

Avoid ambiguity.

### 11. Task Decomposition Principle
Large engineering tasks almost always decompose into smaller subtasks.
These subtasks tend to activate **different cognitive modes** because they impose different information-processing requirements.

This section defines:
- the **Normative mapping rules** (how CMF interprets task → mode activation),
- **Informational examples** (how it looks in real work).

### 11.1 Normative: Task-Type → Mode-Activation Rules
The following rules define *how CMF interprets the cognitive structure of tasks*.

They describe **how task properties activate particular dimensions**, not how specific people behave.

#### Rule 1 — Ambiguity Resolution activates Holistic → Analytic progression.
Tasks that require clarifying vague or incomplete requirements activate framing modes that start broad and converge to structure.

#### Rule 2 — Architectural Definition activates Abstract + Logical + Sequential modes.
Tasks that require defining boundaries, invariants, or system behavior activate modes focused on modeling and linear reasoning.

#### Rule 3 — Implementation activates Concrete + Sequential or Concrete + Parallel modes.
Tasks that involve writing code or translating models into artifacts activate detail-oriented processing, either single-threaded or multi-threaded depending on task structure.

#### Rule 4 — Debugging activates Concrete + Parallel modes.
Tasks requiring rapid hypothesis testing, context jumping, or inspection of multiple clues tend to activate concrete, multi-context processing.

#### Rule 5 — User-Facing Sensemaking activates Holistic + Intuitive modes.
Tasks involving interpretation of user intent, UX reasoning, or aesthetic quality activate modes that rely on global patterns and semantic impressions.

#### Rule 6 — Documentation activates Abstract + Sequential modes.
Tasks requiring linear explanation of systems or processes activate modes that prioritize ordering and structure.

These rules do **not** describe people.
They describe **task geometry** — the structural demands a task places on information processing.

### 11.2 Informational: Examples of How Tasks Activate Modes
The following examples illustrate (but do not define) how tasks typically behave. They are provided to make the normative rules intuitive, and must not be treated as required, universal, or prescriptive.

#### 11.2.1. Example: Architecture Review Preparation

Likely activated modes:
- Abstract (create models first)
- Logical (define invariants)
- Sequential (prepare arguments in order)

#### 11.2.2. Example: Live Outage Debugging

Likely activated modes:
- Concrete (inspect actual system state)
- Parallel (jump between logs, traces, hypotheses)

#### 11.2.3. Example: Product-Vision Brainstorming

Likely activated modes:
- Holistic (start from global patterns)
- Intuitive (semantic, experience-based reasoning)

#### 11.2.4. Example: Writing TA / SDD

Likely activated modes:

Abstract + Sequential (linear explanation of models)
Logical (cause–effect reasoning)

#### 11.2.5. Example: Refactoring Legacy Code

Likely activated modes:
- Concrete (specific details of implementation)
- Sequential (stepwise transformation)
- Sometimes Parallel (holding multiple versions in mind)

### 11.3. Why This Principle Matters

Task decomposition explains why:
- People who collaborate on a single feature may appear to “think differently” — they are simply working in **different mode-activating subtasks**.
- Two engineers can both be highly competent but operate with **different costs** depending on which subtask they own.
- Misalignment often arises because people are **in different modes**, not because “they don’t understand each other”.
- Many tasks require *multiple* modes sequentially, which explains the subjective feeling of fatigue when switching is frequent.

## 12. Misalignment Modes (Informational)
Common friction patterns arise when:

- one person is in **Abstract** and another is in **Concrete**
- one is in **Sequential** and another is in **Parallel**
- one is in **Analytic** and another is in **Holistic**
- one is in **Logical** and another is in **Intuitive**

Misalignment can also appear when changes increase the future cognitive cost of working on a system. For example, breaking structure, removing invariants, or introducing inconsistent patterns forces future work into higher-cost modes. The conflict arises from task geometry, not from any property of the individual.

CMF provides a vocabulary for **alignment without conflict**.

## 13. Allowed Use Cases
CMF is designed for:
- improving engineering communication
- reducing friction in design reviews
- structuring tasks more clearly
- debugging misalignment
- making documentation more accessible
- improving collaboration and mentoring
- onboarding new engineers
- creating safe, predictable processes

This RFC explicitly does **not** define personality, potential, or value.

## 14. Summary
Cognitive Modes Framework is:
- a tool for **interpreting information processing during tasks**
- not a psychological model
- not a typology
- not a system of labels

Modes are:
- temporary
- switchable
- cost-variable
- context-dependent
- neutral

This RFC defines a **safe, pragmatic, engineering-grounded** framework for understanding communication and collaboration in software development.
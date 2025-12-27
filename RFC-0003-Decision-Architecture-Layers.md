# RFC 0003: Decision Architecture Layers

*This document defines Decision Architecture Layers — a layered model describing where decisions live, how responsibility is distributed, and how consequences propagate across complex engineering systems.*

| Field | Value |
| --- | --- |
| Author | Dmitriy Kirenkin |
| Status | In review |
| Created | 2025–12–27 (CET) |
| Last Updated | 2025–12–27 (CET) |
| Category | Communication, Collaboration, Task Structuring, Engineering Alignment |
| Intended Audience | Software Engineers, Engineering Managers, Product Managers, Designers |

## 1. Purpose

This RFC introduces **Decision Architecture Layers** — a layered model describing **how decisions are structured, where responsibility resides**, and **how consequences propagate** in engineering systems.

The model defines four layers of decision-making:
- L4 — Product / Experience
- L3 — Platform / System Constraints
- L2 — Solution Architecture
- L1 — Implementation / Execution

These layers are **not organizational roles**, **not job levels**, and **not seniority markers**.

They are **decision layers** — cognitive and structural zones where different types of decisions are made, defended, and paid for over time.

## 2. Scope and Boundaries (Safety by Architecture)

Decision Architecture Layers describe **decisions**, not people.

This model does not define:
- roles or job titles
- seniority or career progression
- performance evaluation
- ownership assignment
- team structure
- reporting lines

The model applies to:
- software systems
- technical documents
- organizational decisions
- product development
- any domain where decisions have delayed consequences

The layers describe **where a decision belongs**, not **who must make it**.

## 3. Non-Applicability Clause (Normative)

Decision Architecture Layers **must not** be used to:
- classify individuals
- assign value or authority to people
- define organizational hierarchy
- justify exclusion from decision-making

A single person may operate on **multiple layers** within the same task.

A single decision may involve **multiple layers** sequentially.

The model constrains **decision structure**, not human capability.

## 4. Core Definition (Normative)

A **Decision Architecture Layer** is defined as: **A structural layer describing a class of decisions with distinct responsibility boundaries, time horizons, and consequence profiles.**

Each layer:
- answers a different **class of questions**
- carries a different **type of responsibility**
- incurs consequences on a different **time scale**
- interacts with adjacent layers through translation, not substitution

## 5. The Four Decision Layers (Normative)

### 5.1. L4 — Product / Experience

Primary question: **Why should this exist?**

L4 decisions define:
- user value and meaning
- experience coherence
- long-term intent and trajectory
- trade-offs under uncertainty

Characteristics:
- incomplete information
- delayed feedback
- irreversible perception effects
- high ambiguity

Responsibility:
- accepting uncertainty
- choosing direction without full proof
- living with long-term outcomes

Typical artifacts:
- product intent
- vision statements
- PRDs
- strategic narratives

Cognitive profile (typical, not prescriptive):
`Holistic + Intuitive + Parallel`

### 5.2. L3 — Platform / System Constraints

Primary question: **What is possible and stable?**

L3 decisions define:
- system-wide constraints
- invariants and guarantees
- interaction contracts
- sources of truth

Characteristics:
- historical coupling
- cross-team impact
- migration cost
- long-lived consequences

Responsibility:
- maintaining coherence
- enforcing constraints
- absorbing organizational and technical debt

Typical artifacts:
- platform architecture documents
- feasibility assessments
- system interaction contracts

Cognitive profile:
`Abstract + Logical + Parallel`

### 5.3. L2 — Solution Architecture

Primary question: **How does this system work?**

L2 decisions define:
- concrete solution structure
- component responsibilities
- trade-offs and rationale
- boundaries between parts

Characteristics:
- convergent decision-making
- explicit trade-offs
- medium-term consequences
- high structural leverage

Responsibility:
- defending architectural choices
- rejecting unsafe shortcuts
- explaining decisions after context is gone

Typical artifacts:
- High-Level Solution Design (HL SDD)
- architecture decision records
- design rationales

Cognitive profile:
`Abstract + Logical + Sequential`

### 5.4. L1 — Implementation / Execution

Primary question: **How is this executed?**

L1 decisions define:
- concrete behavior in production
- code structure
- operational handling
- error recovery

Characteristics:
- local scope
- fast feedback
- high volume
- execution pressure

Responsibility:
- correctness
- reliability
- operational response

Typical artifacts:
- code
- tests
- runbooks
- Low-Level Design (when needed)

Cognitive profile:
`Concrete + Logical + Sequential or Parallel`

## 6. Layer Properties (Normative)

### 6.1. Responsibility Gradient

As decisions move downward:
- uncertainty decreases
- reversibility increases
- feedback speed increases

As decisions move upward:
- ambiguity increases
- consequences are delayed
- responsibility becomes strategic

Responsibility **cannot be eliminated** by pushing decisions downward.

### 6.2. Consequence Propagation

Violations at higher layers:
- amplify downstream
- are expensive to correct
- often appear as “technical problems” later

Lower-layer optimizations **cannot compensate** for higher-layer decision failures.

## 7. Layer Transitions (Normative)

Decisions must pass through layers **by translation**, not by skipping.

Correct flow:
```
L4 → L3 → L2 → L1
```

Each transition:
- preserves intent
- introduces constraints
- reduces ambiguity

Skipping layers:
- hides responsibility
- increases future cost
- creates structural debt

## 8. Layer Skipping and Trade-offs (Informational)

Skipping a layer may be **acceptable** if done consciously.

Examples:
- Prototypes may minimize L3/L2
- Experiments may delay L2 formalization
- Emergencies may collapse layers temporarily

However:
- skipped layers do not disappear
- their decisions are merely deferred
- cost reappears later, often amplified

## 9. Misalignment Patterns (Informational)

Common conflicts arise when:
- L4 intent is debated using L2 arguments
- L2 decisions are overridden by L1 convenience
- L3 constraints are treated as optional
- L1 problems are escalated as L4 failures

These conflicts are structural, not personal.

## 10. Documents as Layer Translation Interfaces (Informational)

Documents serve as **translation artifacts** between layers.

Their purpose is:
- to preserve intent
- to make assumptions explicit
- to prevent responsibility leakage

More documents do **not** imply better architecture.
Better translation does.

## 11. Relationship to CMF and TMR (Normative)

- **CMF ([RFC 0001](https://github.com/ideamod/decision-architecture-rfcs/blob/main/RFC-0001-Cognitive-Modes-Framework.md))** describes how information is processed
- **TMR ([RFC 0002](https://github.com/ideamod/decision-architecture-rfcs/blob/main/RFC-0002-Task-Mode-Requirements.md))** describes what tasks demand
- **Decision Architecture Layers** describe where decisions live

The three models are orthogonal and complementary.

## 12. Summary

Decision Architecture Layers provide:
- a structural model of decision-making
- clear responsibility boundaries
- an explanation for recurring engineering conflicts
- a language for alignment without personal attribution

The model:
- is non-organizational
- non-psychological
- non-prescriptive
- concerned with decisions, not people

Used correctly, it makes complexity **visible**, responsibility **explicit**, and trade-offs **conscious**.
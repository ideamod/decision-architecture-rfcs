# RFC 0002: Task Mode Requirements (TMR)

*This document defines TMR — a normative extension to CMF ([RFC 0001](https://github.com/ideamod/decision-architecture-rfcs/blob/main/RFC-0001-Cognitive-Modes-Framework.md)).
It specifies how engineering tasks activate cognitive modes, how to express those requirements formally, and how multi-stage tasks must be described using a strictly defined notation.*

| Field | Value |
| --- | --- |
| Author | Dmitriy Kirenkin |
| Status | In review |
| Created | 2025–12–03 (CET) |
| Last Updated | 2025–12–26 (CET) |
| Category | Communication, Collaboration, Task Structuring, Engineering Alignment |
| Intended Audience | Software Engineers, Engineering Managers, Product Managers, Designers |


## 1. Purpose
RFC 0002 introduces **Task Mode Requirements** (TMR) — a normative formal language describing how engineering tasks activate Cognitive Modes defined in **CMF ([RFC 0001](https://github.com/ideamod/decision-architecture-rfcs/blob/main/RFC-0001-Cognitive-Modes-Framework.md))**.

TMR provides:
- a precise **notation** for expressing the cognitive structure of tasks
- a safe, non-psychological way to **compare and decompose tasks**
- a framework for **multi-stage task sequencing**
- a common protocol for **collaboration alignment**

TMR describes **tasks**, not people.

## 2. Scope and Boundaries (Safety by Architecture)
TMR defines **cognitive requirements of tasks only**.

TMR does **not** model:
- ability
- performance
- potential
- personality
- stable traits
- preference consistency
- role fit
- seniority
- long-term cognitive profile

Because TMR does not model any of these constructs, it is naturally outside the scope of hiring, promotion evaluation, HR assessment, or decisions involving capability or potential.

TMR exists exclusively for **task structuring** and **collaboration engineering**.

## 3. Non-Applicability Clause (Normative)
TMR cannot be used to infer personal traits or abilities, because it does not model them.

TMR describes: **what a task demands**, NOT **what a person is capable of**.

Tasks are **structural**.\
People are **dynamic**.

TMR expresses only the structural side.

## 4. Definition: Task Mode Requirement (Normative)
A **Task Mode Requirement** (**TMR**) is a four-component normative specification describing **which cognitive modes a task structurally requires** across the dimensions:

1. Representation (Abstract ↔ Concrete)
2. Reasoning (Logical ↔ Intuitive)
3. Attention (Sequential ↔ Parallel)
4. Framing (Analytic ↔ Holistic)

Each component specifies either:
- one pole of the axis (`A/C`, `L/I`, `S/P`, `An/H`), or
- `*` meaning either pole is acceptable.

TMR describes **task geometry**, not human behavior.

## 5. TMR Notation (Normative)
A TMR is written as:

```
REP.REAS.ATT.FRAME
```

Where:

- `A` = Abstract, `C` = Concrete
- `L` = Logical, `I` = Intuitive
- `S` = Sequential, `P` = Parallel
- `An` = Analytic, `H` = Holistic
- `*` = either mode acceptable

### Examples:
```
A.L.S.An     = Abstract, Logical, Sequential, Analytic
C.I.P.*      = Concrete, Intuitive, Parallel, framing irrelevant
*.L.*.*      = must be Logical
A.*.S.*      = Abstract + Sequential required
```

### Multi-stage notation:

Stages are connected with `->`:

```
*.*.*.H -> *.*.*.An
```

Meaning: the task starts with Holistic framing, then converges to Analytic framing.

## 6. Why TMR Exists (Informational)
CMF ([RFC 0001](https://github.com/ideamod/decision-architecture-rfcs/blob/main/RFC-0001-Cognitive-Modes-Framework.md)) describes **how people process information** during tasks.\
TMR describes **what tasks demand**.

Engineering tasks differ systematically:
- Debugging: Concrete + Parallel
- Architecture: Abstract + Logical + Sequential
- Brainstorming: Holistic + Intuitive
- Documentation: Abstract + Sequential

TMR provides a **shared, neutral language** to express these requirements precisely and safely.

## 7. Single-Stage Task Patterns (Normative)
Below are typical TMRs for single-stage engineering tasks.

### Implementation:
`C.*.S.An` — Concrete, stepwise, analytic translation into code.\
Many teams effectively operate as `C.L.S.An`, but the minimal structural requirement is `C.*.S.An`.

### Parallel Implementation (high concurrency):
`C.*.P.An` — Multiple active contexts; analytic boundaries maintained..

### Technical Assessment / System Design Doc:
`A.L.S.An` — Abstract modeling, logical invariants, sequential explanation.

### UX / Product Sensemaking:
`*.I.P.H` — Pattern-based reasoning, multi-context processing, holistic framing.

### Live Outage Debugging:
`C.L.P.An` — Concrete evidence, rapid hypothesis testing, parallel attention, analytic framing.

These patterns describe **task geometry**, not personal style.

## 8. Multi-Stage Task Patterns (Normative)
Many tasks require **ordered cognitive stages**, not a single mode.

### Ambiguity Resolution:
`*.*.*.H -> *.*.*.An` — Start broad, pattern-oriented → converge to structure and boundaries.

### Architecture → Implementation:
`A.L.S.An -> C.*.*.An` — First model the system → then translate models into concrete code.

### Refactoring Legacy Code:
`C.L.S.An -> C.L.P.An` — First establish sequential understanding → then juggle multiple structures.

### Vision → Architecture → Implementation:
`H.I.P.H -> A.L.S.An -> C.*.*.An` — Global intent → structured models → concrete translation.

These flows encode task choreography.

## 9. TMR and Task Decomposition (Normative)
TMR enforces the principle: Every large task is a sequence of cognitive stages with distinct geometries.

To structure work:
1. Identify natural cognitive stages.
2. Assign TMR to each stage.
3. Ensure transitions reflect real information-processing demands.

TMR gives teams a shared structural model of **how the task actually unfolds**.

## 10. Collaboration Engineering: Using TMR Safely (Informational)
TMR is not a tool for evaluating people.\
Its purpose is **alignment**.

TMR helps teams:
- plan tasks
- reduce friction
- design clearer documentation
- distribute subtasks based on availability or preference (not ability)
- diagnose communication mismatches

Typical friction it explains:
- “Why did this meeting feel chaotic?”
- “Why is this PR hard to review?”
- “Why are we talking past each other?”

Often: **the conversation and the task are in different modes**.

## 11. Limits and Safety Requirements (Normative)
TMR must **not** be used to:
- assign value
- judge ability
- predict personality
- stereotype communication styles
- label individuals

TMR *may* be used to:
- interpret task demands
- clarify cognitive structure
- improve workflows
- reduce overload
- design sequential collaboration patterns

This ensures ethical, safe, and strictly engineering-grounded usage.

## 12. Compatibility With RFC 0001 (Normative)
[RFC 0001](https://github.com/ideamod/decision-architecture-rfcs/blob/main/RFC-0001-Cognitive-Modes-Framework.md) defines:
- cognitive modes as temporary configurations
- the four independent CMF dimensions
- mode switching and switching cost
- low-cost vs high-cost operation

RFC 0002 adds:
- a formal language for describing task requirements
- a notation for multi-stage task structure
- a framework for decomposing large tasks
- a foundation for collaboration engineering across roles

TMR extends CMF without modifying it.

## 13. Summary
TMR provides a clean, normative language for describing:
- what tasks structurally require
- how tasks unfold across cognitive stages
- how teams can align around shared workflows
- how large tasks can be decomposed safely and predictably

TMR is:
- engineering-grounded
- neutral
- strictly non-psychological
- safe by design
- concerned with tasks, not people

Together with [RFC 0001](https://github.com/ideamod/decision-architecture-rfcs/blob/main/RFC-0001-Cognitive-Modes-Framework.md), TMR forms the foundation of a practical, ethical, and powerful model for **Collaboration Engineering**.
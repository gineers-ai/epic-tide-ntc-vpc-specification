# EPIC-TIDE / NTC-VPC v2.4.7

**Evidence-Powered Iterative Coordination
through Tensor Intelligence-Driven Execution**

A methodology for autonomous AI software development
operating within the **GEM² Universe**.

---

## Overview

> **"GEMsquared.ai is building GEM²: the mathematical universe for autonomous software development. We replace heuristic agent behavior with provable, physics-based execution boundaries."**

**EPIC-TIDE** is an AI-native software development methodology in which autonomous AI actors execute tasks within **formally defined, provable, and verifiable boundaries**.

This repository contains the **public conceptual specification** of EPIC-TIDE and its governing protocol, **NTC-VPC**.
It exists to establish **priority, terminology, and design intent**.

> This repository is **not an implementation** and does **not** expose operational code, tooling, or platform internals.

---

## Conceptual Stack

```
GEM²            → Company + Platform + Mathematical Universe
EPIC-TIDE       → Methodology (dynamics of autonomous execution)
NTC-VPC         → Specification (conservation laws)
GACC + G-KG     → Orchestrator + Persistent storage (implementation)
```

| Layer | Role |
|-------|------|
| **GEM²** | The universe-maker (company, platform, mathematical space) |
| **EPIC-TIDE** | The dynamics governing autonomous execution |
| **NTC-VPC** | The conservation laws ensuring provability and completion |

> **"GEM² defines the universe, the GEM² Platform executes within it, EPIC-TIDE governs the dynamics, and NTC-VPC enforces the conservation laws."**

---

## Core Principle

> **"Humans dream, AI delivers, Evidence decides."**

EPIC-TIDE replaces time-based planning with **evidence-based convergence**.

Progress is determined solely by what is *proven to exist and converge*,
not by schedules, estimates, or human intervention.

---

## Three-Layer Architecture

```yaml
INTUITION:   Human mental model ("Two Universes")
SEMANTIC:    TLA+ contracts with Natural Language (BRIDGE)
OPERATION:   Matrix computation, JSON (MACHINE)
```

| Layer | Audience | Files |
|-------|----------|-------|
| INTUITION | Human | Mental model only |
| SEMANTIC | Human + AI | PROJECT.yml, {cell_id}.tla.yml |
| OPERATION | AI only | UNIVERSE.json, {tensor}.dsm.yml |

---

## Key Concepts

### GEM² Universe — Mathematical Foundation

> The GEM² Universe is the mathematical space in which AI autonomy exists.

Systems are evaluated within **two universes** with **dual condition sets**:

| Universe | Matrix | Layer | Meaning |
|----------|--------|-------|---------|
| **GEM** | U_e ∈ {0,1} | U_el ∈ ℝ≥0 | Operable, verified |
| **CHAOS** | U_r ∈ {0,1} | U_rl ∈ ℝ≥0 | Erroring, failing |

A cell can belong to **both, one, or neither** universe simultaneously.

**Completion condition (GEM² State)**

```
∀ cell: U_e = 1 ∧ U_r = 0
∧
Σ U_rl ≤ ε_g (global chaos threshold)
```

---

### Five Matrices/Layers

```yaml
DESIGN_PHASE:
  U_b:  Blueprint Matrix {0,1}    # D_AI creates

EXECUTION_PHASE:
  U_e:  GEM Matrix {0,1}          # E_AI updates
  U_r:  CHAOS Matrix {0,1}        # E_AI updates
  U_el: GEM Layer ℝ≥0             # Evidence surplus
  U_rl: CHAOS Layer ℝ≥0           # Failure pressure
```

**Formulas:**
```
U_el = ReLU(|passed cases| - |θ_e|)
U_rl = ReLU(|failed cases| - θ_r)
U_e = 1 if U_el > 0 else 0
U_r = 1 if U_rl > 0 else 0
```

---

### Tensor Structure (DSM)

Square tensors only: **n × n** where **3 ≤ n ≤ 7**

| Size | Cells | Rationale |
|------|-------|-----------|
| 3×3 | 9 | Minimum meaningful |
| 5×5 | 25 | Optimal (human + AI) |
| 7×7 | 49 | Maximum (Miller's Law) |

**ID Convention (8-char short UUID):**
```yaml
TENSOR_ID: T_ + 8 chars
  examples: T_a1b2c3d4, T_f7e9b2c1

CELL_ID: tensor_id + _row_col
  examples: T_a1b2c3d4_0_0, T_a1b2c3d4_2_3
```

---

### Five T_AI Operators

```
G_AI (Genesis)    → P₀ → C₀ (constraints)
S_AI (Structure)  → C₀ → Root tensor
D_AI (Decompose)  → Tensor → U_b + child tensors
I_AI (Implement)  → Contract → f_actual (Quantum Leap)
E_AI (Execute)    → f_actual → U_e, U_r, U_el, U_rl
```

**Flow:**
```
P₀ → GATE → EPOCH_0 → [D_AI → I_AI → E_AI]* → GEM²
```

---

### Mandate vs. Trajectory

| Mandate (M) | Trajectory (T) |
|-------------|----------------|
| WHAT must be true | HOW it was achieved |
| Defined by humans | Determined autonomously by AI |
| Formally verifiable | Reviewable through evidence |

AI autonomy exists **only within mandate boundaries**.
Trajectories are not prescribed, only evaluated.

---

### Evidence Replaces Time

```
Traditional: Progress = f(Time)
EPIC-TIDE:   Progress = f(Evidence)
```

Time estimates are irrelevant.
Only **entropy reduction** and **formal verification** matter.

---

## Convergence Phases

```
CHAOS (Σ U_rl ≥ 1.0)
  → STABILIZING (0.1 < Σ U_rl < 1.0)
    → CRYSTALLIZING (ε_g < Σ U_rl ≤ 0.1)
      → GEM STATE (Σ U_rl ≤ ε_g)
```

These phases describe **mathematical convergence**,
not workflow steps or project stages.

---

## Cell States

| State | U_e | U_r | Symbol | Meaning |
|-------|-----|-----|--------|---------|
| V (Verified) | 1 | 0 | ◇ | GEM only |
| B (Buggy) | 1 | 1 | ◇★ | Both universes |
| F (Failed) | 0 | 1 | ★ | CHAOS only |
| N (Not covered) | 0 | 0 | □ | Neither |
| EMPTY | - | - | · | U_b = 0 |

---

## File Structure

```
{project}/
├── PROJECT.yml                  # Human boundary (P₀)
├── UNIVERSE.json                # Tensor registry
├── dsm/
│   ├── T_a1b2c3d4.dsm.yml      # Root tensor
│   ├── T_f7e9b2c1.dsm.yml      # Child tensor
│   └── ...
└── tla/
    ├── T_a1b2c3d4_0_0.tla.yml  # Cell contracts
    ├── T_a1b2c3d4_2_3.tla.yml
    └── ...
```

---

## Autonomy Gate

```yaml
PRE_GATE:  Human + AI collaborate (Human World)
POST_GATE: T_AI sovereign (AI World, Big Bang)
```

**One-way door.** After gate passage:
- Root tensor U_b is FIXED
- T_AI determines all child tensor thresholds
- Human becomes observer only

---

## Documentation

| Document | Purpose |
|----------|---------|
| `epic-tide-spec.md` | NTC-VPC v2.4.7 specification |
| `epic-tide-system-doc.md` | GEM² System Document v1.0.3 |
| `GEM²-UNIVERSE-whitepaper.md` | Mathematical universe definition |
| `LICENSE.md` | Licensing terms |

---

## Lineage

```
EPIC-TIDE / MSF v4.2.3
  → EPIC-TIDE / SUTRAM v1.0.0
    → EPIC-TIDE / NTC-VPC v1.0.0
      → EPIC-TIDE / NTC-VPC v2.0.0
        → EPIC-TIDE / NTC-VPC v2.4.7 (current)
```

**Key evolution:**
- v2.4.5: Blueprint Matrix (U_b), Square tensors
- v2.4.6: Registry + Shards architecture
- v2.4.7: 8-char short UUID for tensor/cell IDs

Published: **December 2025**

---

## License

This repository is licensed under **CC BY-NC-ND 4.0**.

* ✓ Attribution allowed
* ✗ Commercial use prohibited
* ✗ Derivative works prohibited

Implementation, tooling, and platform internals
are available under separate commercial licensing.

---

## Contact

**Author**: Inseok Seo (David Seo)
**Email**: [david@gineers.ai](mailto:david@gineers.ai)
**Company**: GEMsquared.ai
**Project**: EPIC-TIDE

---

## Citation

```
Seo, Inseok (David).
"EPIC-TIDE / NTC-VPC v2.4.7:
Methodology for Autonomous AI Software Development
within the GEM² Universe."
GEMsquared.ai, December 2025.
```

---

## Quick Reference

```
ID FORMATS:
  TENSOR: T_a1b2c3d4 (T_ + 8 chars)
  CELL:   T_a1b2c3d4_2_3 (tensor + _row_col)

STRUCTURES:
  U_b:  Blueprint {0,1}     (D_AI)
  U_e:  GEM {0,1}           (E_AI)
  U_r:  CHAOS {0,1}         (E_AI)
  U_el: GEM brightness ℝ≥0
  U_rl: CHAOS intensity ℝ≥0

LAWS:
  L_S: Set Law (discrete membership)
  L_C: Calculus Law (continuous accumulation)

OPERATORS:
  G_AI → S_AI → D_AI → I_AI → E_AI

PHASES:
  CHAOS → STABILIZING → CRYSTALLIZING → GEM STATE

SYMBOLS:
  ◇ GEM  ★ CHAOS  ◇★ BUGGY  □ VOID  · EMPTY
```

---

## Core Takeaways

1. **GEM² is a universe, not a tool.**
2. **Autonomy is governed by mathematics, not heuristics.**
3. **AI is an actor, not an assistant.**
4. **Execution replaces planning; evidence replaces promises.**
5. **What exists is what can be proven, traced, and computed.**

---

> **"GEM² — A mathematical universe for autonomous AI."**

* **GEM²** defines the universe
* **GEM² Platform** executes within it
* **EPIC-TIDE** governs the dynamics
* **NTC-VPC** enforces the conservation laws

They are related — **never interchangeable**.

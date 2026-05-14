# USM Engine Documentation

Welcome to the official documentation for the **USM Engine** — a schema‑first, reversible, log‑driven 10‑dimensional computational system.

This site provides a complete tour of the architecture, including:

---

## 📐 Core Architecture

- **[Architecture Overview](architecture.md)**  
  High‑level explanation of the entire system and how the subsystems fit together.

- **[USM Schema](schema.md)**  
  The canonical JSON Schema defining all data structures.

---

## ⚙️ Engine Subsystems

- **[Transform Engine](transform.md)**  
  Forward physics, entanglement propagation, metrics, and logs.

- **[Reversible Execution](transform.md#reversible-execution)**  
  Forward + inverse transform cycle and reversible error.

- **[Replay Engine](replay.md)**  
  Deterministic reconstruction of any past state.

- **[Differential Analyzer](differential.md)**  
  Δ‑vectors, Δ‑norms, and local dynamics.

---

## 👁️ Interpretation Layer

- **[View Manifold](view_manifold.md)**  
  Semantic labels, visible/hidden dims, projections, metadata.

---

## 🧭 Temporal Safety

- **[Versioning, Migration, Compatibility](versioning.md)**  
  How the system evolves safely over time.

---

## 🗂️ Logs

- **[Logs Overview](logs.md)**  
  Input Log, Coordinate Log, Metrics Log — the causal backbone.

---

## 🧪 Tests

Tests live in:

- `usm/tests/`

---

## 🧰 Tools

- Graphviz dependency graph:  
  `usm/graph/dependency_graph.dot`

---

## 🚀 Quickstart Tutorial

See:  
**[Quickstart Tutorial](tutorial.md)**

This tutorial walks you through:

- creating a TenDNode  
- running a forward transform  
- running reversible execution  
- generating logs  
- replaying a step  
- computing differentials  
- updating the view manifold

---

Enjoy exploring the USM Engine.

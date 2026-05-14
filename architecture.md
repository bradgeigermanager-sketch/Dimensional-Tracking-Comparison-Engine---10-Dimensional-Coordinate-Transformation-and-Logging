# Architecture

The USM Engine is a **schema-first, reversible, log-driven 10D computational system**.

It is composed of the following subsystems:

- **[USM Schema](schema.md)** — single source of truth for all models.
- **[Transform Engine](transform.md)** — forward physics (DecaMatrix + entanglement).
- **[Reversible Execution](transform.md#reversible-execution)** — forward + inverse + error.
- **[Replay Engine](replay.md)** — log-driven time machine.
- **[Logs](logs.md)** — Input, Coordinate, Metrics.
- **[Differential Analyzer](differential.md)** — Δ-based dynamics.
- **[View Manifold](view_manifold.md)** — semantic lens + projections.
- **[Versioning & Migration](versioning.md)** — temporal safety net.
- **Graphviz Dependency Graph** — `usm/graph/dependency_graph.dot`.

## Code Map

- Models → [`usm/core/models.py`](../usm/core/models.py)
- Transform Engine → [`usm/engine/transform_engine.py`](../usm/engine/transform_engine.py)
- Replay Engine → [`usm/engine/replay_engine.py`](../usm/engine/replay_engine.py)
- Differential Analyzer → [`usm/engine/differential_analyzer.py`](../usm/engine/differential_analyzer.py)
- View Manifold → [`usm/view/view_manifold.py`](../usm/view/view_manifold.py)

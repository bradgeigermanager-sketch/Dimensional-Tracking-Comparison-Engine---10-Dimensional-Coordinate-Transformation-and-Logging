# Replay Engine

Code:  
[`usm/engine/replay_engine.py`](../usm/engine/replay_engine.py)

Replay reconstructs past steps using:

- **Input Log** → [`logging_models.py`](../usm/core/logging_models.py)
- **Coordinate Log**
- **Metrics Log**
- **Transform Engine** → [`transform_engine.py`](../usm/engine/transform_engine.py)

Replay validates:

- transform correctness
- log integrity
- entanglement behavior

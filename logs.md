# Logs

The engine uses three primary logs:

- **Input Log**
- **Coordinate Log**
- **Metrics Log**

All log models are defined in:

- [`logging_models.py`](../usm/core/logging_models.py)

Logs are emitted by:

- **Transform Engine** → [`transform_engine.py`](../usm/engine/transform_engine.py)
- **Reversible Execution** → [`reversible_execution.py`](../usm/engine/reversible_execution.py)
- **Replay Engine** → [`replay_engine.py`](../usm/engine/replay_engine.py)

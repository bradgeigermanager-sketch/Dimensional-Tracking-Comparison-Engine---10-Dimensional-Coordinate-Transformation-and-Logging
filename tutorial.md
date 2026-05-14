**(Quickstart Tutorial — hands‑on, runnable, and linked)**

```markdown
# Quickstart Tutorial

This tutorial walks you through the core workflow of the USM Engine.

You will:

1. Create a `TenDNode`
2. Run a forward transform
3. Run reversible execution
4. Inspect logs
5. Replay a step
6. Compute differentials
7. Update the View Manifold

---

# 1. Create a TenDNode

```python
from usm.core.models import TenDNode, EntanglementBond, ViewManifold

node = TenDNode(
    state_vector=[0.0] * 10,
    decamatrix=[1.0] * 121,
    entanglement=[
        EntanglementBond(source_dim=0, target_dim=1, ratio=0.5, type="excitatory")
    ],
    view_manifold=ViewManifold(
        visible_dims=[0,1,2],
        hidden_dims=[3,4,5,6,7,8,9],
        labels={0:"X",1:"Y",2:"Z"},
        projections={},
        metadata={}
    )
)
```

---

# 2. Run a forward transform

```python
from usm.engine.transform_engine import forward_step

node2, input_log, coord_log, metrics_log = forward_step(
    node_id="demo",
    node=node,
    step_index=0,
    delta_axis=0,
    delta_value=1.0
)
```

---

# 3. Run reversible execution

```python
from usm.engine.reversible_execution import reversible_cycle

inv_coord, inv_metrics = reversible_cycle(
    node_id="demo",
    node=node2,
    step_index=1
)
```

---

# 4. Inspect logs

```python
print(input_log)
print(coord_log)
print(metrics_log)
print(inv_coord)
print(inv_metrics)
```

---

# 5. Replay a step

```python
from usm.engine.replay_engine import replay_step

ok = replay_step(node, input_log, coord_log)
print("Replay valid:", ok)
```

---

# 6. Compute differentials

```python
from usm.engine.differential_analyzer import compute_differentials

stats = compute_differentials([coord_log, inv_coord])
print(stats)
```

---

# 7. Update the View Manifold (PCA-2D)

```python
from usm.view.view_manifold import update_pca_2d

node3 = update_pca_2d(node2, history=[node.state_vector])
print(node3.view_manifold.projections)
```

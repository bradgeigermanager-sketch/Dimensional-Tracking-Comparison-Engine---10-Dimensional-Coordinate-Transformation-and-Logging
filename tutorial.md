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

# Layers

Each foundry uses different GDS numbers for each process step.

We follow the generic layer numbers from  the book "Silicon Photonics Design: From Devices to Systems Lukas Chrostowski, Michael Hochberg".

GDS | layer_name     | Description
--- | ------------   | ---
1   | 1 WGCORE       | 220 nm Silicon core
2   | 2 SLAB150      | 150nm Silicon slab (70nm shallow Etch for grating couplers)
3   | 3 SLAB90       | 90nm Silicon slab (for modulators)
47  | MH             | heater
41  | M1             | metal 1 
45  | M2             | metal 2 
40  | VIA1           | VIA1
44  | VIA2           | VIA2
46  | PADOPEN        | Bond pad opening
51  | UNDERCUT       | Undercut
52  | DEEPTRENCH     | Deep trench
66  | TEXT           | Text markup
64  | FLORRPLAN      |
65  | DICING         |

Layers are available in `pp.LAYER` or `pp.layer(layer_name)`


```eval_rst
.. automodule:: pp.layers
   :members:

```

You basically have two options:

1. You use the generic layermap from the table and use a script to remap the GDS layers into the specific foundry layer map.

2. You create a PDK that has all the layer information for the foundry (no remap needed)


```

from fab1pdk.layers import layer
from fab1pdk.mm1 import mm1x2

component = mmi1x2()

```


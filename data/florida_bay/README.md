# Florida Bay food web

The carbon flows of the Florida Bay ecosystem. Nodes are compartments: species or groups of organisms, plus special nodes such as Input, Output and Respiration.

- **Size:** 128 nodes, 2,106 directed edges.
- **An arrow i → j means:** carbon is transferred from compartment i to compartment j (often j eats i).

## Files

- `nodes.csv`: `node_id,label,group,x,y`. `node_id` runs from 0 to n−1 and can be used as a matrix index. `x`, `y` are coordinates only where the original data had them.
- `edges.csv`: `source,target`, one binary directed edge per row, using `node_id`. No repeated rows.

## Original source

SNAP, <https://snap.stanford.edu/data/Florida-bay.html>, based on the ecological study cited as Ulanowicz et al. in the references; group metadata from Benson et al.

## What the teaching team did to the data

The official binary edge set was kept as it is. There are no repeated rows or self-loops. Only 62 of the 128 compartments have a recorded ecological group; the others are left blank.

## Keep in mind

A random walk along carbon flow is a model, not the movement of animals. A high score does not mean ecological importance in general.

Cite the original source in your report and state that the teaching team prepared the data. Full references are in the catalogue (`catalogue/Network_Catalogue.pdf`). For course use only; do not redistribute.

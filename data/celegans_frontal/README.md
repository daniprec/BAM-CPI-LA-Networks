# *C. elegans* neural network

The wiring of the frontal part of the nervous system of the roundworm *C. elegans*. Nodes are neurons, labelled by name, and two-dimensional coordinates are given so that the network can be drawn as it sits in the worm.

- **Size:** 131 nodes, 764 directed edges.
- **An arrow i → j means:** there is a synaptic connection from neuron i to neuron j.

## Files

- `nodes.csv`: `node_id,label,group,x,y`. `node_id` runs from 0 to n−1 and can be used as a matrix index. `x`, `y` are coordinates only where the original data had them.
- `edges.csv`: `source,target`, one binary directed edge per row, using `node_id`. No repeated rows.

## Original source

SNAP, <https://snap.stanford.edu/data/C-elegans-frontal.html>. Cited as Kaiser and Hilgetag in the references.

## What the teaching team did to the data

All 131 neurons and 764 edges are kept, with no repeated rows or self-loops. Names and coordinates are copied from the original.

## Keep in mind

The graph is anatomical connectivity, not recorded activity. A synapse by itself does not show that one neuron drives another in an experiment.

Cite the original source in your report and state that the teaching team prepared the data. Full references are in the catalogue (`catalogue/Network_Catalogue.pdf`). For course use only; do not redistribute.

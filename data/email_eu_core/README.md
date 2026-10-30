# Email-Eu-core

Email traffic between members of a large European research institution. Each node is an anonymous member and has a department label (42 departments). Only messages between members of the institution are included.

- **Size:** 1,005 nodes, 25,571 directed edges.
- **An arrow i → j means:** member i sent at least one email to member j.

## Files

- `nodes.csv`: `node_id,label,group,x,y`. `node_id` runs from 0 to n−1 and can be used as a matrix index. `x`, `y` are coordinates only where the original data had them.
- `edges.csv`: `source,target`, one binary directed edge per row, using `node_id`. No repeated rows.

## Original source

Stanford Network Analysis Project (SNAP), <https://snap.stanford.edu/data/email-Eu-core.html>. Cited as Yin et al. and Leskovec et al. in the references.

## What the teaching team did to the data

The official file was used unchanged: all 1,005 nodes and 25,571 edges. The 642 self-loops (emails to oneself) are kept. The group is the department number.

## Keep in mind

The graph says that a message was sent, not how many, when, or what they said. Do not attempt to identify any person.

Cite the original source in your report and state that the teaching team prepared the data. Full references are in the catalogue (`catalogue/Network_Catalogue.pdf`). For course use only; do not redistribute.

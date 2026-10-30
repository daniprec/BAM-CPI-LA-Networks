# CollegeMsg: private messages

Private messages exchanged on an online social network at the University of California, Irvine, over about 193 days. A message does not imply a reply.

- **Size:** 1,899 nodes, 20,296 directed edges.
- **An arrow i → j means:** user i sent at least one private message to user j.

## Files

- `nodes.csv`: `node_id,label,group,x,y`. `node_id` runs from 0 to n−1 and can be used as a matrix index. `x`, `y` are coordinates only where the original data had them.
- `edges.csv`: `source,target`, one binary directed edge per row, using `node_id`. No repeated rows.

## Original source

SNAP, <https://snap.stanford.edu/data/CollegeMsg.html>. Cited as Panzarasa et al. in the references.

## What the teaching team did to the data

The original file lists 59,835 timestamped messages. We kept only the sender and the receiver, collapsed repeated messages between the same ordered pair, and removed messages to oneself. Timestamps and message counts are not in the files. Users are anonymous numbers.

## Keep in mind

The graph records who wrote to whom, not what was said or whether the person answered. Do not attempt to identify any person.

Cite the original source in your report and state that the teaching team prepared the data. Full references are in the catalogue (`catalogue/Network_Catalogue.pdf`). For course use only; do not redistribute.

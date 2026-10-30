# Bitcoin Alpha: web of trust

Traders on the Bitcoin Alpha platform rate each other from -10 (total distrust) to +10 (total trust) to reduce fraud. The original network is signed and weighted; this one keeps only the positive trust ratings.

- **Size:** 3,783 nodes, 22,650 directed edges.
- **An arrow i → j means:** user i gave user j a positive trust rating (from +1 to +10).

## Files

- `nodes.csv`: `node_id,label,group,x,y`. `node_id` runs from 0 to n−1 and can be used as a matrix index. `x`, `y` are coordinates only where the original data had them.
- `edges.csv`: `source,target`, one binary directed edge per row, using `node_id`. No repeated rows.

## Original source

SNAP, <https://snap.stanford.edu/data/soc-sign-bitcoin-alpha.html>. Cited as Kumar et al. in the references.

## What the teaching team did to the data

Ratings of 0 or below do not create edges, and the rating values are dropped. If a user rated the same person more than once, the pair counts as one edge if any rating was positive. All 3,783 users stay as nodes even if they have no positive ratings.

## Keep in mind

About 7% of the original ratings were negative, so the graph is a partial picture of the community. A high score means many positive ratings, not proven honesty. This is one of the two largest networks.

Cite the original source in your report and state that the teaching team prepared the data. Full references are in the catalogue (`catalogue/Network_Catalogue.pdf`). For course use only; do not redistribute.

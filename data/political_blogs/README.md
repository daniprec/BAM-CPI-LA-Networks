# Political blogs

US political weblogs around the 2004 presidential election. Each blog is labelled liberal or conservative.

- **Size:** 1,490 nodes, 19,022 directed edges.
- **An arrow i → j means:** blog i linked to blog j in a February 2005 crawl of the blogs' front pages.

## Files

- `nodes.csv`: `node_id,label,group,x,y`. `node_id` runs from 0 to n−1 and can be used as a matrix index. `x`, `y` are coordinates only where the original data had them.
- `edges.csv`: `source,target`, one binary directed edge per row, using `node_id`. No repeated rows.

## Original source

Mark Newman's network data page, <https://websites.umich.edu/~mejn/netdata/>. Cited as Adamic and Glance in the references.

## What the teaching team did to the data

The original file has 19,090 link rows. We collapsed 65 repeated links and removed 3 self-loops, which gives 19,022 binary edges. Blog addresses are kept as labels. The group is the political side.

## Keep in mind

The source warns that the political labels were assigned partly from directories and partly by hand, so some may be wrong. A link is not necessarily an endorsement.

Cite the original source in your report and state that the teaching team prepared the data. Full references are in the catalogue (`catalogue/Network_Catalogue.pdf`). For course use only; do not redistribute.

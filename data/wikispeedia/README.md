# Wikispeedia: Wikipedia articles

A small snapshot of Wikipedia: the 4,604 articles of the *Wikipedia Selection for Schools*, used in the Wikispeedia navigation game. Each article has a subject (Science, Geography, Art, History, and so on).

- **Size:** 4,604 nodes, 119,772 directed edges.
- **An arrow i → j means:** article i contains a hyperlink to article j.

## Files

- `nodes.csv`: `node_id,label,group,x,y`. `node_id` runs from 0 to n−1 and can be used as a matrix index. `x`, `y` are coordinates only where the original data had them.
- `edges.csv`: `source,target`, one binary directed edge per row, using `node_id`. No repeated rows.

## Original source

SNAP, <https://snap.stanford.edu/data/wikispeedia.html>. Cited as West and Leskovec and as West et al. in the references. Wikipedia text is available under CC BY-SA.

## What the teaching team did to the data

We used the article list and the link list of the original download. Repeated links and self-links were removed. The label is the article title and the group is the subject of its first listed category. The game's navigation paths are not part of the data.

## Keep in mind

This is a 2007 school subset, so only links between these articles exist. It is the largest network of the catalogue (see the note on size).

Cite the original source in your report and state that the teaching team prepared the data. Full references are in the catalogue (`catalogue/Network_Catalogue.pdf`). For course use only; do not redistribute.

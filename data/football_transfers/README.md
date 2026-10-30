# Football transfers

The football transfer market around the English Premier League. Nodes are the Premier League clubs of the data and the clubs they bought players from or sold players to. The group tells you whether a club is a league club or another club.

- **Size:** 519 nodes, 4,755 directed edges.
- **An arrow i → j means:** at least one permanent player transfer went from club i (seller) to club j (buyer).

## Files

- `nodes.csv`: `node_id,label,group,x,y`. `node_id` runs from 0 to n−1 and can be used as a matrix index. `x`, `y` are coordinates only where the original data had them.
- `edges.csv`: `source,target`, one binary directed edge per row, using `node_id`. No repeated rows.

## Original source

Transfermarkt data as collected in <https://github.com/ewenme/transfers>. Cited as Menezes in the references.

## What the teaching team did to the data

Each transfer gives an arrow from the selling club to the buying club. Loans, youth-team promotions and transfers without a clear fee were left out. Club names were cleaned automatically and merged when they plainly referred to the same club; a few clubs may still be split or merged wrongly. Clubs outside the league with very few trading partners were removed.

## Keep in mind

Transfers between two clubs that are both outside the league are missing, so the outer clubs exist in this graph only because of their trade with league clubs. The data were scraped and may have errors, especially for older seasons.

Cite the original source in your report and state that the teaching team prepared the data. Full references are in the catalogue (`catalogue/Network_Catalogue.pdf`). For course use only; do not redistribute.

# Lichess chess: who lost to whom

Online games played on the Lichess chess server and collected in a public dataset of about 20,000 games. A decisive game is an arrow from the loser to the winner. Players are grouped by their average rating.

- **Size:** 1,780 nodes, 2,891 directed edges.
- **An arrow i → j means:** player i lost at least one decisive game to player j.

## Files

- `nodes.csv`: `node_id,label,group,x,y`. `node_id` runs from 0 to n−1 and can be used as a matrix index. `x`, `y` are coordinates only where the original data had them.
- `edges.csv`: `source,target`, one binary directed edge per row, using `node_id`. No repeated rows.

## Original source

Chess Game Dataset (Lichess), <https://github.com/arthur9916/Chess-Game-Dataset-Lichess->. Game data from Lichess, <https://lichess.org>. Cited as the dataset authors in the references.

## What the teaching team did to the data

Draws were left out because they have no direction. Repeated results between the same pair give one edge. Players with only a few distinct opponents were removed repeatedly so that a core of players remains. The label is the Lichess username.

## Keep in mind

This network is sparse, since most players face few opponents. It is not a random sample of Lichess players. It may behave very differently from the other networks.

Cite the original source in your report and state that the teaching team prepared the data. Full references are in the catalogue (`catalogue/Network_Catalogue.pdf`). For course use only; do not redistribute.

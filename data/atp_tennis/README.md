# ATP tennis: who lost to whom

Men's professional tennis, seasons 2016–2025. Every player is a node. A win is an arrow *from the loser to the winner*, so a random walker moves from a defeated player to the player who beat him.

- **Size:** 1,191 nodes, 19,986 directed edges.
- **An arrow i → j means:** player i lost at least once to player j in a tour-level match.

## Files

- `nodes.csv`: `node_id,label,group,x,y`. `node_id` runs from 0 to n−1 and can be used as a matrix index. `x`, `y` are coordinates only where the original data had them.
- `edges.csv`: `source,target`, one binary directed edge per row, using `node_id`. No repeated rows.

## Original source

Jeff Sackmann / Tennis Abstract, <https://github.com/JeffSackmann/tennis_atp> (CC BY-NC-SA 4.0: attribution, non-commercial). Cited as Sackmann in the references.

## What the teaching team did to the data

We read one match file per season, turned each match into one arrow from loser to winner, and collapsed repeated pairs into one edge. The label is the player name and the group is the country code most often listed for the player.

## Keep in mind

Only the pairs that met in these seasons are connected, and the number of meetings, the score and the surface are ignored. You can compare your results with the official rankings, but they measure different things.

Cite the original source in your report and state that the teaching team prepared the data. Full references are in the catalogue (`catalogue/Network_Catalogue.pdf`). For course use only; do not redistribute.

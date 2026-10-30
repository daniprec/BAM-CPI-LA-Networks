# Food.com: what people cook next

A recipe-to-recipe network built from the order in which users review recipes on the website Food.com. If a user reviewed a cake and later a lasagna, the cake points to the lasagna. A random walker behaves like a typical user moving from recipe to recipe. Nodes are the 1,500 most-reviewed recipes, grouped by dish type.

- **Size:** 1,500 nodes, 13,893 directed edges.
- **An arrow i → j means:** some user reviewed recipe i and, on a later day, reviewed recipe j as their next review.

## Files

- `nodes.csv`: `node_id,label,group,x,y`. `node_id` runs from 0 to n−1 and can be used as a matrix index. `x`, `y` are coordinates only where the original data had them.
- `edges.csv`: `source,target`, one binary directed edge per row, using `node_id`. No repeated rows.

## Original source

Food.com Recipes and Interactions, as used in Majumder et al., shared by the teaching team. Cited as Majumder et al. in the references.

## What the teaching team did to the data

For each user we sorted their reviews by date and linked each recipe to the next different recipe reviewed on a later day. Reviews on the same day were not ordered, so they give no edge. Only recipes with names and enough reviews were kept. Review texts and ratings are not included.

## Keep in mind

Reviews are written when users choose to post them, not necessarily when they cook. Only the most popular recipes are present.

Cite the original source in your report and state that the teaching team prepared the data. Full references are in the catalogue (`catalogue/Network_Catalogue.pdf`). For course use only; do not redistribute.

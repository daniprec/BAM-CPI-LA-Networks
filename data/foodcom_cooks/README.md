# Food.com: cooks reviewing cooks

A reputation network on Food.com. Users publish recipes and review the recipes of others; an arrow goes from the reviewer to the author. To keep the network manageable, we kept its dense core: users that remain after repeatedly removing everyone with fewer than 10 connections. The group tells how many recipes the user has published.

- **Size:** 2,121 nodes, 62,068 directed edges.
- **An arrow i → j means:** user i reviewed at least one recipe published by user j.

## Files

- `nodes.csv`: `node_id,label,group,x,y`. `node_id` runs from 0 to n−1 and can be used as a matrix index. `x`, `y` are coordinates only where the original data had them.
- `edges.csv`: `source,target`, one binary directed edge per row, using `node_id`. No repeated rows.

## Original source

Same data as the previous network, Food.com Recipes and Interactions (Majumder et al.).

## What the teaching team did to the data

Reviews were joined to the recipes' authors, reviews of one's own recipes were removed, and repeated pairs collapsed to one edge. Users are anonymous numbers. Review texts, ratings and dates are not included.

## Keep in mind

The core is only a small part of the site, so your conclusions apply to this group of users. Do not attempt to identify any person.

Cite the original source in your report and state that the teaching team prepared the data. Full references are in the catalogue (`catalogue/Network_Catalogue.pdf`). For course use only; do not redistribute.

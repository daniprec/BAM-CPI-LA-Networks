# BAM-CPI-LA-Networks

Directed networks for the Fall 2026 joint project of **Computer Programming I** and **Linear Algebra** (Bachelor in Applied Mathematics, IE University): *Network Centrality and PageRank Using Matrices in Python*.

**Each group works on a different network, assigned first come, first served.** Read the **[Network Catalogue (PDF)](catalogue/Network_Catalogue.pdf)**, choose, and claim your network as announced by the teaching team. The catalogue explains every network, its original source, and how to cite it.

## Networks

| Folder | Network | Nodes | Edges |
|---|---|---:|---:|
| [`email_eu_core`](data/email_eu_core) | Email-Eu-core | 1,005 | 25,571 |
| [`political_blogs`](data/political_blogs) | Political blogs | 1,490 | 19,022 |
| [`florida_bay`](data/florida_bay) | Florida Bay food web | 128 | 2,106 |
| [`celegans_frontal`](data/celegans_frontal) | *C. elegans* neural network | 131 | 764 |
| [`collegemsg`](data/collegemsg) | CollegeMsg: private messages | 1,899 | 20,296 |
| [`wikispeedia`](data/wikispeedia) | Wikispeedia: Wikipedia articles | 4,604 | 119,772 |
| [`bitcoin_alpha`](data/bitcoin_alpha) | Bitcoin Alpha: web of trust | 3,783 | 22,650 |
| [`atp_tennis`](data/atp_tennis) | ATP tennis: who lost to whom | 1,191 | 19,986 |
| [`football_transfers`](data/football_transfers) | Football transfers | 519 | 4,755 |
| [`lichess_chess`](data/lichess_chess) | Lichess chess: who lost to whom | 1,780 | 2,891 |
| [`foodcom_recipes`](data/foodcom_recipes) | Food.com: what people cook next | 1,500 | 13,893 |
| [`foodcom_cooks`](data/foodcom_cooks) | Food.com: cooks reviewing cooks | 2,121 | 62,068 |

## Format

Every network has the same files:

```
data/<name>/nodes.csv    node_id,label,group,x,y
data/<name>/edges.csv    source,target
data/<name>/README.md    what it is, original source, preparation, limitations
```

Edges are binary (no repeated rows). Self-loops were removed everywhere except in `email_eu_core`, which keeps its 642 self-loops.

## Loading in Python (Colab or local)

```python
import pandas as pd
base = "https://raw.githubusercontent.com/<owner>/BAM-CPI-LA-Networks/main/data/<name>/"
nodes = pd.read_csv(base + "nodes.csv")
edges = pd.read_csv(base + "edges.csv")
n = len(nodes)
```

(Replace `<owner>` and `<name>`. This URL works only if the repository is public; otherwise download the folder.)

## Citing and licenses

Your report must cite the **original source** of your network (see `catalogue/Network_Catalogue.pdf`) and say that the teaching team prepared the data. The data are provided for this course only. See [`NOTICE.md`](NOTICE.md) for the data licenses.

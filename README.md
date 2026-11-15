# 🕸️ Graph Neural Networks: From Theory to Practice

An introductory study of **Graph Neural Networks (GNNs)**: the graph-theory background, and hands-on experiments comparing GNNs with non-graph baselines on node, edge, and graph-level tasks.

## Contents

1. **Background**
   - Graph theory basics: directed / undirected, weighted, simple vs. multigraphs, node degree, adjacency matrix
   - Why standard neural networks struggle with graph-structured data
2. **Cora citation network** (2,708 papers, 7 classes)
   - Graph visualization with NetworkX
   - Node classification: GCN vs. CNN vs. MLP
   - Edge classification with a GCN
   - Link prediction: GCN vs. MLP
3. **TUDataset PROTEINS** (1,113 protein graphs)
   - Graph classification: GCN vs. a simple feed-forward network

## Results

| Task | GCN | Baseline |
|---|---|---|
| Node classification (Cora) | **0.81** | CNN 0.53 · MLP 0.52 |
| Link prediction (Cora) | **0.79** | MLP 0.79 |
| Edge classification (Cora) | **0.73** | – |
| Graph classification (PROTEINS) | **0.76** | Simple NN 0.66 |

The main takeaway: using the graph structure (message passing between neighbours) gives a large improvement on node classification, where the connections carry most of the information.

## Tech stack

Python · PyTorch · PyTorch Geometric · NetworkX · scikit-learn · Matplotlib · Seaborn

## How to run

```bash
pip install torch torch_geometric networkx scikit-learn matplotlib seaborn
jupyter notebook finalprojectcode.ipynb
```

Datasets (Cora, PROTEINS) are downloaded automatically by PyTorch Geometric.

## Author

Michaela Chrisafaki – Physicist, Machine Learning

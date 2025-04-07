

To run our method on GOOD datasets, here is an example:

```
python run.py --device 0 --batch_size 64 --dataset goodmotif --domain basis --shift covariate --base_gnn gin --early_stop_epochs 50  --nhid 128 --epochs 100 --pretraining_epochs 10 --nlayers 4 --edge_gnn_layers 2  --edge_gnn gin --edge_uniform_penalty 0.001 --edge_prob_thres 90 --edge_budget 0.85 --edge_penalty 10   --seed 1 --with_bn --dropout 0.0
```

Here, `dataset` can be chosen among $\{goodmotif,goodhiv\}$

`edge_gnn` corresponds to the subgraph selector $t(\cdot)$, `edge_gnn_layers` denotes the #layers in $t(\cdot)$. `edge_uniform_penalty`  corresponds to $\lambda_2$ in the paper, `edge_prob_thres`  corresponds to $K$ in our paper, `edge_budget` corresponds to $\eta$ in our paper, `edge_penalty`  corresponds to $\lambda_1$ in our paper. 

The software versions are listed below:

```
torch==2.2.0
torch_geometric==2.4.0
numpy==1.24.4
ogb==1.3.6
```


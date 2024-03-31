# GNN based Quark-Gluon Classification

### Task: To classify input as Quark/Gluon using Graph Neural Networks(GNN).

    Datasets: https://cernbox.cern.ch/s/oolDBdQegsITFcv

### Approach 1:

![graph_formation](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/2516e942-d7cd-41d3-b388-f6a1bfa837dc)
*Note: Approach inspired from the paper [Vision GNN: An Image is Worth Graph of Nodes](https://arxiv.org/abs/2206.00272)*


-> **Making Patches:** The matrix had a shape of (3,125,125). I have split this matrix into patches of patch_size (used 25). 


-> **Node Features:** The matrix is broken into 25 such patches. Each patch is considered as a Node for our Graph, the node features being the flattened pixel values (1875 dimension).

-> **Edge Formation:** KNN is used to find the neigbours of this node features and the K edges are formed based on which Node embedding is closer.

-> **Edge Features:** Also the mean square error of the node features between which there is an edge is taken as the Edge feature.

-> **Dataloader:** This Graph is then loaded into the dataloader and then further training process is done


------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Approach 2:

![graph_formation_A2](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/43736c09-3c5d-4398-b26c-b2de7760ad60)

-> **Node Features:** The number of non-zero pixel values are very less in number. Considering this, we can take all the non-zero pixels as the nodes

-> **Edge Formation:** KNN is used to find the neigbours of this node features and the K edges are formed based on which Node embedding is closer.
	
-> **Dataloader:** This Graph is then loaded into the dataloader and then further training process is done

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Model




![Pipeline2](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/f8cacd18-f497-4652-b112-4cab7e7af6a3)

| Model Name | Accuracy | Notebook Link | PDF Link | Model Weights | Readme | Inference Notebook | ROC AUC Score |
|------------|----------|---------------|----------|---------------|--------| -------------------|---------------|
| GCNConv    | 73.09%    | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GCNConv/gcnconv-final.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GCNConv/gcnconv-final.pdf) | [Weights](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GCNConv/GCNConv.pth) | [readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GCNConv/GCNConv.md) | [Inference](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GCNConv/infernce_GCNConv-final.ipynb) | [0.7697](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GCNConv/ROC_GCNConv.png) |
| SAGEConv   | 71.12%    | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/SAGEConv/graphsage-15epoch.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/SAGEConv/graphsage-15epoch.pdf) | [Weights](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/SAGEConv/graphsage_15epoch.pth) | [readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/SAGEConv/SAGEConv.md)
| GATConv    | 68.16%    | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GATConv/GATConv.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GATConv/gatconv.pdf) | [Weights](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GATConv/GATConv.pth) | [readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GATConv/GATConv.md)  | [Inference](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GATConv/Infernce_GATConv-final.ipynb) | [0.8660](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GATConv/ROC_GATConv.png) |


### Working on the value of threshold is going to improve the accuracy of the model even more, By seeing the ROC AUC score.


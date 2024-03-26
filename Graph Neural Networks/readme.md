# GNN based Quark-Gluon Classification

### Task: To classify input as Quark/Gluon using Graph Neural Networks(GNN).

    Datasets: https://cernbox.cern.ch/s/oolDBdQegsITFcv

### Approach:

#### Formation of Graph from Matrix
*Note: Approach inspired from the paper Vision GNN: An image is worth Graph of Nodes*


![graph_formation](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/2516e942-d7cd-41d3-b388-f6a1bfa837dc)

-> **Making Patches:** The matrix had a shape of (3,125,125). I have split this matrix into patches of patch_size (used 25 and 5). 


-> **Node Features:** For understanding lets take for now that the patch_size is 25. Then the matrix is broken into 25 such patches. Each patch is considered as a Node for our Graph, the node features being the flattened pixel values.

-> **Edge Formation:** KNN is used to find the neigbours of this node features and the K edges are formed based on which Node embedding is closer.

-> **Edge Features:** Also the mean square error of the node features between which there is an edge is taken as the Edge feature.

-> **Dataloader:** This Graph is then loaded into the dataloader and then further training process is done

------------------------------------------------------------------------------------------------------------------------------------------------------------------
    

	



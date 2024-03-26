# GNN based Quark-Gluon Classification

### Task: To classify input as Quark/Gluon using Graph Neural Networks(GNN).

    Datasets: https://cernbox.cern.ch/s/oolDBdQegsITFcv

This dataset was of the file format  .test.snappy.parquet extension
It contains a matrix of shape (3,) in which each element was an array of 125 elements and that 125 elements had 125 elements. 
The dataset also contained the m0 and pt values along with the target which was binary due to binary classification problem statement.

### Approach:

#### Formation of Graph from Matrix

-> The matrix had a shape of (3,125,125). I have split this matrix into patches of patch_size (used 25 and 5). 


-> For understanding lets take for now that the patch_size is 25. Then the matrix is broken into 25 such patches. Each patch is considered as a Node for our Graph, the node features being the flattened pixel values.

-> KNN is used to find the neigbours of this node features and the K edges are formed based on which Node embedding is closer.

-> Also the mean square error of the node features between which there is an edge is taken as the Edge feature.

-> This Graph is then loaded into the dataloader and then further training process is done
------------------------------------------------------------------------------------------------------------------------------------------------------------------
    

	



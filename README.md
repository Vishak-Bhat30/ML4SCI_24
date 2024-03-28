# <p align="center">ML4SCI_24 </p>


## Common Task 1. Electron/photon classification

### Project Resources

| Resource Type          | Description                                       | Link                                                                                        |
|------------------------|---------------------------------------------------|---------------------------------------------------------------------------------------------|
| **Directory**          | Complete collection of project files.             | [Common Task 1](https://github.com/Vishak-Bhat30/ML4SCI_24/tree/main/Common%20Task%201)    |
| **Detailed Solution**  | Breakdown of the approach used.     | [Read Solution](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%201/ML4SCI_Electron_photon_classification.md) |
| **Jupyter Notebook**   | Code and analysis in a Notebook format.       | [Open Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%201/ML4SCI_task1_Resnet15.ipynb) |
| **PDF Version**        | Pdf of the notebook.                 | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%201/ml4sci-task1-resnet15.pdf) |
| **Model Weights**      | Model weights for replication and testing.    | [Weights](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%201/model_resnet15.pth)       |


### Detailed Training Outcomes

I carefully monitored the training progress over 100 epochs, ensuring optimal performance without overfitting. Below are the key metrics at the conclusion of training:

- **Final Epoch**: 100/100
- **Training Loss**: 0.3649
- **Validation Accuracy**: 84.11%
- **Validation Loss**: 0.3474

<img src="https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/9d892ec4-6cd9-4e33-ad5f-4d56b3862a9a" width="450" alt="Training Curve">


*Figure: Training curve demonstrating the model's performance over iterations.*




## Common Task 2.  Deep Learning based Quark-Gluon Classification

### Models Overview

| Model Name     | Architecture | Detailed Solution | Notebook | PDF | Model Weight | Accuracy |
|----------------|--------------|-------------------|----------|-----|--------------|----------|
| VGG-based      | VGG12        | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/VGG/Quark_Gluon_classification_VGG12.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/VGG/ML4SCI-24-task2_VGG12.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/VGG/ML4SCI-24-task2-VGG12.pdf) | [VGG12 PTH](https://drive.google.com/file/d/1O71TYGBMDg8TTDzjivJmJFM5AE-9KA8z/view?usp=sharing) | 72.56% |
| LeNet-based    | LeNet5       | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/LeNet/Quark_Gluon_classification_LeNet.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/LeNet/ML4SCI-24-task2-LeNet5.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/LeNet/ML4SCI-24-task2-LeNet5.pdf) | [LeNet PTH](https://drive.google.com/file/d/10g7icdcjzLBUFsSSlsNxCTcZekdvZpwy/view?usp=sharing) | 71.26% |
| ResNet-based    | ResNet50     | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/Resnet/Quark_Gluon_classification_Resnet.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/Resnet/ML4SCI-24-task2-2-resnet.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/Resnet/ml4sci-24-task2-2-resnet.pdf) | [ResNet PTH](https://drive.google.com/file/d/1lAQ-nNRmqXakOe0jMu_MiC-whsnMIgME/view?usp=sharing) | 70.61% |
| DenseNet-based | DenseNet121  | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/DenseNet/Quark_Gluon_classification_DenseNet.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/DenseNet/ML4SCI-24-task2-densenet.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/DenseNet/ml4sci-24-task2-densenet.pdf) | [DenseNet PTH](https://drive.google.com/file/d/1rgDY7GgYoHsWSmWxei8IoqBsCuPx03ch/view?usp=sharing) | 69.70% (overfit)|
| MobileNet-based| MobileNetV3  | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/MobileNet/Quark_Gluon_classification_MobileNet.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/MobileNet/ML4SCI-24-task2-2-mobilenet.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/MobileNet/ml4sci-24-task2-2-mobilenet.pdf) | [MobileNet PTH](https://drive.google.com/file/d/12wAngj_0EKgX0Vl_lllFp7wGLihadgCZ/view?usp=sharing) | 65.31% (overfit) |
| EfficientNet-based | EfficientNetB0 | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/EfficientNet/Quark_Gluon_classification_EfficientNet.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/EfficientNet/ML4SCI-24-task2-2-efficientnet.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/EfficientNet/ml4sci-24-task2-2-efficientnet.pdf) | [EfficientNet PTH](https://drive.google.com/file/d/18gh6SCjKS227dSFMTJ_2sNZNh_M1MBNG/view?usp=sharing) | 63.57% (overfit)|




### Results and Analysis

During the training of both models, it was observed that the models started to overfit after approximately 10 epochs. The models were saved at the point where the gap between the train loss and the validation loss was minimal. This strategy helped achieve an accuracy of around 73% on the validation set for both models.

Below are the training curves for the VGG12 and LeNet architectures, illustrating the point of overfitting and the epoch at which the models were saved.

| Model Architecture | Training Curve |
|-------------------|----------------|
| VGG12             | <img src="https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/79c1cd93-921a-4ad4-ab92-656ba3d24f43" width="450" alt="Training Curve"> |
| LeNet             |<img src="https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/3c486ed0-c3d8-4e37-8ed7-87f5818cbfa3" width="450" alt="Training Curve"> |
| ResNet             |<img src="https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/12cbc9a7-317a-4949-ba66-4a28a31ee367" width="450" alt="Training Curve"> |
| DenseNet             |<img src="https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/9bd8f6ed-6029-47a4-8ddf-0298b67cd07a" width="450" alt="Training Curve"> |
| MobileNet             |<img src="https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/c929091c-d862-4084-a63a-13f4d658c1a8" width="450" alt="Training Curve"> |
| EfficientNet             |<img src="https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/f263e48a-6e07-4d10-ba93-46de7cbe77cc" width="450" alt="Training Curve"> |



**Observation:** The training curves indicate that careful monitoring of both train and validation losses is crucial to prevent overfitting and to choose the optimal model state for deployment.


## GNN based Quark-Gluon Classification

### Approach 1:

![graph_formation](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/2516e942-d7cd-41d3-b388-f6a1bfa837dc)

### Approach 2:
![graph_formation_A2](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/fa9541db-6081-4733-bee7-54770f77ffe0)

------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Models Overview  

| Model Name | Accuracy | Notebook Link | PDF Link | Model Weights | Readme |
|------------|----------|---------------|----------|---------------|--------|
| GCNConv    | 73.09%    | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GCNConv/gcnconv-final.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GCNConv/gcnconv-final.pdf) | [Weights](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GCNConv/GCNConv.pth) | [readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GCNConv/GCNConv.md)
| SAGEConv   | 67.44%    | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/SAGEConv/graphsage-67.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/SAGEConv/graphsage-67.pdf) | [Weights](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/SAGEConv/SAGEConv.pth) | [readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/SAGEConv/SAGEConv.md)
| GATConv    | 65.09%    | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GATConv/GATConv.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GATConv/gatconv.pdf) | [Weights](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GATConv/GATConv.pth) | [readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Graph%20Neural%20Networks/GATConv/GATConv.md)


	





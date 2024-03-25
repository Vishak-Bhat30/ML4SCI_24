# <p align="center">ML4SCI_24</p>


## Common Task 1. Electron/photon classification

### Project Resources

| Resource Type          | Description                                       | Link                                                                                        |
|------------------------|---------------------------------------------------|---------------------------------------------------------------------------------------------|
| **Directory**          | Complete collection of project files.             | [View Directory](https://github.com/Vishak-Bhat30/ML4SCI_24/tree/main/Common%20Task%201)    |
| **Detailed Solution**  | Comprehensive breakdown of the approach used.     | [Read Solution](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%201/ML4SCI_Electron_photon_classification.md) |
| **Jupyter Notebook**   | Code and analysis in an interactive format.       | [Open Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%201/ML4SCI_task1_Resnet15.ipynb) |
| **PDF Version**        | Printable notebook for reference.                 | [Download PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%201/ml4sci-task1-resnet15.pdf) |
| **Model Weights**      | Pre-trained model for replication and testing.    | [Download Weights](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%201/model_resnet15.pth)       |


### Results 
<img src="https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/9d892ec4-6cd9-4e33-ad5f-4d56b3862a9a" width="350" height="250">

Achieved an accuracy of 84% + in the Validation data after 80-20 split.

Epoch 100/100: 100%|██████████| 1557/1557 [00:49<00:00, 31.36it/s, training loss=0.3649]
Validation Accuracy: 84.11%
VAL LOSS 0.34736170422121226
Model parameters saved
Finished Training



## Common Task 2.  Deep Learning based Quark-Gluon Classification

### Models Overview

| Model Name     | Architecture | Detailed Solution | Notebook | PDF | Model Weight | Accuracy |
|----------------|--------------|-------------------|----------|-----| -------------|----------|
| VGG-based      | VGG12        | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/Quark_Gluon_classification_VGG12.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/ML4SCI-24-task2_VGG12.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/ML4SCI-24-task2-VGG12.pdf) | [VGG12 PTH](https://drive.google.com/file/d/1O71TYGBMDg8TTDzjivJmJFM5AE-9KA8z/view?usp=sharing) | 72.56% |
| LeNet-based    | LeNet5       | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/Quark_Gluon_classification_LeNet.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/ML4SCI-24-task2-LeNet5.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/ML4SCI-24-task2-LeNet5.pdf) | [LeNet PTH](https://drive.google.com/file/d/10g7icdcjzLBUFsSSlsNxCTcZekdvZpwy/view?usp=sharing) | 71.26% |

### Results and Analysis

During the training of both models, it was observed that the models started to overfit after approximately 10 epochs. The models were saved at the point where the gap between the train loss and the validation loss was minimal. This strategy helped achieve an accuracy of around 73% on the validation set for both models.

Below are the training curves for the VGG12 and LeNet architectures, illustrating the point of overfitting and the epoch at which the models were saved.

| Model Architecture | Training Curve |
|-------------------|----------------|
| VGG12             | ![VGG12 Training Curve](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/79c1cd93-921a-4ad4-ab92-656ba3d24f43) |
| LeNet             | ![LeNet Training Curve](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/3c486ed0-c3d8-4e37-8ed7-87f5818cbfa3) |

**Observation:** The training curves indicate that careful monitoring of both train and validation losses is crucial to prevent overfitting and to choose the optimal model state for deployment.





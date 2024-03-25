# <p align="center">ML4SCI_24</p>


## Common Task 1. Electron/photon classification

### Solution

| Description               | Link                                                                                  |
|---------------------------|---------------------------------------------------------------------------------------|
| Directory                 | [Common Task 1](https://github.com/Vishak-Bhat30/ML4SCI_24/tree/main/Common%20Task%201) |
| Detailed Solution         | [Solution MD](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%201/ML4SCI_Electron_photon_classification.md) |
| Notebook                  | [Notebook IPYNB](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%201/ML4SCI_task1_Resnet15.ipynb) |
| Notebook as PDF           | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%201/ml4sci-task1-resnet15.pdf)          |
| Model Weights             | [Weights PTH](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%201/model_resnet15.pth)          |


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

| Model Name     | Architecture | Detailed Solution | Notebook | PDF |
|----------------|--------------|-------------------|----------|-----|
| VGG-based      | VGG12        | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/Quark_Gluon_classification_VGG12.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/ML4SCI-24-task2_VGG12.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/ML4SCI-24-task2-VGG12.pdf) |
| LeNet-based    | LeNet5       | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/Quark_Gluon_classification_LeNet.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/ML4SCI-24-task2-LeNet5.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/ML4SCI-24-task2-LeNet5.pdf) |

Model weights for both models can be found [here](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/model_weights.pth).


### Results 

As seen in the below training curve the model starts to overfit after around 10 epochs.
So I have saved that model where the gap between the train loss and the validation loss is less.


Achieved accuracy around 73% on the validation set.

<div style="display: flex; flex-direction: row;">
    <div style="flex: 50%; padding: 5px;">
        <img src="https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/79c1cd93-921a-4ad4-ab92-656ba3d24f43" alt="Image 1" style="width: 400px;">
        <p style="text-align: center;">VGG12</p>
    </div>
    <div style="flex: 50%; padding: 5px;">
        <img src="https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/3c486ed0-c3d8-4e37-8ed7-87f5818cbfa3" alt="Image 2" style="width: 400px;">
        <p style="text-align: center;">LeNet</p>
    </div>
</div>





## Common Task 2.  Deep Learning based Quark-Gluon Classification

### Models Overview

| Model Name     | Architecture | Detailed Solution | Notebook | PDF | Model Weight | Accuracy | ROC AUC |
|----------------|--------------|-------------------|----------|-----|--------------|----------|---------|
| VGG-based      | VGG12        | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/VGG/Quark_Gluon_classification_VGG12.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/VGG/ML4SCI-24-task2_VGG12.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/VGG/ML4SCI-24-task2-VGG12.pdf) | [VGG12 PTH](https://drive.google.com/file/d/1O71TYGBMDg8TTDzjivJmJFM5AE-9KA8z/view?usp=sharing) | 72.56% | [0.7841](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/VGG/ROC_VGG.png) |
| ResNet-based    | ResNet50     | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/Resnet/Quark_Gluon_classification_Resnet.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/Resnet/ML4SCI-24-task2-2-resnet.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/Resnet/ml4sci-24-task2-2-resnet.pdf) | [ResNet PTH](https://drive.google.com/file/d/1lAQ-nNRmqXakOe0jMu_MiC-whsnMIgME/view?usp=sharing) | 70.61% | [0.8504](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/Resnet/ROC_Resnet.png) |
| LeNet-based    | LeNet5       | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/LeNet/Quark_Gluon_classification_LeNet.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/LeNet/ML4SCI-24-task2-LeNet5.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/LeNet/ML4SCI-24-task2-LeNet5.pdf) | [LeNet PTH](https://drive.google.com/file/d/10g7icdcjzLBUFsSSlsNxCTcZekdvZpwy/view?usp=sharing) | 71.26% | [0.8150](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/LeNet/ROC_LeNet.png) |
| DenseNet-based | DenseNet121  | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/DenseNet/Quark_Gluon_classification_DenseNet.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/DenseNet/ML4SCI-24-task2-densenet.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/DenseNet/ml4sci-24-task2-densenet.pdf) | [DenseNet PTH](https://drive.google.com/file/d/1rgDY7GgYoHsWSmWxei8IoqBsCuPx03ch/view?usp=sharing) | 69.70% (overfit)| [0.8349](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/DenseNet/ROC_DenseNet.png) |
| MobileNet-based| MobileNetV3  | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/MobileNet/Quark_Gluon_classification_MobileNet.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/MobileNet/ML4SCI-24-task2-2-mobilenet.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/MobileNet/ml4sci-24-task2-2-mobilenet.pdf) | [MobileNet PTH](https://drive.google.com/file/d/12wAngj_0EKgX0Vl_lllFp7wGLihadgCZ/view?usp=sharing) | 65.31% (overfit) | [0.7168](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/MobileNet/ROC_MobileNet.png) |
| EfficientNet-based | EfficientNetB0 | [Readme](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/EfficientNet/Quark_Gluon_classification_EfficientNet.md) | [Notebook](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/EfficientNet/ML4SCI-24-task2-2-efficientnet.ipynb) | [PDF](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/EfficientNet/ml4sci-24-task2-2-efficientnet.pdf) | [EfficientNet PTH](https://drive.google.com/file/d/18gh6SCjKS227dSFMTJ_2sNZNh_M1MBNG/view?usp=sharing) | 63.57% (overfit)| [0.7241](https://github.com/Vishak-Bhat30/ML4SCI_24/blob/main/Common%20Task%202/EfficientNet/ROC_EfficientNet.png) |




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

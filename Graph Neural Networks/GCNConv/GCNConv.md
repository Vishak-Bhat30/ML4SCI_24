# GCNConv

### Model Architecture

    DeepGNN(
      (conv1): GCNConv(75, 1024)
      (bn1): BatchNorm1d(1024, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
      (conv2): GCNConv(1024, 512)
      (bn2): BatchNorm1d(512, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
      (conv3): GCNConv(512, 256)
      (bn3): BatchNorm1d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
      (conv4): GCNConv(256, 128)
      (bn4): BatchNorm1d(128, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
      (dropout): Dropout(p=0.5, inplace=False)
      (lin): Linear(in_features=128, out_features=2, bias=True)
    )

### Results

Saved Best Model: Epoch 11, Val. Acc.: 0.7309
Epoch: 001, Train Loss: 0.5905, Val. Loss: 0.5734, Val. Acc.: 0.7309
![Training_curve_GCNConv](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/5a3bf958-db58-4037-9c52-edff7abfdaf7)

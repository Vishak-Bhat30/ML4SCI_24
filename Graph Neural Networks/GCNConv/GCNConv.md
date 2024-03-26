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

Saved Best Model: Epoch 8, Val. Acc.: 0.7309
Epoch: 001, Train Loss: 0.5905, Val. Loss: 0.5734, Val. Acc.: 0.7309

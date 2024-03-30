# GATConv

### Model Architecture

    CorrectedGNN(
      (conv1): GATConv(1875, 64, heads=1)
      (conv2): GATConv(64, 64, heads=1)
      (lin): Linear(in_features=64, out_features=2, bias=True)
    )

### Results

Epoch: 003, Train Loss: 0.5265, Val. Loss: 0.9244, Val. Acc.: 0.6816
Training: 100%|██████████| 140/140 [05:33<00:00,  2.38s/it, loss=0.242]

Early stopping

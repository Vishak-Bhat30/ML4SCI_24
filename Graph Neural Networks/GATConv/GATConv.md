# GATConv

### Model Architecture

    CorrectedGNN(
      (conv1): GATConv(1875, 64, heads=1)
      (conv2): GATConv(64, 64, heads=1)
      (lin): Linear(in_features=64, out_features=2, bias=True)
    )

### Results

Epoch: 001, Train Loss: 0.6747, Val. Loss: 0.6509, Val. Acc.: 0.6502
Training: 100%|██████████| 140/140 [02:11<00:00,  1.07it/s, loss=0.764]

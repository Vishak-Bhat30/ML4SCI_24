# SAGEConv

### Model Architecture

    GraphSAGENet(
      (sage1): SAGEConv(1875, 512, aggr=mean)
      (sage2): SAGEConv(512, 256, aggr=mean)
      (sage3): SAGEConv(256, 128, aggr=mean)
      (dropout): Dropout(p=0.5, inplace=False)
      (lin): Linear(in_features=128, out_features=2, bias=True)
    )

### Results

Saved Best Model: Epoch 8, Val. Acc.: 0.6233
Epoch: 008, Train Loss: 0.6310, Val. Loss: 0.6810, Val. Acc.: 0.6233
Training: 100%|██████████| 140/140 [06:49<00:00,  2.92s/it, loss=0.801]


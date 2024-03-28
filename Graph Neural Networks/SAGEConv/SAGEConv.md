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

Saved Best Model: Epoch 5, Val. Acc.: 0.6744
Epoch: 005, Train Loss: 0.6234, Val. Loss: 0.6171, Val. Acc.: 0.6744

![GraphSAGE 67](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/b3e331f3-acc4-4d15-bfea-ae415847886c)

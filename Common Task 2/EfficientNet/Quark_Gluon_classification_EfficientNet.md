# Common Task 2. Quark/Gluon classification:

Task: To classify input as Quark/Gluon (EfficientNet).

    Datasets: https://cernbox.cern.ch/s/oolDBdQegsITFcv

This dataset was of the file format  .test.snappy.parquet extension
It contains a matrix of shape (3,) in which each element was an array of 125 elements and that 125 elements had 125 elements. 
The dataset also contained the m0 and pt values along with the target which was binary due to binary classification problem statement.


    Approach:
	Created a dataframe which has the matrix of images of shape  3,125,125 and pt m0 and label y. 


	Then I created the class dataset and dataloader and then split the data into training 
	and testing sets so that I can validate my model. 80% of the data were used for the 
	training and the remaining 20% was used for the test purpose.
------------------------------------------------------------------------------------------------------------------------------------------------------------------

    MODEL:
	Then the EfficientNet from the timm models was taken. 

------------------------------------------------------------------------------------------------------------------------------------------------------------------

	HyperParameters:
	→ criterion =  nn.CrossEntropyLoss()
	→ optimizer = optim.Adam()
  	→ scheduler = optim.lr_scheduler.StepLR()
    → learning_rate = 0.001
    → optimizer = optim.Adam()
    → number of epochs= 14
    → batch_size = 256
		
 ------------------------------------------------------------------------------------------------------------------------------------------------------------------

    Results: 
     Epoch 3/20 [Val] Loss: 3.2673, Acc: 0.5953: 100%|██████████| 59/59 [00:00<00:00, 67.72it/s]
    Epoch 3/20, Train Loss: 0.2260, Val Loss: 2.0355, Val Accuracy: 0.5953

     The model starts to overfit
             

![efficientnet](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/c02f96d3-b804-4022-b4ad-2ff36e1eb06f)

The above image is the training curve

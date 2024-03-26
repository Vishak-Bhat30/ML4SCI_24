# Common Task 2. Quark/Gluon classification:

Task: To classify input as Quark/Gluon (MobileNet).

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
	Then the MobileNet from the timm models was taken. 

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
     Epoch 5/20 [Val] Loss: 0.9942, Acc: 0.6280: 100%|██████████| 175/175 [00:02<00:00, 79.54it/s]
    Epoch 5/20, Train Loss: 0.1945, Val Loss: 1.2929, Val Accuracy: 0.6280

     The model starts to overfit
             
![mobilenet-](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/27280613-cd3e-4bd0-a0ce-a7cb0b4e5069)



The above image is the training curve

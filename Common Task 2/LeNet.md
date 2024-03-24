# Common Task 2. Quark/Gluon classification:

Task: To classify input as Quark/Gluon(LeNet).

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
	I tried few modeltaken from the timm models. I tried using mobilenet models, resnet , efficientnet, squeezenet, shufflenet, DenseNet
    and many more. Out of those A simple model similar to Lenet5 was performing the best. Other models were simply overfitting the training
     data.
        
 
	LeNet5(
      (conv1): Conv2d(3, 6, kernel_size=(5, 5), stride=(1, 1))
      (pool): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
      (conv2): Conv2d(6, 16, kernel_size=(5, 5), stride=(1, 1))
      (dropout1): Dropout(p=0.25, inplace=False)
      (fc1): Linear(in_features=12544, out_features=120, bias=True)
      (dropout2): Dropout(p=0.5, inplace=False)
      (fc2): Linear(in_features=120, out_features=84, bias=True)
      (fc3): Linear(in_features=84, out_features=2, bias=True)
    )
			  


	
------------------------------------------------------------------------------------------------------------------------------------------------------------------

	HyperParameters:
                → criterion =  nn.CrossEntropyLoss()
		→ optimizer = optim.Adam()
  		→ scheduler = optim.lr_scheduler.StepLR()
    		→ learning_rate = 0.0001
                → optimizer = optim.Adam()
                → number of epochs= 20
                → batch_size = 256
		
 ------------------------------------------------------------------------------------------------------------------------------------------------------------------

    Results: Epoch 14/20, Train Loss: 0.5254, Val Loss: 0.5763, Val Accuracy: 0.7158
	     The epoch 14 weights should be taken for the inference because after this point the 
	     training error and the validation error the difference increases.

             The model weight is present in the google drive here -  
        	

![__results___13_0](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/0b917835-9615-4063-afca-cffccde09857)

The above image is the training curve

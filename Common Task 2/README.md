# Common Task 2. Quark/Gluon classification:

Task: To classify input as Quark/Gluon.

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
	Then  the class of architecture which contains the architecture from nn.module was made. 
        The architecture was similar to VGG and had 12 total layers (9 convolutional, 3 fully connected) layers,
	where all the conv layers were having the kernel size of 3*3. 
 
	VGG12(
	  (features): Sequential(
	    (0): Conv2d(3, 64, kernel_size=(3, 3), stride=(1, 1))
	    (1): ReLU(inplace=True)
	    (2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1))
	    (3): ReLU(inplace=True)
	    (4): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
	    (5): Conv2d(64, 128, kernel_size=(3, 3), stride=(1, 1))
	    (6): ReLU(inplace=True)
	    (7): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1))
	    (8): ReLU(inplace=True)
	    (9): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
	    (10): Conv2d(128, 256, kernel_size=(3, 3), stride=(1, 1))
	    (11): ReLU(inplace=True)
	    (12): Conv2d(256, 256, kernel_size=(3, 3), stride=(1, 1))
	    (13): ReLU(inplace=True)
	    (14): Conv2d(256, 256, kernel_size=(3, 3), stride=(1, 1))
	    (15): ReLU(inplace=True)
	    (16): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
	    (17): Conv2d(256, 512, kernel_size=(3, 3), stride=(1, 1))
	    (18): ReLU(inplace=True)
	    (19): Conv2d(512, 512, kernel_size=(3, 3), stride=(1, 1))
	    (20): ReLU(inplace=True)
	    (21): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
	  )
	  (classifier): Sequential(
	    (0): Linear(in_features=4608, out_features=4096, bias=True)
	    (1): ReLU(inplace=True)
	    (2): Dropout(p=0.5, inplace=False)
	    (3): Linear(in_features=4096, out_features=512, bias=True)
	    (4): ReLU(inplace=True)
	    (5): Dropout(p=0.5, inplace=False)
	    (6): Linear(in_features=512, out_features=2, bias=True)
	  )
	)
			  


	
------------------------------------------------------------------------------------------------------------------------------------------------------------------

	HyperParameters:
                → criterion =  nn.CrossEntropyLoss()
                → optimizer = optim.Adam()
                → number of epochs= 14
                → batch_size = 256
 ------------------------------------------------------------------------------------------------------------------------------------------------------------------

    Results: Train Loss: 0.5258, Val Loss: 0.5746, Val Accuracy: 0.7256
	     The epoch 6 weights should be taken for the inference because after this point the 
	     training error and the validation error the difference increases.

             The model weight is present in the google drive here -  
        	https://drive.google.com/file/d/1O71TYGBMDg8TTDzjivJmJFM5AE-9KA8z/view?usp=sharing

![__results___14_0](https://github.com/Vishak-Bhat30/ML4SCI_24/assets/102585626/69763e74-aec8-46d7-a61b-97815006c237)
The above image is the training curve

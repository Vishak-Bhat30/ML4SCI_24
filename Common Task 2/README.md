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

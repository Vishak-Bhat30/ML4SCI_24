# ML4SCI

This repo contains the .ipynb and .pdfs of the model trained for ML4SCI for GSoC 2024.

# Common Task 1. Electron/photon classification:
         
Task: To classify input as Electron/Photons.

    Dataset :  The below dataset was  provided
    
                               https://cernbox.cern.ch/index.php/s/AtBT8y4MiQYFcgc (photons)	
 		                   https://cernbox.cern.ch/index.php/s/FbXw3V4XNyYB3oA(electrons)
                             
The dataset mainly contained files that were of .hdf5 format. 
The data contained the matrix in the shape of 32,32,2 were the 2 represented the number of channels.
The channels represented hit energy and time.
             



	Approach: --> Firstly I reshaped the matrix into 2,32,32 so that it could be fed into the neural network 

              --> Created a Dataset class that returns the matrix and the label for that matrix denoting the 
              class that matrix belongs to when an index is given under the __getitem__() function 

              --> Then I have made the dataLoader        

              --> The dataset is split into a train and a test set using the function train_test_split() of sklearn. 
              The test size is taken as 10 percent of the given data and the train size is implied that it will be 90 percent.
------------------------------------------------------------------------------------------------------------------------------------------------------------------

    MODEL: → Replicated Resnet architecture with 15 layers forming the Resnet15.
                 ResNet15(
		  (conv1): Conv2d(2, 64, kernel_size=(7, 7), stride=(2, 2), padding=(3, 3), bias=False)
		  (bn1): BatchNorm2d(64, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		  (maxpool): MaxPool2d(kernel_size=3, stride=2, padding=1, dilation=1, ceil_mode=False)
		  (layer1): Sequential(
		    (0): ResNetBlock(
		      (conv1): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
		      (bn1): BatchNorm2d(64, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
		      (bn2): BatchNorm2d(64, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (shortcut): Sequential()
		    )
		    (1): ResNetBlock(
		      (conv1): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
		      (bn1): BatchNorm2d(64, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
		      (bn2): BatchNorm2d(64, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (shortcut): Sequential()
		    )
		  )
		  (layer2): Sequential(
		    (0): ResNetBlock(
		      (conv1): Conv2d(64, 128, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1), bias=False)
		      (bn1): BatchNorm2d(128, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
		      (bn2): BatchNorm2d(128, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (shortcut): Sequential(
		        (0): Conv2d(64, 128, kernel_size=(1, 1), stride=(2, 2), bias=False)
		        (1): BatchNorm2d(128, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      )
		    )
		    (1): ResNetBlock(
		      (conv1): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
		      (bn1): BatchNorm2d(128, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
		      (bn2): BatchNorm2d(128, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (shortcut): Sequential()
		    )
		  )
		  (layer3): Sequential(
		    (0): ResNetBlock(
		      (conv1): Conv2d(128, 256, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1), bias=False)
		      (bn1): BatchNorm2d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (conv2): Conv2d(256, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
		      (bn2): BatchNorm2d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (shortcut): Sequential(
		        (0): Conv2d(128, 256, kernel_size=(1, 1), stride=(2, 2), bias=False)
		        (1): BatchNorm2d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      )
		    )
		    (1): ResNetBlock(
		      (conv1): Conv2d(256, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
		      (bn1): BatchNorm2d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (conv2): Conv2d(256, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
		      (bn2): BatchNorm2d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (shortcut): Sequential()
		    )
		  )
		  (layer4): Sequential(
		    (0): ResNetBlock(
		      (conv1): Conv2d(256, 512, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1), bias=False)
		      (bn1): BatchNorm2d(512, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (conv2): Conv2d(512, 512, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
		      (bn2): BatchNorm2d(512, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      (shortcut): Sequential(
		        (0): Conv2d(256, 512, kernel_size=(1, 1), stride=(2, 2), bias=False)
		        (1): BatchNorm2d(512, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
		      )
		    )
		  )
		  (avgpool): AdaptiveAvgPool2d(output_size=(1, 1))
		  (linear): Linear(in_features=512, out_features=2, bias=True)
		)

 ------------------------------------------------------------------------------------------------------------------------------------------------------------------
    HyperParameters:
                → criterion =  nn.CrossEntropyLoss()
                → optimizer = optim.Adam()
                → number of epochs= 20
                → batch_size = 256
                → learning_rate =  0.01
                → scheduler = ReduceLROnPlateau
                
    
------------------------------------------------------------------------------------------------------------------------------------------------------------------
     Results:
       
The model weights are the follows:

The above image is the training curve



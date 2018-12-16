# Convolutional_Neural_Networks
Creating CNNs using Keras

Homework Assignment 3: Convolutional Neural Networks
Depaul University 
CSC 578 Neural Networks and Deep Learning
Professor Noriko Tomuro
Fall 2018

The objective of this assignment is to enhance understanding of Convolutional
Neural Networks (CNNs) and to gain experience with Kaggle Competitions


1.	Load and Prepare Data (CIFAR-10)
	-	CIFAR-10 consists of 60k 32x32 color images in 10 classes,
		with 6,000 images per class. It is one of the most widely
		used benchmark datasets for image classification
	-	The code loads the data (packaged in Keras), split into
		three subsets(train/validation/test, for X and Y separately), and
		obtains the binarized one-hot-vector representation for the
		target (y) vectors.
	-	Preprocess the data:
		-	Scale the values of the images (X) to a range of 0 to 1
			for all three sets
		-	Show any one image per class from the training set
		-	Show the images in a grid format

2.	Build and Train Network
	-	Build a base model with the following configuration:
		-	[1st layer] Convolution -- 32 5x5 filters, stride (1,1), activation relu
		-	[2nd layer] Max pooling -- size 2x2, stride (2,2)
		-	[3rd layer] Convolution -- 32 5x5 filters, stride (1,1), activation relu
		-	[4th layer] Max pooling -- size 2x2, stride (2,2)
		-	[5th layer] Fully connected (Dense) -- 512 nodes, activation relu
		-	[6th layer] Fully connected (Dense) -- 10 nodes, activation softmax
	-	Note that you need to flatten the image before the fully connected layer

3.	Compile the Model
	-	Loss = 'categorical_crossentropy'
	-	Optimizer = 'adam'
	-	Metrics = ['accuracy']

4.	Train the Model
	-	Be sure to use the binarized y vectors (y_train_bin and y_valid_bin)
	-	Use the validation data for the validation_data option
	-	If desired, save the history of training for later use
	-	Monitor the training. Pay attention to overfitting

5.	Trying Different Architectures 
	-	Options:
		-	Add more convolutional layers
		-	Change the number of filters
		-	Change the size of the filters
		-	Add more fully connected layers
		-	Add dropout layers
		-	Add regularization
		-	Tweak hyper-parameters (eta, batch size etc.)

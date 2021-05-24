## Implementing transfer learning on art images dataset using three different pre-trained models

**Objective**

* Train pre-trained alexnet, vgg19 and resnet50 models using transfer learning on given art images dataset to compare and visualize their performance on different classes.

**Workflow**

1. Configure environment
	- Import the required packages & modules
	- Setting up the training mode based on CUDA capability
	
2. Data preparation
	- Data transformation where data are rotated, flipped, resized and cropped
	- Data loading using DataLoader from PyTorch

3. Modelling - Generate at least 2 models
	- Model Definition
		- Load the required pre-trained model
		- Replace the last layer with a custom linear classifier layer
		- Specify the loss function and the optimizer
	- Model Training & Validation
		- Training Preparation
		- Train and validate
	- Model Testing
		- Testing preparation
		- Test

4. Model saving

**Deliverable**

In this notebook we:
- downloaded and loaded pre-trained famous models.
- applied transfer learning using them on our dataset.
- compared, plotted and visualized the train, test and valid statistics.

The end deliverable from this section is three trained models using the pre-trained models. The expected accuracy of your model should be at least 80% on the test data. The code should include the following parts: data preparation, modelling and model saving.

**Importance to project**

The use of pre-trained models can dramatically reduce development time and complexity. It is important to be aware of these models, their transfer capacity and level of precision. Lastly, these models will be used as a base for the subsequent modules. 

**Notes (if applicable)**

There are multiple pre-trained models available and specific to computer vision. It is always worth checking which specific task they aim to solve. These tasks can be image generation, neural style transfer, image classification, image captioning, anomaly detection, and so on

**Resources**

- To help you understanding the concepts related to this milestone:
	- [Deep Learning with PyTorch](https://livebook.manning.com/book/deep-learning-with-pytorch/chapter-2/): this resource will help you to have a better understanding of pretrained models.
	- To have a better understanding of [pretrained models](https://www.manning.com/books/deep-learning-with-pytorch)
	- [Transfer learning for deep learning](https://machinelearningmastery.com/transfer-learning-for-deep-learning/): this resource gives a very clear and brief introduction to Transfer Learning.

- To help you in the resolution of the exercices:
	- [Deep Learning with PyTorch - Dataloader](https://livebook.manning.com/book/deep-learning-with-pytorch/chapter-14/73): this section provides explanations and examples about PyTorch dataloaders.
	- [Deep Learning with PyTorch - Models](https://livebook.manning.com/book/deep-learning-with-pytorch/chapter-8/182): this section explains how to implement a model in PyTorch.
	- [Deep Learning with PyTorch - Transforms](https://livebook.manning.com/book/deep-learning-with-pytorch/chapter-7/28): this section describes how PyTorch Transforms should be implemented.

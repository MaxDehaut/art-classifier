# Implementing customised classifier on art images

**Objective**

* Train a model from scratch on given art images dataset and visualize its performance on different classes.

**Workflow**

1. Configure environment
	- Import the required packages & modules
	- Setting up the training mode based on CUDA capability
	
2. Data preparation
	- Data transformation where data are rotated, flipped, resized and cropped
	- Data loading using DataLoader from PyTorch

3. Modelling
	- Model Definition
		- Initialise the CNN Model
		- Define the model flow (using forward method)
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
- build a customised classifier (CNN model) written in PyTorch
- aim to understand the main component of a model and how to configure them
- address three crucial steps of Neural Network Model implementation

The end deliverable from this section is a Jupyter Notebook containing a customized classifier (CNN model) written in PyTorch. The code should include the following parts: data preparation, modelling and model saving.

**Importance to project**

The use of customized models can dramatically improve development time and complexity. This milestone is crucial in the understanding of Deep Learning models. 

**Resources**

- To learn more about [CNN Architecture](https://livebook.manning.com/book/grokking-deep-learning-for-computer-vision/chapter-5/19)

- To help you in the resolution of the exercice:
	- To build the model architecture, you can find a good [example here](https://livebook.manning.com/book/grokking-deep-learning-for-computer-vision/chapter-3/257). The example is based on Keras but the structure is similar.
	- To familiarise yourself with the concept of loss function, the following [reference](https://livebook.manning.com/book/grokking-deep-learning-for-computer-vision/chapter-10/86)
	- To set the the optimizer, the following [reference](https://livebook.manning.com/book/grokking-deep-learning-for-computer-vision/chapter-4/310) will help.

**For further reading**

- You might want to consider to increase your understand of Deep Learning PyTorch models by reading [Deep Learning with PyTorch](https://www.manning.com/books/deep-learning-with-pytorch). The book gives an very clear end-to-end explanation of these models.
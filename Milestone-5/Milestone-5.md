# Applying Semantic Segmentation on Art images dataset

Image segmentation is the process of partitioning a digital image into multiple segments (sets of pixels, also known as image objects). Image segmentation is typically used to locate objects and boundaries (lines, curves, etc.) in images. More precisely, image segmentation is the process of assigning a label to every pixel in an image such that pixels with the same label share certain characteristics.

The first section of this notebook will help you to familiarise yourself with the use of pre-trained segmentation models. Globally, these models tend to perform well but the segmentation can be improved by using additional art images. The second section will show how these pre-trained models can be refined.
  
## Objective of this notebook
* Applying Semantic Segmentation on images from Art Paintings dataset using pre-trained DeepLabV3 model to detect various object boundaries.
* Train pre-trained DeepLabv3 model using transfer learning on given art images dataset.

**Workflow**

1. Configure environment
	- Import the required packages & modules
	- Setting up the training mode based on CUDA capability

2. Implementation of Pre-trained Model
	- Prepare the dataset
	- Apply semantic segmentation 

3. Implementation of Transfer Learning based on pre-trained model
	- Define a customised dataset 
	- Train and validate the customised model
	- Test the newly created customised model

 **Deliverable**

The end deliverable from this section is Jupyter Notebook containing the code which performs the semantic segmentation. This segmentation should leverage DeepLab v3 model. The code should include the following parts: semantic segmentation and transfer learning-based semantic segmentation.

**Importance to project**

Performing segmentation without knowing the exact identity of all objects in the painting is an important part of our visual understanding process which can give a powerful model to understand the painting and also be used to improve or augment existing computer vision techniques.

**Resources**

- To help you in the resolution of the exercice:
	- Insights on image conversion to a segmentation map can be found [here](https://numpy.org/doc/stable/reference/generated/numpy.zeros_like.html) and [here](https://numpy.org/doc/stable/reference/generated/numpy.stack.html?highlight=stack#numpy.stack)
	- Additional information regarding how to unsqueeze image can be found [here](https://pytorch.org/docs/stable/generated/torch.unsqueeze.html)
	- Look [here](https://pytorch.org/docs/stable/generated/torch.argmax.html?highlight=argmax#torch.argmax) for help on how to take a max index for each pixel position

- Books & Projects you might want to consider:
	- [Deep Learning with PyTorch](https://www.manning.com/books/deep-learning-with-pytorch)
	- [Art Style Transfer Using Neural Networks](https://www.manning.com/liveproject/art-style-transfer-using-neural-networks)

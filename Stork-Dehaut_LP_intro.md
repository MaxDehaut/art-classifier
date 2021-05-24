# about this liveProject
Imagine that you are a data scientist at the (fictional) World wide Painting Museum. The museum has decided to digitalize the painting collection of several well know museums and you have been tasked to create an index of the paintings. This index should group the paintings based on their art categories. Considering the number of paintings, you are considering using Machine Learning techniques. The curator likes the idea but has challenged you on several points: how relevant is the dataset, which categories will be used to group the paintings, which techniques will be used and will they come to the same conclusions, how accurate a machine learning model can be ...

The purpose of this liveProject is to address these challenges related to the the implemetation of identifying a painting using Machine Learning techniques. Going further and considering that the range of styles in photographs is limited compared to art categories, this liveProject can also be seen as an introduction to architecture of Neural Network models.


# Techniques employed

The following are some of the techniques you’ll employ throughout this project. Don’t worry if you haven’t mastered one of these areas; we’ll give you the resources to learn more. Data scientists must use a diverse range of techniques, many of which are picked up on the job for a specific project!

Listed under the bullets are the Python libraries for the technique.

* Extracting images from various sources (webscrapping, zipfile)
  * [request](https://pypi.org/project/requests/) is a simple and easy to use HTTP library
  * [ZipFile](https://docs.python.org/3/library/zipfile.html) supports decryption of encrypted files in ZIP archives

* Elaboration of a Convolutional neural network
  * [Pytorch](https://pytorch.org/)
  * [Image transforation](https://pytorch.org/docs/stable/torchvision/transforms.html)

* Implementation of [pre-trained models](https://www.analyticsvidhya.com/blog/2020/08/top-4-pre-trained-models-for-image-classification-with-python-code/)

* [Image Segmentation](https://en.wikipedia.org/wiki/Image_segmentation#:~:text=In%20digital%20image%20processing%20and,also%20known%20as%20image%20objects).&text=Image%20segmentation%20is%20typically%20used,lines%2C%20curves%2C%20etc.))

Resources are provided for working with these techniques/libraries both as embedded in Manning liveBooks and as links to external documentation. On the job, you will often be given partial information and must learn how to seek out relevant resources on your own!


# Project outline

This liveProject will be broken into 5 milestones:

**[1]. [Data Collection and preparation]**
This milestone helps to collect images and to build a structure which will facilitate the model training and testing phases.

**[2]. [Transfer Learning]**
The milestone helps to understand how pre-trained models can help in classifying the paintings based on their genre.

**[3]. [Art Classifier]**
This milestone focuses on the implementation of a convolutional neural network in order to classify the paintings based on their genre.

**[4]. [Visualizing Statistics]**
This milestone aims to compare the performance of each models and their respective metrics.

**[5]. [Image Segmentation]**
In this milestone, you will learn how to label a group of common pixels.

Please note that the documentation is embedded within the notebook.


# Prerequisites
This liveProject is intended for intermediate Python programmers with at least some deep learning experience, preferably in image classification with convolutional neural networks. Knowledge of PyTorch would be helpful, but is not required. To begin this liveProject, you will need to be familiar with:

* TOOLS
   * Basics of Pytorch: you understand the purpose of Pytorch and the concept of tensor.
   * Intermediate Python
      * Familiar with Python syntax incl. importing modules
      * Basic IO manipulation using PIL module
      * Basic debugging (console, print)
      * Basic numeric processing using NumPy
      * Basic plotting using MatplotLib

* TECHNIQUES (if applicable)
   * Classification as a machine learning task
   * Understand the concepts of transfer learning
   * Intermediate deep learning concepts such as convolutional neural networks


# Python libraries and setup
This uses Python 3.8. It is recommended to use the Anaconda distribution of Python and conda for managing the libraries.

The following Python libraries will be utilized in this project. Again, you don’t need working experience with all of these, as you can pick up the basics by reading documentation and putting them to use.

* PIL: For object-oriented filesystem path management
* NumPy: For numerical processing
* matplotlib: For general visualization
* jupyter: For running Jupyter Notebooks
* pytorch: For supporting the model building process

To install these libraries, clone the base Git repository to your computer and run conda env create -f environment.yml from the root project directory (assuming you are using conda).

Once the virtual environment is created, you can activate it with conda activate imageSeg and run a Jupyter Notebook with jupyter notebook.

Any additional libraries you need can be installed with conda install “library.” Managing Python package versions with virtual libraries is a crucial data science skill to avoid situations where code that works on one machine causes errors on another!


# Recommended resources	

These are resources directly referenced throughout the liveProject and can directly impact or expand your understanding of the liveProject's content.

* [Data Science Bookcamp](https://livebook.manning.com/book/data-science-bookcamp/welcome/v-3/) by Leonard Apeltsin
* [The Quick Python Book, Third Edition](https://livebook.manning.com/book/the-quick-python-book-third-edition/about-this-book/) by Naomi Ceder
* [Think Like a Data Scientist](https://livebook.manning.com/book/think-like-a-data-scientist/about-this-book/) by Brian Godsey
* [Deep Learning for Vision Systems](https://livebook.manning.com/book/deep-learning-for-vision-systems) by Mohamed Elgendy
* [Deep Learning with PyTorch](https://livebook.manning.com/book/deep-learning-with-pytorch) by Eli Stevens, Luca Antiga, and Thomas Viehmann

* Documentation on Python libraries:
   * [pandas](https://pandas.pydata.org/pandas-docs/stable/)
   * [matplotlib](https://matplotlib.org/3.1.1/contents.html)
   * [scikit-learn](http://scikit-learn.org/stable/documentation.html)
   * [Python official docs](https://docs.python.org/3/)

We provide additional resources and tutorials throughout the project. Feel free to use any resources you can find to complete the project. If you run into problems or have questions, refer to the Frequently Asked Question (FAQs) within the Summary section.


# For further reading

	- [Grokking Artificial Intelligence Algorithms](https://livebook.manning.com/book/grokking-artificial-intelligence-algorithms)
   - [Grokking Deep Reinforcement Learning](https://livebook.manning.com/book/grokking-deep-reinforcement-learning)

Additional resources and tutorials are provided throughout the project. Feel free to use any resources you can find to complete the project.
If you run into problems or have questions, refer to the Frequently Asked Questions (FAQs) within the Summary section.
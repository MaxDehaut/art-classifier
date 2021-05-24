## Data Collection and Preparation

**Objective**

* Data collection and preparation is a crucial step of model building. In this milestone, you will learn two techniques to collect images and how to build a structure which will facilitate the model training and testing.

**Workflow**

1. Extract images from various sources:
   	* The first technique will extract a set of images from an archive file.
	* The second download technique will be based on a file containing a list of urls.
		* This technique offers a higher level of flexibility.

2. Prepare the data to facilitate the elaboration of model:
   	* Create a typical structure containing `test`, `train` and `valid` folders
	* Split the downloaded images across the three folders based on a 60/20/20 distribution
	* Move the images downloaded in phase 1

**Deliverable**

In this notebook we:
- collect a set of images for multiple art categories
- created a structure that will be faciliate the model building

The end deliverable from this section is a dataset folder containing a typical structure (`test`, `train` and `valid`) with the images to be processed.

**Importance to project**

* Data collection and preparation can be extremely tidious. Automate this process is therefore crucial.
* Using a typical structure can dramatically facilitate the elaboration of a model.

**Notes (if applicable)**

* Feel free to download as many art categories and images as you want but please note that it will not necessarily reinforce the accuracy of the model. Indeed some categories overlaps.

**Resources**

- To help you in the resolution of the exercice:
	- To retrieve the list of folders/files, you might consider using [Pathlib](https://livebook.manning.com/book/the-quick-python-book-third-edition/chapter-12/search-search-39).
	- To filter the list of files based on the extension, you might consider using [Pathlib - Glob](https://livebook.manning.com/book/the-quick-python-book-third-edition/chapter-20/57).
	- To split the set of images, you will use the [Numpy - Split](https://numpy.org/doc/stable/reference/generated/numpy.split.html)

**For further reading**

- You might want to consider to increase your understand of Python by reading [The Quick Python Book, 3rd Edition](https://livebook.manning.com/book/the-quick-python-book-third-edition)


## [Data Collection and Preparation]
**Graduated Help**
Feeling stuck? Use as little or as much help as you need to reach the solution!

*help*
* To retrieve the list of folders/files, you might consider using [Pathlib](https://livebook.manning.com/book/the-quick-python-book-third-edition/chapter-12/search-search-39).
* To filter the list of files based on the extension, you might consider using [Pathlib - Glob](https://livebook.manning.com/book/the-quick-python-book-third-edition/chapter-20/57).
* To split the set of images, you will use the [Numpy - Split](https://numpy.org/doc/stable/reference/generated/numpy.split.html)

*more help*

* Hint for step 1: The flow should be:
	* Checking that the file path is a correct path
	* For function 1: Returning the list of files filtered by extension (check `glob`)
	* For function 2: Returning a **sorted** list of folders excluding those starting with the prefix

* Hint for step 2: The flow should be:
	* Lists all the 'jpg' images in the folder
	* Shuffle the images - source code provided
	* Determine a splitting index: 5 = 20%
	* Split the files across the 3 datasets

*partial solution*

* Step 1 should look like:
	```
	# Retrieves the list of files with a directory
	def getFilesInDirectory(pathToDir, extension = "*.*"):
		if  ...:
			...
		return ...

	# Retrieves the list of folders with a directory
	def getFolderNamesInDirectory(pathToDir, prefix = ""):
		if  ...:
			...
		return ...
	```

* Step 2 should look like:
	```
	# Sets the datasets
	files = ...
	random.shuffle( files )
	split_idx = ...
	split_images = ...	
	```

*full solution*

  [INSERT  ... - Solution.ipynb](http://www.manning.com)

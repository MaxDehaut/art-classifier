
LINK TO QUIZ QUESTION TYPES: https://livebook.manning.com/exercise-examples

## <div style="text-align: justify"> This quiz will give you a good idea of the skills needed to complete this liveProject. While it's optional, we recommend all learners take it before beginning.</div>

Under each question write:

Explain: [EXPLANATION OF THE ANSWER AND A RESOURCE (PREFERABLY MANNING) OR TWO TO HELP PERFECT THE FEATURED SKILL] 


1. You would like to retrieves a sorted list of folders within a directory (here called 'pathToDir'). Which of the following line is correct:

_[ sorted([fld.name for fld in pathToDir.iterdir() if fld.is_dir()]) ]_

[ ([fld.name for fld in pathToDir.iterdir() if fld.is_dir()]).sort() ]

[ ([fld.name for fld in pathToDir.iterdir() if fld.is_dir()]) ]

Explain:
[All the entries within the directory 'pathToDir' are filtered by type (directory or a file). A list is created and then sorted. ]
- [List - Sorting](https://livebook.manning.com/book/the-quick-python-book-third-edition/chapter-5/89])


2. Before splitting a list into several groups, you would like to shuffle its content. Which approach would you pick ?

_[ random.sample(theList) ]_

_[ random.shuffle(theList) ]_

[ theList = random.sample(seed=123)] ]

Explain:
[Depending on whether you want to keep the original list or not, you will either execute random.sample (which returns a *NEW* shuffled list) or random.shuffle (returning the original list). ]
- [Random - Shuffle](https://livebook.manning.com/book/tiny-python-projects/chapter-16/9])


3. Why should you choose GPU over CPU when it is down to model training ?

[ GPUs contain more complex cores ]_

_[ GPUs manage concurrent hardware threads ]_

_[ GPUs handle better floating-point throughput ]_


4. What would be the 3 main layers of Convolutional Neural Networks ?

_[Convolution, Pooling and Fully Connected]_

[Data Transformation, Data Conversion, Data Classification]

[Convolution, Optimization and Loss Function]

Explain: The three main components of CNNs are described [here](https://livebook.manning.com/book/grokking-deep-learning-for-computer-vision/chapter-3/)

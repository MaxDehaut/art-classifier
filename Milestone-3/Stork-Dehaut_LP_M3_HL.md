
## [Art Classifier]
**Graduated Help**
Feeling stuck? Use as little or as much help as you need to reach the solution!

*help*
* To build the model architecture, you can find a good [example here](https://livebook.manning.com/book/grokking-deep-learning-for-computer-vision/chapter-3/257). The example is based on Keras but the structure is similar.
* To familiarise yourself with the concept of loss function, the following [reference](https://livebook.manning.com/book/grokking-deep-learning-for-computer-vision/chapter-10/86)
* To set the the optimizer, the following [reference](https://livebook.manning.com/book/grokking-deep-learning-for-computer-vision/chapter-4/310) will help.

*more help*

* Hint for step 1: The flow should be:
	* Define the architecture of the model (`__init()__`)
        * Define 5 layers of 2D convolution using `nn.Conv2d`
        * Define 1 layer for 2D max pooling using `nn.MaxPool2d`
        * Define 1 layer for DropOut using `nn.Dropout`
        * Define 3 fully connected layers using `nn.linear`
    * Define the architecture flow
        * For each convolutional layer:
            * Set the activation function using `relu`
            * Set a max pooling layer after each convolutional layer
        * Flat the output of convolutional part using `view()`
        * Apply each fully connected layer
        * Drop out each fully connected layers.
	* Instantiate the model

* Hint for step 2: The flow should be:
	* Set the loss function
    * Set the optimizer


*partial solution*

* Step 1 should look like:
	```
    class Net(nn.Module):

        def __init__(self):
            super(Net, self).__init__()

            self.conv1 = nn. ...
            self.conv2 = nn. ...
            self.conv3 = nn. ...
            self.conv4 = nn. ...
            self.conv5 = nn. ...

            self.maxpool = nn. ...        

            self.dropout = nn. ...

            self.fc1 = nn. ... 
            self.fc2 = nn. ...
            self.fc3 = nn. ...
            
        def forward(self, x):
            x = F.relu(self.conv1(x))
            x = self.maxpool(x)
            ...
            ...
            
            x = x.view( ... )
            
            x = self.dropout(x)
            x = self.dropout(F.relu(self.fc1(x)))

            ...
            
            return x

    # instantiate the CNN
    model_scratch = Net()

    # move model to GPU if CUDA is available
    if train_on_gpu == True:
        model_scratch.to(device)
    ```

* Step 2 should look like:
	```
    ### Set loss function
    criterion = nn. ...

    ### Set optimizer
    optimizer = optim. ...
	```

*full solution*

  [INSERT  ... - Solution.ipynb](http://www.manning.com)

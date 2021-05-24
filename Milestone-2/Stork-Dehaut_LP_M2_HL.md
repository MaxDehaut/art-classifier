
## [Transfer Learning]
**Graduated Help**
Feeling stuck? Use as little or as much help as you need to reach the solution!

*help*
- [Deep Learning with PyTorch - Dataloader](https://livebook.manning.com/book/deep-learning-with-pytorch/chapter-14/73): this section provides explanations and examples about PyTorch dataloaders.
- [Deep Learning with PyTorch - Models](https://livebook.manning.com/book/deep-learning-with-pytorch/chapter-8/182): this section explains how to implement a model in PyTorch.
- [Deep Learning with PyTorch - Transforms](https://livebook.manning.com/book/deep-learning-with-pytorch/chapter-7/28): this section describes how PyTorch Transforms should be implemented.


*more help*

* Hint for step 1: The flow should be:
	* Define the data-augmentation transforms and apply
        * Randomly rotating the training
        * Randomly cropping and resizing it
        * Randomly flipping it horizontally
        * Convert to tensor
        * Apply normalization
    * Data augmentation isn't applied on validation and testing set.
        * These images are resized to 256 pixels and then cropped from center to make it 224-dim square images.
    * Load and apply above transforms on the 3 datasets using ImageFolder

* Hint for step 2: The flow should be:
	* Prepare one data loader for each train, test and validation

* Hint for step 3 (optional but recommended): The flow should be:
	* Define one data-augmentation transform resizing to 256 pixels and then cropping from center to make it 224-dim square images.
    * Load and apply above transforms on dataset using ImageFolder
	* Prepare one data loader for the visualisation

* Hint for step 4: The flow should be:
    * Print in/out features. The features are either located under the fully connected layer or under the classifier, depending on the type of pre-trained models used.
    * Store the features into a variable ( n_inputs )
    * Add the features to a linear layer (n_inputs, nbr of art categories)
    * Set the linear layer as the last layer to the model

* Hint for step 5: The flow should be:
    * Declare the criterion based on CrossEntropyLoss method from Pytorch.nn module
    * Based on the pre-trained model, declare the optimizer based on Adam. Use the parameters of the model.

* Hint for step 6: The flow should be:
    * Iterate through the train dataloader
    * Set the gradients of the optimizer to zero using the appropriate method of the optimizer class
    * Use the criterion to evaluate the batch loss based on the outputs & labels
    * Convert raw output values into probabilities using exponential function (torch)

* Hint for step 7: The flow should be:
    * Iterate through the test dataloader
    * Use the criterion to evaluate the batch loss based on the outputs & labels


*partial solution*

* Step 1 should look like:
	```
    train_transforms = transforms.Compose([transforms. ...,     # Rotation
                                        transforms. ...,        # Resized crop
                                        transforms. ...,        # Horizontal flip
                                        transforms.ToTensor(),
                                        transforms. ...])       # Normalise
                    
    test_transforms  = transforms.Compose([transforms. ...,     # Resize
                                        transforms. ...,        # Center & Crop
                                        transforms.ToTensor(),
                                        transforms. ...])       # Normalise
                    
    valid_transforms  = transforms.Compose([transforms. ...,    # Resize
                                        transforms. ...,        # Center & Crop
                                        transforms.ToTensor(),
                                        transforms. ...])       # Normalise
                    
    train_dataset = datasets.ImageFolder( ... )
    test_dataset  = datasets.ImageFolder( ... )
    valid_dataset = datasets.ImageFolder( ... )
    ```

* Step 2 should look like:
	```
    train_dataloader = torch.utils.data.DataLoader(..., batch_size=..., num_workers=..., shuffle = ...)
    test_dataloader  = torch.utils.data.DataLoader(..., batch_size=..., num_workers=..., shuffle = ...)
    valid_dataloader = torch.utils.data.DataLoader(..., batch_size=..., num_workers=..., shuffle = ...)
	```

* Step 3 (optional but recommended) should look like:
	```
    visual_transforms = transforms.Compose([transforms. ...,
                                        transforms. ...,
                                        transforms. ...])

    visual_dataset = datasets.ImageFolder(..., transform=...)

    visualization_dataloader = torch.utils.data.DataLoader(..., batch_size=..., num_workers=..., shuffle=...)

    dataiter = iter(visualization_dataloader)
    images, labels = dataiter.next()

    images = images.numpy()

    plotCols = 4
    plotRows = math.ceil(batch_size/plotCols)
    fig = plt.figure(figsize=(25, 25))
    for idx in np.arange(batch_size):
        ax = fig.add_subplot(plotRows, plotCols, idx+1, xticks=[], yticks=[])
        plt.imshow(np.transpose(images[idx], (1, 2, 0)))
        ax.set_title(artCategories[labels[idx]])
	```

* Step 4 should look like:
	```
    print(model. ... .in_features) 
    print(model. ... .out_features) 
    n_inputs = model. ... .in_features
    last_layer = nn.Linear(n_inputs, len(artCategories))
    model. ... = last_layer
	```

* Step 5 should look like:
	```
    criterion = nn.CrossEntropyLoss()

    if model_name == 'resnet50':
        optimizer = optim.Adam(model. ... .parameters(), lr=0.001)
    else:
        optimizer = optim.Adam(model. ... .parameters(), lr=0.001)
	```

* Step 6 (only the missing line of code are shown) should look like:
	```
    # Getting one batch of images and their corresponding true labels
    for batch_i, (images, labels) in enumerate(..._dataloader):

    # clear the previous/buffer gradients of all optimized variables
    optimizer. ...()
    
    # calculate the batch loss
    loss = criterion(..., ...)

    # calculate the batch loss
    batch_loss = criterion(..., ...)
    validation_loss += batch_loss.item()
    
    # Calculating accuracy
    ps = torch.exp( ... )
	```

* Step 7 (only the missing line of code are shown) should look like:
	```
    # iterate over test data - get one batch of data from testloader
    for images, labels in ..._dataloader:
    
    # calculate the batch loss
    loss = criterion(..., ...)
	```


*full solution*

  [INSERT  ... - Solution.ipynb](http://www.manning.com)

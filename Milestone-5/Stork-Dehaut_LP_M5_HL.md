
## [Applying Semantic Segmentation on Art images dataset]
**Graduated Help**
Feeling stuck? Use as little or as much help as you need to reach the solution!

*help*
- Insights on image conversion to a segmentation map can be found [here](https://numpy.org/doc/stable/reference/generated/numpy.zeros_like.html) and [here](https://numpy.org/doc/stable/reference/generated/numpy.stack.html?highlight=stack#numpy.stack)
- Additional information regarding how to unsqueeze image can be found [here](https://pytorch.org/docs/stable/generated/torch.unsqueeze.html)
- Look [here](https://pytorch.org/docs/stable/generated/torch.argmax.html?highlight=argmax#torch.argmax) for help on how to take a max index for each pixel position


*more help*

* Hint for step 1: Write the `decode_segmap` function. The flow should be:
	* Store the number of labels
    * Initialise the channels r/g/b with zeros using `zeros_like` from numpy package
    * Loop on the categories
        * Get the indexes in the image where that particular class label is present
        * Assign to each indexed channel the corresponding color where that class label is present
    * Stack the 3 separate channels into one `RGB` image using `stack` from numpy package

* Hint for step 2: Complete the `segment` function. The flow should be:
	* Apply the `segment_transforms` against the local image and then add a dimension using `unsqueeze(0)`
    * Execute the model and retrieve the `out`
    * Apply argmax method on the output previsouly squeezed, based on dimension '0'
    * Lastly, invoke `decode_segmap` method with the required arguments

* Hint for step 3: Complete the Transformation & Data loaders definition. The flow should be:
	* Instantiate the `SegmentationDataset` class passing the appropriate parameters for both training (`T`) and validation (`V`)
    * Ïnstantiate the `DataLoader` for both training (`T`) and validation (`V`). The parameters for DataLoader are similar to what you have done in the previous milestones.

* Hint for step 4: Complete the Training and Validation phase. The flow should be:
	* The model mode can activate through `train()` or `eval()` methods.
    * Predictions should be collected through `max()` method


*partial solution*

* Step 1 should look like:
	```
    len_categories = len(label_colors)
    
    r = np.zeros_like(...).astype(np...)
    g = 
    b = 

    for l in range(0, len_categories):
        idx = image == l
        r[...] = label_colors[..., ...]
        g...
        b...

    rgb = np.stack(...)
    ```

* Step 2 should look like:
	```
    inp = segment_transforms(...)....to(device)
    out = seg_model.to(device)(...)...
    image = ...(...).detach().cpu().numpy()
    rgb = decode_segmap(...)
    ```

* Step 3 should look like:
	```
    tv_datasets = {x: SegmentationDataset(pathToSegmentedImg, pathToSegmentedMask, x) for x in ['T', 'V']}
    tv_dataloaders = {x: DataLoader(tv_datasets[x], batch_size=batch_size, drop_last=True, shuffle=True, num_workers=num_workers) for x in ['T', 'V']}
    ```

* Step 4 should look like:
	```
    if phase == 'T':
        # Set to training mode
        seg_model.train()
    else:
        # Set to evaluation mode
        seg_model.eval()


    # Returns the maximum values (tuple: values, indices) of each row of the `outputs` in the dimension `1`
    _, preds = (outputs, 1)

    ```


*full solution*

  [INSERT  ... - Solution.ipynb](http://www.manning.com)

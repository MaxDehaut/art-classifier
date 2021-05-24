
## [Visualizing statistics]
**Graduated Help**
Feeling stuck? Use as little or as much help as you need to reach the solution!

*help*
- Use this [reference](https://matplotlib.org/3.3.3/api/_as_gen/matplotlib.pyplot.plot.html) if you need help in building plots.


*more help*

* Hint for step 1: The flow should be:
	* In the previous paragraph, we have loaded the checkpoints saved with each model.
    * Go through each checkpoint in the checkpoint 'library' to collect each metric
    * Go through each metric and display its content

* Hint for step 2: The flow should be:
	* Go through the collection of checkpoints
    * Add to the losses (training, valid) to the declared collections
    * Add to the accuracy to the declared collection
    * Add to the class accuracy (testing) to the declared collection
    * Add the length of the training lossed to the number of epochs collection
    * Collect the maximum number of epochs

* Hint for step 3: The flow should be:
	* x-Axis represents the number of epochs
    * On the y-Axis:
        * y should show the training losses
        * z should show the valid losses

* Hint for step 4: The flow should be:
    * the `ys` collection should contain the training losses
    * the plot should show the `x`, the `ys` and use the model name as a label


*partial solution*

* Step 1 should look like:
	```
    for ... in ...:
        for ... in ...:
            print(...)
    ```

* Step 2 should look like:
	```
    for checkpoint in checkpoints:
        ... .append( checkpoint. ... )
        ... .append( checkpoint. ... )
        ... .append( checkpoint. ... )
        ... .append( checkpoint. ... )
        ... .append( len( checkpoint. ... ) )
        max_numEpoch = ...(max_numEpoch, len(checkpoint. ...) )
    ```

* Step 3 should look like:
	```
    x = epochs
    y = training_losses[ ... ]
    z = valid_losses[ ... ]
    ```

* Step 4 should look like:
	```
    x = epochs
    ys = []
    for i in range(len(model_names)):
        ys.append( ... )

    plt.xlabel('Epoch')
    plt.ylabel('Training Loss')
    plt.title('Training Loss  v/s Epoch')

    for i in range(len(model_names)):
        plt.plot( ... )

    plt.legend()
    plt.show()
    ```

*full solution*

  [INSERT  ... - Solution.ipynb](http://www.manning.com)

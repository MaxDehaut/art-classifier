# Plotting and Visualizing Statistics of models trained on Art Paintings dataset

**Objective**

* Compare the performance of the 4 image classification models i.e. 3 different transfer learning algorithms and CNN model from scratch.
* Plot and visualize different charts to compare the results which help to determine the best model.

**Workflow**

1. Configure environment
	- Import the required packages & modules

2. Preparing and collecting the metrics
	- Load the previoulsy saved models using a function like `torch.load`.
	- Extract the above model performance parameters from the dictionary checkpoint objects.

3.	Plotting and Visualizing
	- Plot Loss v/s Epoch graphs for each model individually
	- Plot Training loss v/s epoch (grouped in single plot) and Validation Loss v/s epoch (grouped in single plot) 
	- Plot Accuracy v/s Epoch (grouped in single plot)
	- Visualize Class wise overall accuracy for all models individually using horizontal bar chart.
	- Visualize and Compare individual class accuracies of all the models (grouped in single bar chart)

 **Deliverable**

The end deliverable from this section is Jupyter Notebook containing plots obtained by visualizing train, valid and test statistics of saved trained models. The code should include the following parts: metrics preparation, modelling and model saving.

**Importance to project**

Assessing model performance is a crucial phase of model building process. Multiples evaluation techniques exists to help you understanding how accurate models are which will determine whether or not models can be used.

**Resources**

- To learn more about Performance and Accuracy, the following [section](https://livebook.manning.com/book/grokking-deep-learning-for-computer-vision/chapter-4/26) will help you to better understand the concepts.

- To help you in the resolution of the exercice:
	- Use this [reference](https://matplotlib.org/3.3.3/api/_as_gen/matplotlib.pyplot.plot.html) if you need help in building plots.

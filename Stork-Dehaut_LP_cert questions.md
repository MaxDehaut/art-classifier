
LINK TO QUIZ QUESTION TYPES: https://livebook.manning.com/exercise-examples

## <div style="text-align: justify"> This certificate exam will give you a good idea of the skills learned while completing this liveProject. This exam is required in order to receive a certificate of completion.</div>

Under each question write:

Explain: [EXPLANATION OF THE ANSWER AND A RESOURCE (PREFERABLY MANNING) OR TWO TO HELP EXPLAIN THE FEATURED SKILL. REFERENCING A SPECIFIC MILESTONE WHEN THIS WAS LEARNED IS ALSO HELPFUL.] 


1. What would be the typical transformations applied on images during the training phase (in the context of Art Paintings) ?

_[Resize]_

[Collate]

_[Rotation]_

[Blur]

Explain:
[Data augmentation can be performed by applying, amongst others, resize, crop, rotation, flip, ... ]
- [Deep Learning with PyTorch - Transforms](https://livebook.manning.com/book/deep-learning-with-pytorch/chapter-7/28): this section describes how PyTorch Transforms should be implemented.


2. What could be the right definition for a loss function ?

_[A loss function evaluates the distance between the value estimated by the model and its predicted value, for a given input]_

[A loss function adjusts the weights of the model during the training phase]

[A loss function adjusts the weights of the model during the testing phase]

Explain:
[The loss function is used to evaluate how far the model output/prediction is far from the actual value. The weights are adjusted by the optimizer.]
- [reference](https://livebook.manning.com/book/grokking-deep-learning-for-computer-vision/chapter-10/86)


3. What is an activation function ?

_[An activation function helps to decide if a neuron should be "fired" or not]_

[An activation function is used to format the data during the data augmentation phase]

[An activation function computes and minimizes the gradient at each epoch]

Explain:
[The activation function add non-linearity to the output of a layer before being sent to the next layer]
- [reference](https://livebook.manning.com/book/deep-learning-with-python-second-edition/chapter-4/v-5/67)


4. Which of these are potentially valid metrics for model performance evaluation ?

[Training loss]

[Intersection-Over-Union]

_[Accuracy classification score]_

Explain:
[Multiple metrics can be evaluated during the elaboration of the model. Some metrics are of course more applicable to some techniques than others.] - [reference](https://livebook.manning.com/book/inside-deep-learning/chapter-2/v-2/209)


5. Which statement resets the gradients of all optimized tensors to zero ?

[optimizer.gradients = 0]

[optimizer.init()]

_[optimizer.zero_grad()]_

Explain:
[zero_grad() sets to 0 all the optimized tensors.] - [reference](https://pytorch.org/docs/stable/optim.html)


6. Which statement saves a model that has been trained ?

[model.save(location)]

_[torch.save(model.state_dict(), location)]_

[torch.serialize(model)]

Explain:
[torch.save() is the appropriate method to save a model.] - [reference](https://pytorch.org/docs/stable/generated/torch.save.html?highlight=save#torch.save)


7. Which statement returns the indices of the maximum values of a tensor across a dimension ?

_[torch.argmax(...)]_

[torch.argmin(...)]

[torch.argsum(...)]

Explain:
[Argmax is the correct statement] - [reference](https://pytorch.org/docs/stable/generated/torch.argmax.html?highlight=argmax#torch.argmax)

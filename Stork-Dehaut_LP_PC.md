## Project Conclusions

Congratulations, you have reached the end of this challenging liveBook. You came across multiple techniques such as pretrained models, Convolutional Neural Networks (CNN), Transfer Learning, Semantic Segmentation.

You have learned that there are multiple pretrained models available which address specific needs. Alexnet, Resnet or VGG help to identify objects and classify images into art categories. Despite the limited number of categories, the pretrained models do not perform on well art categories as they would do on other classes. There are multiple reasons for this, the main one being these models were trained on day to day objects. A different classification, based on the painter for instance, would have probably given better results. The choice of classifying based on the art categories is justified by the objective of implementing your own model. 

You then have learned how to build a customised classifier model based on CNN architecture. This should have given you a good understanding of what a fully connected network requires and its major components: loss function, an optimizer, a network of nodes. If customised models require much more effort and knowledge they can better perform than pretrained models and help to address specific requirements.

Whatever the model you use, the understanding of its performance is a crucial step in the model lifecycle. This understanding can be facilitated by the use of plots. In addition, it is also important to use multiple criterias for each models. This was the purpose of Milestone 4.

The objective of the last milestone was to approach art paintings classification from a different angle. Semantic segmentation aims to tag sets of pixels with a label. In this chapter, you have been able to check your understanding of the use of pre-trained models. You probably notice that semantic segmentation tends to perform much better on art paintings.

Now, where could you go from here ? We have listed a serie of paths you might want to consider, based on the domain of expertise:
* Technical:
    * You might consider to extend your understanding of Deep Learning techniques related to Computer Vision;
* Classification:
    * You might try to evaluate other pre-trained models, ResNet for instance has multiple versions;
    * You could elaborate a much more sophisticated and complex customised model;
* Semantic Segmentation:
    * You could elaborate your own customised semantic segmentation model;
* Object Detection, being a combination of semantic segmentation and localisation
    * You might want to consider the use of pre-trained models, specific to object detection;
* Instance segmentation
    * You could consider to refine the semantic segmentation technique applying instance segmentation.

As you can see, this liveBook aims to extend your perspectives. Who knows where this will bring you ;-)

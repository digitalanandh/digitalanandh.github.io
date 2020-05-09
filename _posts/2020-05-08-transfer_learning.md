# Transfer Learning in deep learning

Transfer learning is a technique which allows developers to use a pre-trained neural network from one domain to another. This technique has been found to be very useful and has produced state of the art results.

Common examples of transfer learning can be seen in image recognition space. A pre-trained convolutional neural network (e.g. ResNet-34 or ResNet-50) can be used to identify other animals like bears, horses etc. or even some other shapes like cricket bat or baseball bat.

One more field where transfer learning has been useful is the speech recognition using recurrent neural networks.

For transfer learning, we usually delete the last layer(s) of the pre-trained model usually called the head and then run the model again on the new dataset to update the weights of the later layers (especially the head).

**_How does this work?_**  
The answer lies in understanding how the deep learning model learns to identify the different objects/features or parts of the objects layer by layer.  
The work done by Matthew Zeiler and Rob Fergus [Visualizing and Understanding Convolutional Networks](https://arxiv.org/pdf/1311.2901.pdf) shows how to visualize the neural network weights learner in each layer of the model.

If we look at couple of images of activations of early layers of a CNN, we should be able to understand how transfer learning works and how it can be helpful in a lot of other tasks.

![Layer1](/images/layer1.png "Activations of early layers of a CNN by Matthew D. Zeiler and Rob Fergus")  

If we look at the subset of the features which is shown in the image above, we can see that the model has discovered weights which represent diagonal, horizontal and vertical edges as well as gradients. These are the basic building blocks which the model has created automatically for computer vision.  

The next layer is shown below.
![Layer2](/images/layer2.png "Activations of early layers of a CNN by Matthew D. Zeiler and Rob Fergus")  

The left hand side of the image shows the reconstruction of model weights and the right hand side of the image shows small patches from the actual images which these features most closely match. We can see that the model has learnt to create feature detectors that look like corners, repearing lines, circles and other simple patterns.  

Similarly, the higher level layers of the neural network are able to learn about high level semantic components like ears, legs, tails (in case of animal classifier) etc.  
Since, the lower layers in the pre-trained models learn about basic building blocks of computer vision, which highly resembles the basic visual machinery of human eye, they can be used in other domains of computer vision or image recognition. This is how a pre-trained model with a little bit of fine tuning can help us in other aspects of our study.  

Currently, there are only few domains (image recognition, speech recognition etc.) where we have pre-trained models available (at least during the writing of this post). It would be really great to have these pre-trained models for as many domains as possible.  



>**References:**
>
>1. [Book: Deep Learning for Coders with fastai and PyTorch](https://learning.oreilly.com/library/view/deep-learning-for/9781492045519/)  
>2. [Visualizing and Understanding Convolutional Networks](https://arxiv.org/abs/1311.2901)

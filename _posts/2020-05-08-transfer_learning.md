# Transfer Learning in deep learning

Transfer learning is a technique which allows developers to use a pre-trained neural network from one domain to another. This technique has
been found to be very useful and has produced state of the art results.

Common examples of transfer learning can be seen in image recognition space. A pre-trained convolutional neural network (e.g. ResNet-34 or ResNet-50)
can be used to identify other animals like bears, horses etc. or even some other shapes like cricket bat or baseball bat.

One more field where transfer learning has been useful is the speech recognition using recurrent neural networks.

For transfer learning, we ususally delete the last layer(s) of the pre-trained model usually called the head and then run the model again on the new dataset
to update the weights of the later layers (especially the head).

**_How does this work?_**  
The answer lies in understanding how the deep learning model learns to identify the different objects/features or parts of the objects layer by layer.  
The work done by Matthew Zeiler and Rob Fergus [Visualizing and Understanding Convolutional Networks](https://arxiv.org/pdf/1311.2901.pdf) shows how to 
visualize the neural network weights learner in each layer of the model. 

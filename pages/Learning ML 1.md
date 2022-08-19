# Deeplizard
https://deeplizard.com/learn/video/gZmobeGL0Yg

![](Pasted%20image%2020211212134550.png)

## [[Machine learning]]
> Machine learning is the practice of using algorithms to analyze data, learn from that data, and then make a determination or prediction about new data.
>
## [[Deep learning]]
The neural networks that we use in deep learning aren't actual biological neural networks though. They simply share some characteristics with biological neural networks, and for this reason, we call them _artificial_ neural networks ([[ANN]]s).

For now, here is what you need to know:

1.  ANNs are built using what we call neurons.
2.  Neurons in an ANN are organized into what we call layers.
3.  Layers _within_ an ANN (all but the input and output layers) are called hidden layers.
4.  If an ANN has more than one hidden layer, the ANN is said to be a deep ANN.

![deep neural network with 4 layers](https://deeplizard.com/assets/png/c0870acb.png)

In summary, deep learning uses ANNs that have multiple hidden layers. Keep this in mind as we move forward in this series, and it will become more clear as we continue our journey through deep learning.

## Artificial Neural Networks Explained

> An artificial neural network is a computing system that is comprised of a collection of connected units called neurons that are organized into what we call layers.

The connected neural units form the so-called network. Each connection between neurons transmits a signal from one neuron to the other. The receiving neuron processes the signal and signals to downstream neurons connected to it within the network. Note that neurons are also commonly referred to as _nodes_.

Different layers perform different kinds of transformations on their inputs. Data flows through the network starting at the input layer and moving through the hidden layers until the output layer is reached. This is known as a forward pass through the network. Layers positioned between the input and output layers are known as hidden layers.

Nodes are organized into what we call layers. At the highest level, there are three types of layers in every ANN:
1.  Input layer - One node for each component of the input data.
2.  Hidden layers - Arbitrarily chosen number of nodes for each hidden layer.
3.  Output layer - One node for each of the possible desired outputs.

![](Pasted%20image%2020211212113525.png)

Here, the nodes are depicted with the circles, so let's consider how many nodes are in each layer of this network.

Number of nodes in each layer:

1.  Input layer (left): 2 nodes
2.  Hidden layer (middle): 3 nodes
3.  Output layer (right): 2 nodes

Since this network has two nodes in the input layer, this tells us that each input to this network must have two dimensions, like for example _height_ and _weight_.

Since this network has two nodes in the output layer, this tells us that there are two possible outputs for every input that is passed forward (left to right) through the network. For example, _overweight_ or _underweight_ could be the two output classes. Note that the **output classes are also known as the prediction classes.**

Dense is the most basic kind of layer in an ANN and that each output of a dense layer is computed using every input to the layer.

First we import the required [[Keras]] classes.

```
from keras.models import Sequential
from keras.layers import Dense, Activation
```

Then, we create a variable called `model`, and we set it equal to an instance of a `Sequential` object.

```model = Sequential(layers)```

To the constructor, we pass an array of `Dense` objects. Each of these objects called `Dense` are actually layers.

```
layers = [
    Dense(units=3, input_shape=(2,), activation='relu'),
    Dense(units=2, activation='softmax')
]
```

The first parameter passed to the `Dense` layer constructor in each layer tells us **how many neurons** it should have.

The **input shape** parameter `input_shape=(2,)` tells us how many neurons our input layer has, so in our case, we have two.

Lastly, we have a parameter for a so-called **activation function**. An activation function is a non-linear function that typically follows a dense layer.

1.  `activation='relu'`
2.  `activation='softmax'`

## Layers In A [[Neural Network]] Explained

Each of the eight nodes in this layer represents an **individual feature from a given sample in our dataset.**

 The examples we looked at showed the use of dense layers, which are also known as fully connected layers. There are, however, different types of layers. Some examples include:

-   Dense (or fully connected) layers
-   Convolutional layers
-   Pooling layers
-   Recurrent layers
-   Normalization layers

For example, a convolutional layer is usually used in models that are doing work with image data. Recurrent layers are used in models that are doing work with time series data, and fully connected layers, as the name suggests, fully connects each input to each output within its layer.

### Layer Weights

**Each connection between two nodes has an associated weight,** which is just a number.

Each weight represents the strength of the connection between the two nodes. When the network receives an input at a given node in the input layer, this input is passed to the next node via a connection, and the **input will be multiplied by the weight assigned to that connection.**

1. For each node in the second layer, a **weighted sum is then computed with each of the incoming connections**. 
2. This sum is then passed to an **activation function, which performs some type of transformation on the given sum.** For example, an activation function may transform the sum to be a number between zero and one. The actual transformation will vary depending on which activation function is used. More on activation functions [later](https://deeplizard.com/learn/video/m0pIlLfpXWE).

```
node output = activation(weighted sum of inputs)
```

### Forward Pass Through A Neural Network

Once we obtain the output for a given node, the obtained output is the value that is passed as input to the nodes in the next layer.

This process continues until the output layer is reached. The number of nodes in the output layer depends on the number of possible output or prediction classes we have.

Our final product looks like this:

```
from keras.models import Sequential
from keras.layers import Dense, Activation

layers = [
    Dense(units=6, input_shape=(8,), activation='relu'),
    Dense(units=6, activation='relu'),
    Dense(units=4, activation='softmax')
]

model = Sequential(layers)
```

### Activation Functions In A Neural Network
> In an artificial neural network, an activation function is a function that maps a node's inputs to its corresponding output.

#### Sigmoid Activation Function

Sigmoid takes in an input and does the following:

-   For most negative inputs, sigmoid will transform the input to a number very close to 0.
-   For most positive inputs, sigmoid will transform the input into a number very close to 1.
-   For inputs relatively close to 0, sigmoid will transform the input into some number between 0 and 1.

Mathematically, we writesigmoid(x)=exex+1

![sigmoid function graph from wikipedia](https://deeplizard.com/assets/svg/d6f5d567.svg)

So, for sigmoid, 0 is the lower limit, and 1 is the upper limit.

#### Activation Function Intuition

Well, an activation function is biologically inspired by activity in our brains where different neurons fire (or are activated) by different stimuli.

![chocolate chip cookie](https://deeplizard.com/assets/jpg/3d5eae08.jpg)

For example, if you smell something pleasant, like freshly baked cookies, certain neurons in your brain will fire and become activated. If you smell something unpleasant, like spoiled milk, this will cause other neurons in your brain to fire.

Deep within the folds of our brains, certain neurons are either firing or they're not. This can be represented by a 0 for not firing or a 1 for firing.

```
// pseudocode
if (smell.isPleasant()) {
    neuron.fire();
}
```

With the Sigmoid activation function in an artificial neural network, we have seen that the neuron can be between 0 and 1, and the closer to 1, the more activated that neuron is while the closer to 0 the less activated that neuron is.

#### Relu Activation Function

Now, it's not always the case that our activation function is going to do a transformation on an input to be between 0 and 1.

In fact, one of the most widely used activation functions today called _ReLU_ doesn't do this. ReLU, which is short for _rectified linear unit_, transforms the input to the maximum of either 0 or the input itself.

$$relu(x)=max(0,x)$$

So if the input is less than or equal to 0, then relu will output 0. If the input is greater than 0, relu will then just output the given input.

```
// pseudocode
function relu(x) {
    if (x <= 0) {
        return 0;
    } else {
        return x;
    }
}
```

To understand why we use activation functions, we need to first understand linear functions.

Suppose that f is a function on a set X.  
Suppose that a and b are in X.  
Suppose that x is a real number.

The function f is said to be a linear function if and only if:

$$f(a+b)=f(a)+f(b)$$

and

$$f(xa)=xf(a)$$

An important feature of linear functions is that the** composition of two linear functions is also a linear function.** This means that, even in very deep neural networks, if we only had linear transformations of our data values during a forward pass, the learned mapping in our network from input to output would also be linear.

Typically, the types of mappings that we are aiming to learn with our deep neural networks are more complex than simple linear mappings.

This is where activation functions come in. **Most activation functions are non-linear, and they are chosen in this way on purpose.** Having non-linear activation functions allows our neural networks to compute arbitrarily complex functions.

### Training An Artificial Neural Network
When we train a model, we're basically trying to solve an optimization problem. We're trying to optimize the weights within the model. Our task is to find the weights that most accurately map our input data to the correct output class. This mapping is what the network must _learn_.

Recall, we touched on this idea in our [post about layers](https://deeplizard.com/learn/video/FK77zZxaBoI). There, we showed how each connection between nodes has an arbitrary weight assigned to it. During training, these weights are iteratively updated and moved towards their optimal values.

```
// pseudocode
def train(model):
    model.weights.update()
```

#### Optimization Algorithm

The weights are optimized using what we call an optimization algorithm. The optimization process depends on the chosen optimization algorithm. We also use the term _optimizer_ to refer to the chosen algorithm. The most widely known optimizer is called _stochastic gradient descent_, or more simply, SGD.

**When we have any optimization problem, we must have an optimization objective**, so now let's consider what SGD's objective is in optimizing the model's weights.

The objective of SGD is to minimize some given function that we call a _loss function_. So, SGD updates the model's weights in such a way as to make this loss function as close to its minimum value as possible.

Alright, but what _is_ the actual **loss** we're talking about? Well, during training, we supply our model with data and the corresponding labels to that data.

For example, suppose we have a model that we want to train to classify whether images are either images of cats or images of dogs. We will supply our model with images of cats and dogs along with the labels for these images that state whether each image is of a cat or of a dog.

Suppose we give one image of a cat to our model. Once the forward pass is complete and the cat image data has flowed through the network, the model is going to provide an output at the end. This will consist of what the model thinks the image is, either a cat or a dog.

In a literal sense, the **output will consist of probabilities for cat or dog. **For example, it may assign a 75% probability to the image being a cat, and a 25% probability to it being a dog. In this case, the model is assigning a higher likelihood to the image being of a cat than of a dog.

-   75% chance it's a cat
-   25% chance it's a dog

If we stop and think about it for a moment, this is very similar to how humans make decisions. Everything is a prediction!

The loss is the error or difference between what the network is predicting for the image versus the true label of the image, and SGD will to try to minimize this error to make our model as accurate as possible in its predictions.

## How A Neural Network Learns Explained
#### Gradient Of The Loss Function

After the loss is calculated, the gradient of this loss function is computed with respect to each of the weights within the network. **Note, _gradient_ is just a word for the derivative of a function of several variables.**

At this point, we've **calculated the loss of a single output**, and we **calculate the gradient of that loss with respect to our single chosen weight.** This calculation is done using a technique called _backpropagation_, which is covered in full detail starting [here](https://deeplizard.com/learn/video/XE3krf3CQls).

Once we have the **value for the gradient of the loss function**, we can use this **value to update the model's weight**. The **gradient tells us which direction will move the loss towards the minimum**, and our task is to move in a direction that lowers the loss and steps closer to this minimum value.

#### Learning Rate

We then **multiply the gradient value** by something called a _learning rate_. A learning rate is a small number usually ranging between 0.01 and 0.0001, but the actual value can vary.

**The learning rate tells us how large of a step we should take in the direction of the minimum.**

#### Updating The Weights

Alright, so we **multiply the gradient with the learning rate, and we subtract this product from the weight**, which will give us the new updated value for this weight.

$$new weight=old weight−(learning rate∗gradient)$$

When the gradient of the loss function is computed, the value for the gradient is going to be different for each weight because the gradient is being calculated with respect to each weight.
The weights are going to be **incrementally getting closer and closer to their optimized values** while SGD works to minimize the loss function.

At the end of each epoch during the training process, the loss will be calculated using the network's output predictions and the true labels for the respective input.

## Loss In A Neural Network Explained

Suppose our model is classifying images of cats and dogs, and assume that the label for cat is 0 and the label for dog is 1.

-   cat: 0
-   dog: 1

Now suppose we pass an image of a cat to the model, and the provided output is 0.25. In this case, the difference between the model's prediction and the true label is 0.25−0.00=0.25. This difference is also called the _error_.

$$error=0.25−0.00=0.25$$

This process is performed for every output. For each epoch, the error is accumulated across all the individual outputs.

### Mean Squared Error (MSE)

For a single sample, with MSE, we first calculate the difference (the error) between the provided output prediction and the label. We then square this error. For a single input, this is all we do.

$$MSE(input)=(output−label)(output−label)$$

If we passed **multiple samples** to the model at once (a batch of samples), then we would take the **mean of the squared errors over all of these samples.**

For example, we averaged the squared errors to calculate MSE, but other loss functions will use other algorithms to determine the value of the loss.

If we passed our entire training set to the model at once, then the process we just went over for calculating the loss will occur at the end of each epoch during training.

If we split our training set into batches, and passed batches one at a time to our model, then the **loss would be calculated on each batch.**

With either method, since the loss depends on the weights, we **expect to see the value of the loss change each time the weights are updated**. Given that the objective of SGD is to minimize the loss, we want to see our loss decrease as we run more epochs.

---
The currently available [loss functions for Keras](https://keras.io/losses/) are as follows:

-   mean_squared_error
-   mean_absolute_error
-   mean_absolute_percentage_error
-   mean_squared_logarithmic_error
-   squared_hinge
-   hinge
-   categorical_hinge
-   logcosh
-   categorical_crossentropy
-   sparse_categorical_crossentropy
-   binary_crossentropy
-   kullback_leibler_divergence
-   poisson
-   cosine_proximity

---
## Learning Rate In A Neural Network Explained
Recall that we start the training process with **arbitrarily set weights**, and then we incrementally update these weights as we move **closer and closer to the minimized loss**.

Now, the **size of these steps** we're taking to reach our minimized loss is going to depend on the **learning rate**. Conceptually, we can think of the learning rate of our model as the _step size_.

We know that during training, after the loss is calculated for our inputs, the gradient of that loss is then calculated with respect to each of the weights in our model.

Once we have the value of these gradients, this is where the idea of our learning rate comes in. The gradients will then get multiplied by the learning rate.

$$gradients * learning rate$$

The **learning rate** is another one of those _hyperparameters_ that we have to test and tune with each model before we know exactly where we want to set it, but as mentioned earlier, a typical guideline is to set it somewhere between `0.01` and `0.0001`.

### Batch Size In Artificial Neural Networks
> The _batch size_ is the number of samples that are passed to the network at once.

#### Batches In An Epoch

Let's say we have `1000` images of dogs that we want to train our network on in order to identify different breeds of dogs. Now, let's say we specify our batch size to be `10`. This means that `10` images of dogs will be passed as a group, or as a batch, at one time to the network.

Given that a single epoch is one single pass of all the data through the network, it will take `100` batches to make up full epoch. We have `1000` images divided by a batch size of `10`, which equals `100` total batches.

$$batches\ in\ epoch = training\ set\ size / batch_size$$

The trade-off, however, is that even if our machine can handle very large batches, the **quality of the model may degrade as we set our batch larger** and may ultimately cause the model to be unable to generalize well on data it hasn't seen before.

In general, the **batch size** is another one of the _hyperparameters_ that we must test and tune based on how our specific model is performing during training. This parameter will also have to be tested in regards to how our machine is performing in terms of its resource utilization when using different batch sizes.

#### Mini-Batch Gradient Descent

Additionally, note if using _mini-batch gradient descent_, which is normally the type of gradient descent algorithm used by most neural network APIs like Keras by default, the gradient update will occur on a **per-batch basis**. The size of these batches is determined by the batch size.

This is in contrast to _stochastic gradient descent_, which implements gradient updates **per sample**, and _batch gradient descent_, which implements gradient updates **per epoch**.

---
### Fine-Tuning Neural Networks
> **Transfer learning** occurs when we use knowledge that was gained from solving one problem and apply it to a new but related problem.

_Fine-tuning_ is a way of applying or utilizing **transfer learning**. Specifically, fine-tuning is a process that takes a model that has already been trained for one given task and then tunes or tweaks the model to make it perform a second similar task.

### How To Fine-Tune

Going back to the example we just mentioned, if we have a model that has already been trained to recognize cars and we want to fine-tune this model to recognize trucks, we can first import our original model that was used on the cars problem.

For simplicity purposes, let's say we **remove the last layer** of this model. The last layer would have previously been classifying whether an image was a car or not. After removing this, we want to add a new layer back that's purpose is to classify whether an image is a truck or not.

In some problems, we may want to remove more than just the last single layer, and we may want to add more than just one layer. This will depend on how similar the task is for each of the models.

# [[Word2vec]]
#learn #programming 

Word2vec is a two-layer [[neural net]] that processes text by “vectorizing” words. Its input is a text corpus and its output is a set of vectors: feature vectors that represent words in that corpus. While Word2vec is not a [deep neural network](https://wiki.pathmind.com/neural-network), it turns text into a numerical form that deep neural networks can understand.

Given enough [[data]], usage and contexts, Word2vec can make highly accurate guesses about a word’s meaning based on past appearances. Those guesses can be used to establish a word’s association with other words (e.g. “man” is to “boy” what “woman” is to “girl”), or cluster documents and classify them by topic.

Measuring [cosine similarity](https://wiki.pathmind.com/glossary#cosine), no similarity is expressed as a 90 degree angle, while total similarity of 1 is a 0 degree angle, complete overlap; i.e. Sweden equals Sweden, while Norway has a cosine distance of 0.760124 from Sweden, the highest of any other country.

Here’s a list of words associated with “Sweden” using Word2vec, in order of proximity:

![cosine distance](https://wiki.pathmind.com/images/wiki/sweden_cosine_distance.png)

The nations of Scandinavia and several wealthy, northern European, Germanic countries are among the top nine.

Word2vec is similar to an autoencoder, encoding each word in a vector, but rather than training against the input words through reconstruction, as a [restricted Boltzmann machine](https://wiki.pathmind.com/restricted-boltzmann-machine) does, word2vec trains words against other words that neighbor them in the input corpus.

It does so in one of two ways, either using context to predict a target word (a method known as continuous bag of words, or CBOW), or using a word to predict a target context, which is called skip-gram. We use the latter method because it produces more accurate results on large datasets.

![diagrams](https://wiki.pathmind.com/images/wiki/word2vec_diagrams.png)

A well trained set of word vectors will place similar words close to each other in that space. The words _oak_, _elm_ and _birch_ might cluster in one corner, while _war_, _conflict_ and _strife_ huddle together in another.

Similar things and ideas are shown to be “close”. Their relative meanings have been translated to measurable distances. Qualities become quantities, and algorithms can do their work. But similarity is just the basis of many associations that Word2vec can learn. For example, it can gauge relations between words of one language, and map them to another.

![translation](https://wiki.pathmind.com/images/wiki/word2vec_translation.png)

### N-grams & Skip-grams

Words are read into the vector one at a time, _and scanned back and forth within a certain range_. Those ranges are n-grams, and an n-gram is a contiguous sequence of _n_ items from a given linguistic sequence; it is the nth version of unigram, bigram, trigram, four-gram or five-gram. A skip-gram simply drops items from the n-gram.

The skip-gram representation popularized by Mikolov and used in the DL4J implementation has proven to be more accurate than other models, such as continuous bag of words, due to the more generalizable contexts generated.

This n-gram is then fed into a neural network to learn the significance of a given word vector; i.e. significance is defined as its usefulness as an indicator of certain larger meanings, or labels.

### Advances in NLP: ElMO, BERT and GPT-3

Word2vec is an algorithm used to produce distributed representations of words, and by that we mean _word types_; i.e. any given word in a vocabulary, such as _get_ or _grab_ or _go_ has its own word vector, and those vectors are effectively stored in a lookup table or dictionary. Unfortunately, this approach to word representation does not addres polysemy, or the co-existence of many possible meanings for a given word or phrase. For example, _go_ is a verb and it is also a board game; _get_ is a verb and it is also an animal’s offspring. The meaning of a given word type such as go or get varies according to its context; i.e. the words that surround it.

### GloVe: Global Vectors

Loading and saving GloVe models to word2vec can be done like so:

```
        WordVectors wordVectors = WordVectorSerializer.loadTxtVectors(new File("glove.6B.50d.txt"));
```

## Cosine similarity
https://en.wikipedia.org/wiki/Cosine_similarity


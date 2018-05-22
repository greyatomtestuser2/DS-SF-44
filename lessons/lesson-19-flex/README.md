---
title: Neural Networks
duration: "2:00"
creator:
    name: Adam Jones
    city: SF
---

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Neural Networks
DS | Lesson 19

### LEARNING OBJECTIVES
*After this lesson, you will be able to:*
- Understand various types of neural networks
- Applications of neural networks
- Apply a neural network model for regression
- Apply a neural network model for classification


### STUDENT PRE-WORK
*Before this lesson, you should already be able to:*
- Understand Logistic Regression and link functions
- Be familiar with training and testing classifiers and regressors

## Artificial Neural Networks (60 mins)

We all use computers everyday, but sometimes they fail us and this upsets a lot of people. What we'd like is for our computers to be smarter and more user friendly. So some smart people thought- ‘we should try to make them think more like humans!’

Despite everything computers today can do they're pretty simple: they take some inputs, perform some calculations, and produce some outputs. We’ve known for a while that the tiniest components of your brain that makes it think and do smart things are special cells called neurons. Your brain has billions of these things and they talk to each other using electrical impulses. Essentially, they are what’s responsible for making your brain think and have a consciousness.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/1/10/Blausen_0657_MultipolarNeuron.png/1280px-Blausen_0657_MultipolarNeuron.png)

So, some computer scientists had the idea that we can make a computer that is modeled after this system of neuronal connections they called their idea a neural network. The idea is that we have nodes that have some connections between them. This is similar to the neurons in your brain and the synapses they form- To get a neuron there to do something we trigger a node with some input and that node in turn triggers the nodes it is connected to.

Since we're used to the computer model of computation we'd like to have well-defined input and output nodes. We’d also like to have directed connections so that we know which way information is going. Some connections should be more important than others, and this is dictated by values known as weights.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/b/be/Single_layer_ann.svg/329px-Single_layer_ann.svg.png)

The purpose of having different connection weights is that it allows our nodes to behave more like real neurons. When a node is stimulated by two different nodes you can decide which of the two is more important to it by their connection weights. For example. if the connection weights between B and C is much larger than the connection weight between A and C, then node C decides B is more important to it and takes its value more often though.

But we still need a way for each node to decide independently whether they want to respond to their triggers at all. So, each node gets to think about what it will do. In order to decide, each node is given what is called a transfer function to judge its inputs. Since in the real world, computers treat all data as numbers the transfer function is a math equation (it's usually not that complicated). After the node makes a decision it sets its value and then it can trigger the next set of nodes with that value. Choosing whether or not to accept the triggered value is most important for the output nodes since these are the nodes that produce the results.

One of the most important questions is how the connection weights are determined. As it turns out, the neural networks can learn them. Does this make neural networks smart? Sort of, but it also turns out that the neural networks are very slow learners.

It's done through a process called back propagation. We start with random connection weights. Then for a given set of inputs, we decide on a set of desired outputs. Using the random weights, we first let the network calculate some outputs. Then, we compare the outputs that the neural net calculated to the desired outputs that we defined. Since we gave the network random weights we obviously cannot expect the two outputs to be equal. So we find their difference- we call this difference the ‘error’. We find the error by simply subtracting.

Now that we have the errors we need to adjust the connection weights to try to produce smaller errors. This is where the back propagation comes in. The new weights are calculated using an equation based on the old weights, the nodes input value, the error, and something called the learning rate. Hidden nodes calculate their own error before then pushing the errors back through the hidden nodes and adjusting their weights behind them. This goes on until all the weights have been adjusted and all the nodes have been assigned an error.

The idea is to determine which nodes are most to blame for the error in the output and try to adjust their weights the most. Now that all the weights have been updated the network tries out the original inputs again and outputs should be closer to the desired output. But, there will still be some error so the whole process is repeated again and again and again. Eventually, the network will produce the desired outputs. To try to produce the desired up more quickly we can try adjusting the learning rate and we can change the number of nodes.

So can neural networks make computers think like humans? Not exactly but they can still be very useful!

**Examples**:    
- [Character Encoding](http://yann.lecun.com/exdb/publis/pdf/jackel-95.pdf)
- [Medical Images](https://www.scientificamerican.com/article/deep-learning-sharpens-views-of-cells-and-genes/?utm_source=twitter&utm_medium=social&utm_campaign=sa-editorial-social&utm_content=&utm_term=health_&sf178179792=1)
- [Image Colorization](http://tinyclouds.org/colorize/)
- [Hotdog Detection](https://medium.com/@timanglade/how-hbos-silicon-valley-built-not-hotdog-with-mobile-tensorflow-keras-react-native-ef03260747f3)

---

### BEFORE NEXT CLASS
|   |   |
|---|---|
| **UPCOMING PROJECTS**  | [Final Project, Part 5](../../projects/final-projects/05-presentation/README.md) |

### ADDITIONAL RESOURCES
- Great neural network courses: http://www.fast.ai/

---
layout: post
title: A Completely Randomly Recurring Neural Network
---

Most Artificial Neural Networks today require a preset architecture or structure, neuron interconnections are predefined, parameters are set or at least sanely initialized and only then is the network set in motion.
This got me wondering, could such a setup ever evolve naturally? Could the entire network evolve around a suitably defined problem?
After all we are all a product of a naturally evolved neural network. If we want to truly claim to understand neural networks we should be able to reproduce this process, at least partially.

In my sparse free time I thought of a simple problem, a moving dwindling food source and creatures who could move, procreate, see and consume this food.
The creatures start with a random neuron setup, neurons themselves grow connections towards other neurons, procreate and consume the food for each of their actions.
If the food runs out the creature dies.

The results were predictably random. Probably because even evolution requires a suitable gradient to explore. 

You can see a branch of the simulation running on heroku here: [heroku](http://radiant-taiga-61859.herokuapp.com/)


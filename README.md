# Pytorch-EMNIST-Classification
### Objectives
* Observe how depth of a CNN model affects efficiency, accuracy and training loss 
* Try creating a more advanced CNN model that can be easily tuned
* Apply various hyperparameter tuning techniques to CNN models
-----------------------------


### Implementation
**[Balanced EMNIST Dataset](https://www.nist.gov/itl/products-and-services/emnist-dataset)**

![image](https://user-images.githubusercontent.com/67905366/127757068-89c8a36f-1836-429d-a443-cd662567616c.png)

**Argparse**: used to organize hyperparameters 

![image](https://user-images.githubusercontent.com/67905366/127756324-bf818b52-bb71-463b-871f-007b0ff200f3.png)

**Varying Depths of Convolutional Layers**: used 3 different model codes

![image](https://user-images.githubusercontent.com/67905366/127756391-77a67399-633d-43a2-beee-672e88519dfb.png)

**Pytorch**: a CNN model 

![image](https://user-images.githubusercontent.com/67905366/127756441-627f2850-a0c6-4eda-8fac-f4b8f3f05fc7.png)

-----------------------------
### Observation

Adding more convolutional layers becomes obsolete after a certain threshold
  * Execution time got extended significantly
  * There was a clear trade off between performance vs efficiency
  * Model 4 (the model of the highest depth) performed worse than Model 3

Optimizers
  * To my surprise, train loss and validation loss did not change much with the adam optimizer
  * Training loss and validation loss improved gradually with the SGD optimizer
    * The sgd optimizer showed improvements up to model 3
  * The Adam optimizer had tendency to overfit data in all models

Side Note
* Building a model is about finding the right balance between performance and efficiency
-----------------------------


### Conclusion
After certain number of convolutional layers, the difference in performance between models is quite insignificant; however, the execution time always tend to increase with the depth, causing unwanted inefficiency. Therefore, adding complexity does not always result in improvements to a deep learning model.

In my opinion, a combination of random searching and grid searching to find the optimal number of convolutional layers would be a good approach in reaching the ideal balance between performance and efficiency.

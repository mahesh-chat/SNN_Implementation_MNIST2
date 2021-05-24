# SNN_Implementation_MNIST2
 It contains 3 different implementations of SNN using 3 different loss functions .(cross entropy , online triplet loss , offline triplet loss)

Dataset is downloaded from :-https://www.kaggle.com/zalando-research/fashionmnist


Triplet Loss
It is a distance based loss function that operates on three inputs:
1. anchor (a) is any arbitrary data point,
2. positive (p) which is the same class as the anchor
3. and negative (n) which is a different class from the anchor


Mathematically, it is defined as: L=max(d(a,p)−d(a,n)+margin,0).
We minimize this loss, which pushes d(a,p) to 0 and d(a,n) to be greater than d(a,p)+margin. This means that, after the training, the positive examples will be closer to the anchor while the negative examples will be farther from it. The image below shows the the effect of minimizing the loss.

Triplet Mining for training:-
A model can be trained on triplets by using either offline or offline triplet mining.
1. Offline Triplet Mining: In this approach, we first generate the triplets manually and then fit the data to the network.
2. Online Triplet Mining: In this approach, we feed a batch of training data, generate triplets using all examples in the batch and calculate the loss on it. This approach 


allows us to randomize the triplets and increase the chance to find triplets with high losses — this will help train the model faster. For batch size of N, we can generate at most N ³ triplets.




Binary cross entropy is defined as:- 


![0_qbA8jq4Cv0dPbKhL](https://user-images.githubusercontent.com/46081668/119406302-3a423800-bd00-11eb-8fe4-cd91b2146726.png)





Accruacy achieved using cross entropy is 72 percent .


Accuracy achieved using Offline triplet loss is 50 percent.


Accuracy achieved using online triplet loss is 82 percent.

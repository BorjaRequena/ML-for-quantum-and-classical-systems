This folder contains the slides and an ipython notebook with a tutorial on deep neural networks, deep convolutional neural works and how to train them with fastai.

## Homework Fully Connected and Convolutional Neural Network (Alexandre Dauphin)


**First assignment (warmup):** 

- Implement the k-means algrithm from scratch for a two dimensional dataset. Benchmark it for an example with 2 and 3 clusters. You can generate benchmark examples with [make_blobs](http://scikit-learn.org/stable/modules/generated/sklearn.datasets.make_blobs.html#sklearn.datasets.make_blobs). Show a scatter plot of the results where the color corresponds to the results of the k-means algorithm. What happens if you ask k-means to find more clusters than the real number?
- Edit the notebook of the course and the Dropout function to the fully connected neural network. Look at the Loss function and the accuracy of both training and validation sets. Describe the effect of the Dropout.
- Run the unsupervised algorithm t-SNE (an implementation is present in scikit learn) on the original MNIST data and compare with the results of PCA. Is there some interesting structure in the original data?
- Plot the first and second eigenvectors of the PCA analysis. What do you see? Tip: You can extract the eigenvectors from the plot_PCA function by setting `eigv=True`. Don't forget to reshape the vector in the form of an image

**Second assignment:**

- Import the cifar10 dataset (present in fastai)
- Explore the different kind of images present in the dataset.
- This dataset is known to be much more difficult to classify than the MNIST dataset.
- Do a PCA analysis of the original data. Is there some visible structure in the data?
- Implement a fully connected neural network to classify the cifar10 dataset (you can use a similar architecture to the one for the MNIST with redefined dimensions, do 20 epochs). It should work poorly. 
- Do a PCA analysis on the output. 
- Implement a CNN. I propose the following structure: 7 convolutional layers with respectively 32,32,64,64,128,128,128 filters of size 3X3.  Add a maxpooling after the second layer, the fourth layer and the sixth layer.
- Train the CNN and study the loss function/ accuracy. This could take several long so don't forget to save regularly.
- Add Batch normalization layers and dropout. Does it help to converge?
- Do a PCA analysis and k-means on the layer before the classifier. 
- Implement the data augmentation. Explore the generated images and train the model with data augmentation.
- At the end of the day, you should be able to reach more than 80% of accuracy on the test set.
- Apply the transfer learning for the cifar10 classification (10 epochs). How well is working the transfer learning?

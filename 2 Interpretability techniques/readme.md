This folder contains the slides and a Jupyter notebook with a tutorial on interpretation of deep neural networks with the intuitive example of Class Activation Maps (CAM). [Here](https://arxiv.org/pdf/1512.04150.pdf) you can find the original paper. Code in this tutorial is based on [the code provided by authors of the method](https://github.com/zhoubolei/CAM).


# Tasks for today / Homework (Anna Dawid)

## Numerical tasks:
1. With "copy-paste", create a function which inputs an image URL + id of the model and outputs the CAMs of three classes that have the highest probabilities.

2. Follow the shapes of: 
*   the input image
*   the output of the model
*   the size of the last layer (after GAP)
*   what CAM function exactly does? What is 'weight_softmax[idx].dot(feature_conv.reshape((nc, h*w)))', why then the result is reshaped to (h, w)? What are 'bz, nc, h, w'? Print them out.
*   what cv2.resize does? Why is it needed?

## Discuss:
1. Apply this method to a few images and discuss shortly what one can learn from CAMs and what are their limitations.
2. Apply this method to a few images of the same category (e.g., various dogs, various cats) and again discuss shortly what one can learn from CAMs.
3. Based on classifications described during the lecture, what categories CAM belongs to?
  *   Model-specific or model-agnostic?
  *   Provides local or global explanations?
  *   Is it (a) a surrogate approach? (b) method focused on the model's component analysis? (c) method focused on analysis of the model after data perturbation?
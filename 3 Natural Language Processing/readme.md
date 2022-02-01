# Natural Language Processing
In this block, we are going to divert from our *ML for physics* perspective and have a look at natural language processing (NLP). This field has undergone tremendous progress in recent years. I will try to introduce all the necessary concepts and guide us through the historical development of what is state of the art today: transformer models (honestly: terrible choice in name if you ask me!). If you choose this block for your examination, you will have the choice of three ground-breaking papers introducing `sequence-to-sequence` models, `attention mechanism` and `transformer models`, respectively. After the end of this lecture series, you should be well equipped to understand these papers. Frankly, the maths involved is rather straight-forward, but the concpet of stochastically treating vector-representations of words, processed sequentially *in time*, will be the more challenging part! The challenge is worth is because with understanding NLP, you understand one of the most interesting, advanced and important sub-fields in modern machine learning.

## Homework

### 0. Maths warmup

Consider running the experiment for collecting spam emails every day as discussed in the lecture. Reminder: You are receiving $n=20$ emails every day for a course of $N=1000$ days. With some probability $\Theta$, $x_i$ of the emails on day $i$ are spam. Derive *analytically* the formula
$$
\Theta_\text{opt} = {\sum_i x_i}{nN}
$$
for the optimal parameter $\Theta$.  

*Help:* You need to minimize the negative log-likelihood $\sum_i \log(p_\Theta(x_i))$ with respect to $\Theta$ and you know that this process follows a binomial distribution $p_\Theta(x) = \binom{n}{x} \Theta^x (1-\Theta)^{n-x}$

### 1. Numerical appraoch

Generate some data and perform the same optimization numerically.  

*Help:* See the 0th notebook.

### 2. Use a neural network  

Imagine you didnt know the functional form of the stochastic binomial process at hand. Instead of finding $\Theta$ as in part 1, define and train a (very simple) neural network to reproduce the probability distribution.  

*Help:* A simple fuly-connected network should suffice.

### 3. RNN for name classification

Code a RNN from scratch and perform character-level text classification of the names provided in `/data/names/*.txt`. You may follow `02_name-classification.ipynb`.

### 4. Transformer models 

Work through `03_transformer_tutorial.ipynb` and add a part making word predictions for "Machine Learning for Quantum and Classical physics was ..".
If you are more interested, there is a bigger tutorial with translationfrom German to English on the [pytorch tutorial website](https://pytorch.org/tutorials/beginner/translation_transformer.html).

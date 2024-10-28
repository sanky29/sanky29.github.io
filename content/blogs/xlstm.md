+++
title = 'Xlstm'
date = 2024-10-27T19:39:03+05:30
+++

A couple of weeks ago, my Twitter feed was flooded with discussions about the new xLSTM paper. Curious, I took a quick look at it. Like most papers, it first presents a problem statement, highlights the challenges in solving that problem, and finally details the approach used to address—or not address—these challenges. The xLSTM paper did this well, but it also brought me back to some fundamental questions: How does the original LSTM solve the gradient explosion and vanishing gradient problems?\
\
I decided to take this as an opportunity to revisit LSTMs from first principles, deriving results in simple cases to build an intuitive understanding. I thought it would be helpful to share this journey, and hopefully get some feedback.\
\
Here’s the structure of this blog: 

**Introduction to RNNs:** We’ll start by exploring a simple, one-dimensional RNN and derive the backpropagation updates for its parameters.
Gradient Explosion and Vanishing – Then, we’ll dive into the gradient issues common in RNNs and discuss why they occur. \
**LSTM Architecture:** Next, we’ll break down the LSTM design and see how it mitigates these gradient issues. \
**Brief Overview of xLSTM:** Finally, we’ll touch on the xLSTM model and how it builds on these foundational concepts. 

## RNNs
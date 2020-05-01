# Universal-Image-Classifier-Cpp

---

For the final project, I want to build an application that makes use of artificial intelligence in some manner. 
The primary motivation for this project comes from noticing the extra credit oppurtunity in the Naive Bayes assignment
where students were encouraged to train an artifical neural network to serve as a model for classifying handwritten
digits. My experience in this area comes from building a Machine Learning classifier in C++ for classifying handwritten
digits, so I have the necessary background in parsing a dataset, how to train and test a model, etc.

The goal of this project will be to create an image classifier that will accurately classify everyday objects like
automobiles, vehicles, animals, people etc. The proposed library for building and training the neural network is
the Tensorflow C++ API, a C++ wrapper for the Tensorflow Machine Learning and Deep Learning framework. I plan on using
the CIFAR 10 dataset for the model. Here is a link: https://www.tensorflow.org/install/lang_c; the library contains a
CMake folder.

By the end of the first week, I hope to have the environment set up (Cinder and PyTorch). By the end of the second week,
I hope to have the architecture of the neural network defined and the code for the dataset I/O. By the third week, I
hope to have a working model that can classify an image given by the user. A stretch goal I have would be to expand my
model to work with the CIFAR 100 dataset, which contains 10 subclasses for each of the 10 superclasses provided in CIFAR 10.

---

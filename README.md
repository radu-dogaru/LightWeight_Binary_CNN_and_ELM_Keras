# LightWeight_Binary_CNN_and_ELM_Keras

There notebooks are stored in this repositoy, related to the following paper:
[1] Radu Dogaru and Ioana Dogaru, "BCONV-ELM: Binary Weights Convolutional Neural Network Simulator based on Keras/Tensorflow, for Low Complexity Implementations", Proceedings of the ISEEE 2019 conference, submitted. 

Please cite the above paper if you found this code useful. 

A brief decription of the notebooks (all were tested under the Kaggle platform but may run on any other providing 
a Python environment with TENSORFLOW, KERAS, NUMPY installed): 

1) BCONV-ELM.ipynb  - allows the design of a lightweight CNN with 2 convolutional+pooling layers. 
The optimization of the binary kernels is done while maximizing the accuracy of an extreme learning 
machine (used here for its fast learning). After that, a linear (optionally up to 2 hidden layers may be added) 
perceptron network (for reduced complexity) is trained. The resulting model is well suited for 
hardware orineted implementations (e.g. FPGA, microcontrollers etc.) 

2) Keras-ELM: a convenient implementation of the Extreme Learning Machine including the case with no hidden layer and 
quantization of weights for resource-constrained platforms). This cell is extracted from the above and can be 
used independently on any desired dataset. Since it supports GPU very fast learning (under one minute) is achieved 
for medium sized datasest. It is not recommended for very big data since it requires a lot of RAM on the device. 

3) L-CNN:  the trainable version of the BCONV-ELM: it trains standard Keras/Tensorflow models for 
a lightweight CNN (L-CNN) with up to 3 convolution layers and a linear output perceptron (2 more hidden layers 
could be added but the low complexity implementation is achieved for MLP0). 
Some cells for loading various datasetes are provided



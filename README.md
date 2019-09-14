# Convolutional Neural Network on 2D images, step by step increase of computer vision
  Tensorflow and Keras are used for modeling.

## Process:
First the images are fed and image content is reduced to look at enhanced features for specific details. The convolution layers are added prior to dense filters.
Size of convolution is a 3x3 grid. Convolution is followed by maxpooling layer effectively reducing image by 25%
Training is done on highlighted features obtained after convolution.
The first layer the shape of input data is fed

## Dataset:
The dataset is mnist fashion data.

Reshape: 
takes all the training or test images and puts them into a single list 4D Tensor.

## Normalizing Neural Net:
Treat all values as between 0 and 1, a process called 'normalizing' helps to treat neural net values between 0 and 1, so divide by 255 is used on all training and test images.

Flatten turns the image into 1 dimensional set from square.

## Pooling:
creates a 2x2 array of pixels, and picks the biggest one, thus turning 4 pixels into 1. 

Convolution of Neural Nets:
Add some layers to do convolution before you have the dense layers, and then the information going to the dense layers is more focussed, and possibly more accurate.

## Activation: 
"relu" activation helps drop the negative numbers
"softmax" activation helps pick the biggest

## Loss function:
'sparse_categorical_crossentropy' is used when your target classes are mutually exclusive such as integers e.g 1,2,3 instead of on-hot encoded values which is used for categorical_crossentropy (like [0.4, 0.1, 0.3]).. The LOSS function measures the guessed answers against the known correct answers and measures how well or how badly it did.

## Optimizer:
"adam" is used OPTIMIZER function to make another guess. Based on how the loss function went. Adam optimization algorithm is an extension to stochastic gradient descent. This helps update network weights iterative based in training set.
 “Adam: A Method for Stochastic Optimization“. The name Adam is derived from adaptive moment estimation, where the wieghts are adjusted adaptively. Adam realizes the benefits of both Adaptive Gradient algorith (AdaGrad) and Root Mean Square Propagation (RMSProp). It is efficient, Empirical results demonstrate that Adam works well in practice and compares favorably to other stochastic optimization methods.

### Adam Configuration Parameters
alpha. Also referred to as the learning rate or step size. The proportion that weights are updated (e.g. 0.001). Larger values (e.g. 0.3) results in faster initial learning before the rate is updated. Smaller values (e.g. 1.0E-5) slow learning right down during training
beta1. The exponential decay rate for the first moment estimates (e.g. 0.9).
beta2. The exponential decay rate for the second-moment estimates (e.g. 0.999). This value should be set close to 1.0 on problems with a sparse gradient (e.g. NLP and computer vision problems).
epsilon. Is a very small number to prevent any division by zero in the implementation (e.g. 10E-8).



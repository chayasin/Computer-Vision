# Computer Vision

- Introdunction
- Convolution Neural Network
- Azure

**Outline**

- [Computer Vision](#computer-vision)
  - [Introduction](#introduction)
    - [What computer see?](#what-computer-see)
      - [Pixel](#pixel)
        - [Black an White](#black-an-white)
        - [Color](#color)
  - [Deep Learning](#deep-learning)
    - [Linear Regression](#linear-regression)
      - [Weight](#weight)
      - [Bias](#bias)
      - [Activation function](#activation-function)
    - [Cost Function](#cost-function)
    - [Feed Forward - Back Propagation](#feed-forward---back-propagation)
      - [Feed Forward](#feed-forward)
      - [Back Propagation](#back-propagation)
    - [Vanishing Gradient](#vanishing-gradient)
    - [Overfitting](#overfitting)
      - [Use Regularisation](#use-regularisation)
      - [Use Drop out](#use-drop-out)
    - [Data processing](#data-processing)
  - [Convolution Neural Network (CNN)](#convolution-neural-network-cnn)
    - [Convolution/Kernal/filter](#convolutionkernalfilter)
    - [Pooling](#pooling)
    - [Flatern/fully connected](#flaternfully-connected)
    - [Tranfer Learning](#tranfer-learning)

---

## Introduction

**What is 'Computer Vision'?**

> **Ans** Science of How computer understands *Image* or *VDO*

**Use Cases**

> - Image Classification    : *Is this picture has a cat?*
> - Object detection        : *Where is the cat i nthis picture?*
> - Segmentation            : *Can you outline the cat in this picture?*

-- add images --

**Application**

> Speed detection           : *This is why you get a traffic ticket*
> face detection            : *Many school has this already*
> Tesla self sriving car    : *This is a very good example of computer vision*

### What computer see?

Human can see the whole image and tell what it is. However Computer just see a line if code, such as 1010100010011001100... .

#### Pixel

##### Black an White

Digital image is a combination of pixels. First, consider a black and white picture which is 3 by 3 pixel. each pixel of this picture will be a number between 0 to 255. This number represents the brightness of the pixel, 255 is the brightest color or White and 0 is darkest color or Black.

<center>

|            | 1st row | 2nd row | 3rd row |
|------------|---------|---------|---------|
| 1st column | 0       | 0       | 0       |
| 2nd colomn | 0       | 255     | 0       |
| 3rd column | 0       | 0       | 125     |

</center>

This image is has a white pixel at the center, a grey pixel at the buttom right, and the rest of the image is black.

--add image--

##### Color

Im color image, it use the similar idea. However, instead of using just one number to represent the brightness of a pixel it use 3 numbers to represents the brightness of Red, Green, and Blue of a pixel.

## Deep Learning

Deep learning  has invented many decades ago, however it was not popular because it needs large amount of data to train a model and comsumes huge computational resource.

### Linear Regression

#### Weight

skip

#### Bias

skip

#### Activation function

- Logistic (sigmoid) - continue but slow - threshold \{x<=0.5,x>0.5\}
- ReLU $max(0,x)$ - not continue but fast - threshold \{x=0,x>0\}
- Leaky $max(0.1x,x)$ - has negative value (why??) - threshold \{x<=0,x>0\}

### Cost Function

> Regressinon
>> MSE (square error)
>> RMSE (root of MSE)
>> MAE (absolute error)

> Classification
>> Log-loss (both binary and multiclass cases)

### Feed Forward - Back Propagation

#### Feed Forward

Add random weight to the nodes and inject a sample into the model.

#### Back Propagation

Use the output of the previous step to adjust the weight of the model.

Note that Deep Learning is just a numerical method for solving general problems.

### Vanishing Gradient

In a large ANN one might encounter a problem that the weight of the early layer is hardly adjusted (the weight is vanished).

- use Residuel (see next section)
- use initial weight

Note that: if we set the learning rate too hight, the accuracy might jump back an forth between good and bad value.

### Overfitting

#### Use Regularisation

Just use Ridge or LASSO

#### Use Drop out

drop random nodes of hand picked nodes off the ANN.

### Data processing

Normally we normallise the data to [0,1] before train it. This will solve many problem such as the model put a too large weight on one parameter.

## Convolution Neural Network (CNN)

CNN = Image preprocession + Neural Network

Human will detect small components of picture then combine it to understand the whole picture.

Idea

Input -> Convolution (Feature maping) -> Pooling -> (Flantern ->) Neural network -> Output

### Convolution/Kernal/filter

- Stride เลื่อน kernal ทีละเท่าไหร่
- Padding - add paddle to make same-size output (<-this is not very make sense, however different kernal represent different output)

### Pooling

Reducing the size of the feature (output of the convolution)

- max pooling
- avarage pooling
- random pooling

### Flatern/fully connected

just use every pixels of the output (from pooling) as the input for ANN.

### Tranfer Learning

Use per-trained model and then fine tune new model with new data.

This like borrowing kernel, pooling, or even the NN from other model then retuned some nodes again.

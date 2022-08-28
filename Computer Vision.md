---
title: Compuer Vision
author: Chayasin
header-includes: |
    \usepackage{tikz,pgfplots}
    \usepackage{fancyhdr}
    \pagestyle{fancy}
    \fancyhead[CO,CE]{This is fancy}
    \fancyfoot[CO,CE]{So is this}
    \fancyfoot[LE,RO]{\thepage}
abstract: Computer Vision is a science of how we teach computers to see images an video.
---

# Compuer Vision

- Introdunction
- Convolution Neural Network
- Azure

**Outline**

- [Compuer Vision](#compuer-vision)
  - [Introduction](#introduction)
    - [What computer see?](#what-computer-see)
      - [Pixel](#pixel)

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

Digital image is a combination of pixels. First, consider a black and white picture which is 3 by 3 pixel. each pixel of this picture will be a number between 0 to 255. This number represents the brightness of the pixel, 255 is the brightest color or White and 0 is darkest color or Black.

<center>

|            | 1st row | 2nd row | 3rd row |
|------------|---------|---------|---------|
| 1st column | 0       | 0       | 0       |
| 2nd colomn | 0       | 255     | 0       |
| 3rd column | 0       | 0       | 125     |

</center>

This image is has a white pixel at the center, a grey pixel at the buttom right, and the rest of the image is black.



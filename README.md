# Image_Forgery_Detection
Using CNN's to detect doctored images

# Forgery
Forgery is a white-collar crime that generally refers to the false making or material alteration of a legal instrument with the specific intent to defraud anyone.

### Why use CNN?
During the pre deep learning era of artificial intelligence i.e. before the Image Net challenge of 2012, researchers in image processing used to design hand made features for solving problems of image processing in general and image classification in particular. One such example is the Sobel kernel used for edge detection. The set of image forensic tools used earlier can be grouped into 5 categories namely
Pixel-based techniques that detect statistical anomalies introduced at the pixel level
Format-based techniques that leverage the statistical correlations introduced by a specific lossy compression scheme
Camera-based techniques that exploit artifacts introduced by the camera lens, sensor, or on-chip postprocessing
Physics-based techniques that explicitly model and detect anomalies in the three-dimensional interaction between physical objects, light, and the camera
Geometry-based techniques that make measurements of objects in the world and their positions relative to the camera
Courtesy: https://ieeexplore.ieee.org/abstract/document/4806202
Almost all these techniques exploit the content-based features of an image i.e. the visual information present in the image. CNN's are inspired by visual cortex. Technically, these networks are designed to extract features meaningful for classification i.e. the ones which minimize the loss function. The network parameters — kernel weights are learned by Gradient Descent so as to generate the most discriminating features from images fed to the network. These features are then fed to a fully connected layer that performs the final task of classification.
After looking at a few forged images, it was evident that locating the forged areas by human visual cortex is possible. CNN is thus the perfect deep learning model for this job. If a human visual cortex can detect it, certainly there is more power in a network which would be specifically designed for that task.

### Dataset
Before going into the dataset overview, the terminology used will be made clear
Fake image: An image that has been manipulated/doctored using the two most common manipulation operations namely: copy/pasting and image splicing.
Pristine image: An image that has not been manipulated except for the resizing needed to bring all images to a standard size as per competition rules.
Image splicing: The splicing operations can combine images of people, adding doors to buildings, adding trees and cars to parking lots etc. The spliced images can also contain resulting parts from copy/pasting operations. The image receiving a spliced part is called a “host” image. The parts being spliced together with the host image are referred to as “aliens”.
The entire dataset for both the first and second phase can be found here. For this project, we will be using only the train set. It contains 2 directories — one containing fake images and their corresponding masks and the other containing pristine images. Mask of a fake image is a black and white (not grayscale) image describing the spliced area of the fake image. The black pixels in the mask represent the area where manipulation was performed in the source image to get the forged image, specifically it represents the spliced region.

The dataset consists of 1050 pristine and 450 fake images. Color images are usually 3 channel images one channel for each red, green and blue colors, however sometimes the fourth channel for yellow may be present. Images in our dataset are a mix of 1, 3 and 4 channel images. After looking at a couple of 1 channel images i.e. grayscale images, it was evident that these images
were very few in number
were streams of black or blue color
The challenge setters added these images on purpose as they wanted solutions robust to such noise. Although some of the blue images can be images of a clear sky. Hence some of them were included while others discarded as noise. Coming to four channel images — they too didn’t have any useful information. They were simply grids of pixels filled with 0 values. Thus our pristine dataset after cleaning contained about 1025 RGB images.
Fake images are a mix of 3 and 4 channel images, however, none of them are noisy. Corresponding masks are a mix of 1, 3 and 4 channel images. The feature extraction we will be using requires information from only one channel of the masks. Thus our fake image corpus has 450 fakes. Next up we did a train-test split to keep 20% of 1475 images for final testing.

## About me

**Piyush Pathak**

[**PORTFOLIO**](https://anirudhrapathak3.wixsite.com/piyush)

[**GITHUB**](https://github.com/piyushpathak03)

[**BLOG**](https://medium.com/@piyushpathak03)


# 📫 Follw me: 

[![Linkedin Badge](https://img.shields.io/badge/-PiyushPathak-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/piyushpathak03/)](https://www.linkedin.com/in/piyushpathak03/)

<p  align="right"><img height="100" src = "https://media.giphy.com/media/l3URDstnIjBNY7rwLB/giphy.gif"></p>

# image-processing

## Python libraries used:
Numpy
PIL
OpenCV
urllib
Matplotlib
## Basic Image - Processing Techniques:

#### Point operators/ Point Porcesses:
Basic Image Transform wherein, the output of a pixel in an image depends only on the corresponding input pixel.
output g(x) = h(f(x)) where x is D-Dimensionsal (Usually 2) and x = (i, j) where i and j are the location of the pixels.

Two  commonly used point operations: Multiplication and Addition with a constant. 
                                g(x) = a * f(x) + b . 
a and b are called as gain and bias parameters and sometimes said to control **CONTRAST** and **BRIGHTNESS** respectively. 

Linear blend operator: 
                                g(x) = (1 − α)f0(x) + αf1(x)
By varying α between 0 to 1, this equation can be used to perform cross dissolve between 2 images or videos. 

**Non - linear transform**: 
**Gamma correction or Power-Law transform**
Gamma correction describes the  relationship between pixel's actual value and its luminance. our eyes does not percieve light like cameras do. The light captured in camera is directly proportional to the number of photons that is hit on the camera's sensor. But our eyes percieve light differently. The graph below describes how the light is percieved in camera and in our eyes. 

![alt text](https://cdn.cambridgeincolour.com/images/tutorials/gamma_chart1e.png)

Formula for gamma correction:
g(x) = [f(x)] ^ 1/γ , where γ = 2.2 for most digital cameras. 

On applying gamma correction, it helps to translate the light sensitivity between the camera and the human eye. All the images, when saved are gamma encoded, so that the human eye can percieve the light properly. 
    * The linear encoded images has very less tones/ gradients for describing the dark tones while the gamma encoded images has a sufficient levels of gradients for describing the dark tones

![alt text](https://cdn.cambridgeincolour.com/images/tutorials/gamma_gradient2b.png)

![alt text](https://cdn.cambridgeincolour.com/images/tutorials/gamma_gradient1b.png)


#### Composting and Matting:
Removing an object from a scene in an image is called as **COMPOSTING**. Placing the removed object in some other image without any artifacts is known as **MATTING**. The intermediate object is known as **Alpha matted color Image**. In addition to 3 channels it will have a 4th channel - Alpha channel. If the object is fully opaque, alpha = 1 or if it is transparent(opposite of opaque), then alpha = 0. The pasting of this image over another image(background) is described by:
                                C = (1 − α)B + αF
where, B is the background and F is the foreground.

#### Histogram Equalization:

##### Histogram:
Histogram is a graphical representation of Image's pixel intensity values. It can be interpreted as the data structure that contains the frequency of the pixel intensity levels in an Image. 

![alt text](https://miro.medium.com/max/640/1*c1eCgfFWEPDhE6-ojPFk4g.webp)

RGB images has 3 histograms, one for each channel. 

##### What is Histogram equalization? 

Histogram Equalization is a technique used to adjust the contrast of an Image using its own histogram. It will spread out most frequent pixel intensity. By this, histogram equalization can increase the contrast in the image in areas where there are less contrast. Mathematically, it can be said as integrating the actual distribution (original histogram) to obtain the cummulative distribution. 

![alt text](https://miro.medium.com/max/640/1*PWPxuPXr1CrRgJGo8vMH_g.webp)


If the histogram of an image is dense in a Brighter region, it means that the image is of low contrast. Histogram equalization works on mapping the input pixels in the brighter region to the output pixels in all the region.


##### Contrast - Locally adaptive Histogram Equalization:

An Adaptive histogram equalization method. In general histogram equalization, the histogram is computed for all the pixels in the image. This, while increasing the contrast, increases the contrast of the noise as well. This might create undesirable artifacts. To avoid this, Adaptive histogram equalization is performed. In this method, the image is divided in blocks and histogram is computed at each block in the image. This can significantly reduce the problem faced in Histogram equalization. The adaptive histogram equalization method in OpenCV has a parameter clip, in which the contrast value can be limited. Typically, the contrast limiting must fall in the range 2-5. 


### References: 
1. Book : computer-vision-algorithms-and-applicatons-2nd-edition, by Richard Szeliski
2. https://www.cambridgeincolour.com/tutorials/gamma-correction.htm
3. https://medium.com/@kyawsawhtoon/a-tutorial-to-histogram-equalization-497600f270e2
4. https://medium.com/mlearning-ai/how-to-plot-color-channels-histogram-of-an-image-in-python-using-opencv-40022032e127
5. https://docs.opencv.org/4.x/d5/daf/tutorial_py_histogram_equalization.html




# DIGITAL IMAGE BASICS

### Bit Depth 
Bit depth is determined by the number of bits used to define each pixel. 1 bit can represent two tones, typically black and white. A 2-bit image has four possible combinations: 00, 01, 10, 11, which represent black, dark gray, light gray, and white. An 8-bit image has 256 different tones that can be assigned to each pixel. The image formats such as jpg has 8 bit. Professional cameras capture RAW images with 16 bit. Actual HDR images must have 32 bit depth but the HDR Television screens display 10 bit depth  images. 

![alt text](https://2.bp.blogspot.com/-NQPXItfa_Og/VJ_5VBeHv3I/AAAAAAAAAgA/Ct9Ae_UW6E0/s1600/bitdepths_chart_med.jpg)

### Image 
Digital Images are made up of pixels, and based on the depth of the pixels, Images can be binary Image, Grayscale Image and Coloured Image (combination of primary colours RGB )
    * A **Binary Image** has a pixel value as either 0 or 255. It is a 1- bit Image with a single channel. The bit value is either 0 or 1
    * A **Grayscale image** or gray level Image is one in which, the only colours are shades of gray. Grayscale Images are 8-bit images with single channel in which the value of the pixel will be in the range (0, 255). Gray colour is one in which red, green and blue components have same values in RGB colour space. 

![alt text](image.png)
    * Unlike grayscale Images, **RGB images** are 3 channelled images. Each pixel is made up of 3 channels with each channel representing a colour. Mathematically,  it is a 3 dimensional array, each dimension corresponding to R, G and B values respectively. The regions containing red colour in the original image are lighter in the red channel image. This means that, the regions which contribute more to the red colour of the original image are lighter in the grayscale image of the red channel. The regions which contribute less or do not contribute are dark. This applies for all the three channels.

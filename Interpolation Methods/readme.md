## Sampling, Aliasing, Quantization
#### Sampling:
Sampling is converting the analog signals to digital signal. Once image is captures, the number od samples define the number of pixels in an Image. Higher the samples, higher is its resolution. 

#### Quantization:
Quantization is the process of assigning values to each sample based on their amplitude. Assigning pixel values to each pixel is Quantization. The total number of values we can assign with respect to the amplitude is known as Quantization level. In an Image (8-bit), the quantization level is 256. 

|Sampling|Quantization|
|-------------------------|
|Gives number of Pixels in an Image|Gives the value of each pixel in an Imag|
|It digitalizes analog signal's x axis|It digitalizes the analog signals y - axis|
|Sampling is carried out before Quantization|Quantization is carried out after sampling|

a frame grabber or digitizer is used to sample the analog signal.

After sampling an Image, if the data points are resampled at a different sampling rates, this process is known as Re-sampling. if a picture has nx by ny values and this image is resampled to s * nx by s * ny pixels, 
if s>1, it is called as **upsampling** or **Interpolation**
if s<1, it is called as **downsampling** or **Decimation**

This can sometimes introduce undesirable artifacts in the image. This is known as **aliasing**

*Bandlimited signal* is the one with the highest frequency. The highest frequency is the bandwidth. 
According to the **sampling theorem**, The minimum sampling rate required to reconstruct a signal must be atleast twice the  highest frequency. If resampling does not meet the conditions of the sampling theorem, aliasing occurs.


#### Interpolation
Interpolation is about estimating the values of pixels at unknown points on considering the known data points. Cameras can perform both an optical and a digital zoom. A camera performs an optical zoom by moving the zoom lens so that it increases the magnification of light. However, a digital zoom degrades quality by simply interpolating the image. Even though the photo with digital zoom contains the same number of pixels, the detail is clearly far less than with optical zoom.  

##### Interpolation methods in OpenCV
1. Nearest Neighbour Interpolation: It just resamples the pixel values that is already present in the matrix.
    steps:
    ![alt text](https://3.bp.blogspot.com/-pSLTKOOXJQ0/WgLYhI4PhoI/AAAAAAAAB0I/0bytdJGLbHc_-r5sDH1aEA8G8vhdqx6iACEwYBhgL/s1600/Nearest2.png)
    
2. Bilinear Interpolation: Linear interpolation is for 1D data and bilinear Interpolation is for 2d data. 
    steps for calculation is found in https://theailearner.com/2018/12/29/image-processing-bilinear-interpolation/

3. Bicubic Interpolation: Similar to Bilinear interpolation. Bilinear interpolation considers surrounding 
    4 pixel data to find the value of a pixel.But Bicubic interpolation considers 16 surrounding pixels. 
    Visual insights at https://www.cambridgeincolour.com/tutorials/image-interpolation.htm

4. Lanczos interpolation: This method considers over 8x8 neighborhood,i.e., 64 surrounding pixels. 

#### References:
1. https://sisu.ut.ee/imageprocessing/book/3
2. https://www.imageeprocessing.com/2017/11/nearest-neighbor-interpolation.html
3. https://theailearner.com/2018/12/29/image-processing-bilinear-interpolation/
4. https://www.cambridgeincolour.com/tutorials/image-interpolation.htm

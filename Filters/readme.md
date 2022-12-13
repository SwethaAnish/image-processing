### Linear and Non Linear filters
#### Python Packages used:
    1.OpenCV
    2.Numpy

#### Key take-aways:
    1. Point operations modify each pixel without affecting the  size, geopetry, structure of Image. New pixel value depends upon the previous pixel value.

    2. Filters create a new pixel by considering the values of more than one pixel.

    3. During Convolution, Instead of using k * k kernel, using 2(1- vertical, 1 horizontal) 1*K kernels can reduce computational cost. Eg: for 5*5 Kernel --> 25 Multiplications and 24 additions. 2 5*1 kernel --> 5 + 5 = 10 multiplications, 4+4 additions. This 1D filters are known as Seperable filters.

    4. In Linear filter, Simple filter: Box filter (Moving average filter). This average the value in the k x k window. Kernel has all ones with a scaling factor i.e., 1/k (k * k filter)

    5. Gaussian filter has kernel which has the shape of Gaussian distribution. The values of the kernel depends upon the standard deviation. Higher the standard deviation, higher the smoothening effect.The standard deviation must be proportional to the kernel size for better smoothening effect

    6. Non - linear filter perform better than linear filters. Eg: Guassian filter smoothens noise pixel instead of removing the noise pixel

    7. Median Blurring: In median blurring, the median is taken for all the pixels under the kernel area and the central area is replaced with the median value. Good at removing salt-pepper noise. 

    8. Bilateral filter is good at noise removal while keeping edges sharp. It uses the Guassian filter. In gaussian blurring, edges are not considered. The filter is applied throughout the image. But in Bilateral filter, the pixel intensity difference is computed. the filter is applied only if the pixel intensity difference is minimal. Thus it preserves the edges. Computational cost is high


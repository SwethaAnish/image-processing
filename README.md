# image-processing

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








### References: 
1. 
2. https://www.cambridgeincolour.com/tutorials/gamma-correction.htm




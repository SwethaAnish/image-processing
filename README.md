## image-processing

### Basic Image - Processing Techniques:

#### Point operators/ Point Porcesses:
Basic Image Transform wherein, the output of a pixel in an image depends only on the corresponding input pixel.
output g(x) = h(f(x)) where x is D-Dimensionsal (Usually 2) and x = (i, j) where i and j are the location of the pixels.

Two  commonly used point operations: Multiplication and Addition with a constant. g(x) = a * f(x) + b . a and b are called as gain and bias parameters and sometimes said to control **CONTRAST** and **BRIGHTNESS** respectively. 

Linear blend operator: 
g(x) = (1 − α)f0(x) + αf1(x)
By varying α between 0 to 1, this equation can be used to perform cross dissolve between 2 images or videos. 

Non - linear transform: Gamma correction
g(x) = [f(x)] ^ 1/γ , where γ = 2.2 for most digital cameras.

#### Composting and Matting:
Removing an object from a scene in an image is called as **COMPOSTING**. Placing the removed object in some other image without any artifacts is known as **MATTING**. The intermediate object is known as **Alpha matted color Image**. In addition to 3 channels it will have a 4th channel - Alpha channel. If the object is fully opaque, alpha = 1 or if it is transparent(opposite of opaque), then alpha = 0. The pasting of this image over another image(background) is described by:
                                C = (1 − α)B + αF
where, B is the background and F is the foreground.




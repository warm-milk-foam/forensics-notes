# Chapter9: Steganography (Specific to images) #      
Steganography, as wikipedia defines it, is the concealment of information inside  an image  
So, this section is aimed at   
## LSB ##
As you know, data is stored in bits, such as `01110 0100`   
This technique involves changing the Least Significant Bit, which is the rightmost bit of a byte  so in the earlier example, the rightmost bit is `0`  
For this, lets take a look at this website:  https://incoherency.co.uk/image-steganography/#  
So, for example, lets say I wanted to hide an image of a cat in an image of a tree:  
![alt text](../images/image-35.png)  
As you can see, the cat image is hidden in the cover image, and you cannot notice it at all even if i told you.  
That is because the data of the cat image is hidden in the LSB of the tree image, which contributes very little to the RGB of the pixels in the overall image    
Honestly, this is not the full story of how it works, but this medium article explains it in more depth: https://medium.com/@renantkn/lsb-steganography-hiding-a-message-in-the-pixels-of-an-image-4722a8567046  

However, as you hide the data in more significant bits (closer to the left of the bit 'chain'), the RGB values are changed more drastically, leading you to see the image clearer:  
![alt text](../images/image-36.png)    

## Stegsolve ##

## pngcheck ##

## Colour and bit planes ##


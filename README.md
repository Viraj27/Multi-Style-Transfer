# Neural Style Transfer - what it's all about

Neural Style Transfer is a very neat and catchy technique to generate novel artistic images by transferring the styles of one or more images on a content image. This technique was introduced by [Gatys et al.](https://arxiv.org/abs/1508.06576) and since has been further enhanced and improved upon via different optimization algorithms, regularization techniques and image processing variations. 
 

## Single Style Transfer 

Single style transfer is the technique of transferring the style aspects of one image on a content image to generate an artistic style transferred content image. This is the fundamental technique for style transfer which has been implemented as a tutorial in the [official PyTorch GitHub repository](https://github.com/pytorch/tutorials/blob/master/advanced_source/neural_style_tutorial.py) with some amazing explanation of the flow [right here with a note on optimization by Mr Gatys himself] (https://pytorch.org/tutorials/advanced/neural_style_tutorial.html)

I have used that notebook as reference and cleaned up the order of execution of cells by creating all classes and method definitions at the top and calling them all at once by passing them as parameters to the algorithm. Here are some instances of how a single style transfer works-
<p float = "left">
<img src="images/Mona_Lisa.jpg" width="256">
<img src="images/Scream.png" width="256">
<img src="Results/ML_Scream.jpg" width="256">
</p>
<p float = "left">
<img src="images/Last_Supper.jpg" width="256">
<img src="images/picasso_512x512.jpg" width="256">
<img src="Results/LS_SN.jpg" width="256">
</p>
<p float = "left">
<img src="images/French_Revolution.jpg" width="256">
<img src="images/starry_night.jpg" width="256">
<img src="Results/FR + StN.jpg" width="256">
</p>


## Multi Style Transfer

Multi style transfer os the technique of transferring the styles of two or more images on a content image, blend them with the content image to generate different artistic styles. In this repository, I have extended the Style Transfer with 1 image and added the ability to process 2 style images, easily scalable to multiple images. I've used PyTorch with complete implementation in the notebook itself.

**Note : The weights and the number of iterations are hyperparameters and hence, require tuning respective to the content and style images you provide. Some of the samples below worked with 300 iterations and some of them had to be run for 600-800 iterations. Similiarly, the content and style weights of the images had to be finetuned to get optimal results. Please do not consider the hyperparameters in the notebook as the "correct" values, feel free to play around with them and see what results they get you!**

Some instances of Multi-Style transfer at play - 
<p float = "left">
<img src="images/dancing.jpg" width="256">
<img src="images/Scream.png" width="256">
<img src="images/picasso_512x512.jpg" width="256">
</p>
<img src="Results/Dancing+Scream+Picasso.jpg" width="768" height="512">

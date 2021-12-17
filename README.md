## Objective: To create new images using StyleGAN2 architecture  

## Training the model 
I initially wanted to train the model from scratch, however, I faced some obstacles such as: many data/"images" required (to the tune of tens of thousands) and a long training time required (think a few days) with the premise that Google Colab's GPU would continue to work (which did not). 

Hence, I decided to adopt [StyleGAN2 x DiffAugment](https://github.com/mit-han-lab/data-efficient-gans/tree/master/DiffAugment-stylegan2)  which is an adaptation of StyleGAN2. 

[Developed by researchers at MIT, StyleGAN2 x DiffAugment improves the data efficiency of GANs by imposing various types of differntiable augmentations on both real and fake samples. This effectively stabilises training, and leads to better convergence.](https://hanlab.mit.edu/projects/data-efficient-gans/) 

The upside of using StyleGAN2 x DiffAugment is that it allows for limited images (100 images) for the training of the model. With that, I leveraged on StyleGAN2 x DiffAugment model to train images that was scraped from Instagram. 

## Results 
[A presentation of this StyleGAN2 project journey I embarked on](https://docs.google.com/presentation/d/e/2PACX-1vQwwAgrjzIH5O_MjHq28tdB2Hz2zTdd1NMEziP7hc-25hrO2Lf3742BKWJExebL81aGLjfRyM4kk-lJ/pub?start=true&loop=true&delayms=3000)

After approximately 6 hours of training and running 32 minibatches, I managed to generate new images with a FID score of 200. FID score is a score used to measure the quality of images with a lower score indicating better quality images. 

![Results](results.gif)

## Link to Google Colab notebook 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1JUho62_gwqbHdlCUlGbFh-7tBxMiGC18#scrollTo=HLYCnN36W73k]



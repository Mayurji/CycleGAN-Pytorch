# CycleGAN Using Pytorch and Keras

**CycleGAN Overview**

CycleGAN is a generative model, which transfers the style aspects of an image to another image. Before CycleGAN networks were introduced, a pre-requisite was to train the generative model is that the each image in the training set to exist in both the source and target domain. While it is possible to manufacture this kind of dataset for some style problem settings (e.g., black and white to color photos, maps to satellite images), for others it is impossible. For example, we do not have original photographs of the pond where Monet painted his Water Lilies series, nor do we have a Picasso painting of the Empire State Building. It would also take enormous effort to arrange photos of horses and zebras standing in identical positions.

**Idea behind the architecture**

CycleGAN contains four network, two generators and two discriminators. The first generator, G_AB, converts images from domain A into domain B. The second generator, G_BA, converts images from domain B into domain A.

As we do not have paired images on which to train our generators, we also need to train two discriminators that will determine if the images produced by the generators are convincing. The first discriminator, d_A, is trained to be able to identify the difference between real images from domain A and fake images that have been produced by generator G_BA. Conversely, discriminator d_B is trained to be able to identify the difference between real images from domain B and fake images that have been produced by generator G_AB.

CycleGAN generators take one of two forms: U-Net or ResNet (residual network).

**concepts**

    Upsampling
    Concatenate Layers
    Instance Normalization

[**CycleGAN Paper**](https://arxiv.org/abs/1703.10593)

**Dataset**
     
     Horse2Zebra
     Monet2Photo
 
**Result**

![CycleGAN.png](CycleGAN.png)




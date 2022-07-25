# Super Resolution Network

## Dataset

The dataset used for this problem is a subset of [this](https://www.kaggle.com/datasets/jessicali9530/celeba-dataset) dataset available on kaggle.

## SR-GAN

In SR-GAN, we use Generated Adversarial Network to convert a lower resolution image into higher one. <br>
SR-GAN works by creating two sub-neural networks, Generator and Discriminator which works against each other to produce desired outcomes.
<br><br>
Generator networks takes lower resolution images as input and then applies features learned from VGG-19 pre-trained network to fool the discriminator network.
<br>
Discriminator networks on the other hand, tries to avoid getting fooled by Generated images while training itself on higher resolution and generated images.
<br><br>
Our goal is to minimize the generator loss and maximize the discriminator loss.
<br><br>
In ideal situation, probability of discriminator model to guess right image should be 0.5, which implies that the model is essentially flipping a coin to find the correct images.
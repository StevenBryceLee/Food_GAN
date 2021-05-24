# Food_GAN
Repository containing notebook adapted from PyTorch GAN tutorial to try to generate food images
This repository uses Weights and Biases to perform a hyperparameter sweep over different model training parameters
The Generator attempts to output 3x64x64 images which fool the Discriminator into predicting that the generator output came from the training distribution
Wider hyperparameter searches might make the tool work better. Num_epochs can also be increased to get clearer and more realistic images
Check your wandb dashboard to make sure the generator's loss function is going down. 

I found while training that SGD was a really bad optimizer and usually resulted in perfect descrimination with the generator being unable to learn how to make good images.
Adam worked better.

The size of the latent vector usually was better when bigger as well. The default from the paper was size 100, with my test in size 50 resulting in extremely low learning rates

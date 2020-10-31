Convolutional Neural Networks and Image Classification
In this project, you will apply convolutional neural networks to classify images in a 
dataset of your choice.


Using CIFAR-100 Dataset:
Defining the problem and assembling a dataset
This dataset is just like the CIFAR-10, except it has 100 classes containing 600 images each. 
There are 500 training images and 100 testing images per class. The 100 classes in the CIFAR-100 
are grouped into 20 superclasses. Each image comes with a "fine" label (the class to which 
it belongs) and a "coarse" label (the superclass to which it belongs). The problem is that we 
want to identify and classify images into 100 classes that are subclasses of these coarse 
identifications:

aquatic mammals
fish
flowers
food containers
fruit and vegetables
household electrical devices
household furniture
insects
large carnivores
large man-made outdoor things
large natural outdoor scenes
large omnivores and herbivores
medium-sized mammals fox, porcupine, possum, raccoon, skunk
non-insect invertebrates
people
reptiles
small mammals
trees
vehicles 1
vehicles 2
Choosing a measure of success
Because there are an equal number of eah type of class, this is a class-balanced problem and 
accuracy (or ROCAUC) would suffice. For this problem, we will stick with accuracy.

Deciding on an evaluation protocol
We have plenty of data. 50,000 training samples can be reduced to 40,000 training samples 
and 10,000 validation samples. It will be best to use this hold-out validation set due to the 
fact that we have plenty of samples. In addition, the samples are spread out pretty evenly through 
the training and validation dataset. In the validation set, no class is seen less than 77 times and 
no more than 117 times. This split is perfectly acceptable for validation data.


THE MODELS:

There will be four models produced by these notebooks. The first is a simple model that serves as a 
baseline. The second is one I built that purposefully overfits the training data. The third is one
that was intended to have the best customization of the hyperparameters. The last one adds to the VGG16 
model pretrained on ImageNet dataset with a customized dense layers. 



TO RUN:
Best to use GPUs.

Run in this sequence. 
TrainingModels.ipynb
ThirdModel.ipynb
TestModels.ipynb
VisualizeModel.ipynb

Running these in this order will ensure that you get the .keras files and the .npy files. But, they are attached 
to this repo if needed.
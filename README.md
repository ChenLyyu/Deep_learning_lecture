# Deep learning: an historical perspective
## Description
This repository contains the sildes of the seminar “Deep learning: an historical perspective”,  given October 31 2pm-3pm at SJTU co-organized by SJTU School of Mathematical Sciences and SJTU-ParisTech Elite Institute of Technology
([Intro_Deep_SJTU_2018.pdf](https://github.com/StephaneCanu/Deep_learning_lecture/blob/master/Intro_Deep_SJTU_2018.pdf), 21.5 MB)  

It also contains the slides of the introduction to deep learning 3h lecture given at the ECAS-ENBIS 1-Day Summer School, on the 6 of september, 2018
([00_Main_Deep_2018.pdf](https://github.com/StephaneCanu/Deep_learning_lecture/blob/master/00_Main_Deep_2018.pdf))  

It comes together with practical exercices on deep learning with the solution in python based on keras and some jupyter notebooks within the so called directory.

## Deep learning practical session
### Requirements

Keras should be available on your python environment.  
You can install this library in the local environment using pip 
(`pip3 install keras`)

TP_Deep_2_webcam.py require opencv-python  
You can also install this library in the local environment using pip 
(`pip install opencv-python`)

### TP_Deep_1_MNIST.py (based on MNIST)
The purpose of this code is to help to take our first step in deep learning by reproducing  the results given on the [MNIST site](http://yann.lecun.com/exdb/mnist/). In less than 3 minutes, you will build and train a fully connected neural network (NN) 
performing less than 1.5% error on the [MNIST database](http://yann.lecun.com/exdb/mnist/),
and then, in less than 15 minutes, a convolutional neural network
performing less than 1% error.    
It comes together with the jupyter notebook TP_Deep_1_MNIST.ipynb. 
The other jupyter notebook TP_Deep_1_MNIST_Optim.ipynb, proposes a comparizon of different optimizers on the [MNIST fashion dataset](https://github.com/zalandoresearch/fashion-mnist).

### TP_Deep_2_webcam.py 
require a web cam, and opencv-python `pip install opencv-python`

### TP_Deep_3_fine_tuning.py
It works with the directories contained in these zip files
   - train_cheese.zip
   - test_cheese.zip

to make it run you may:  
 - dowload the TP_Deep_3_fine_tuning.py file to some directory and move to this directory with python (e.g. `cd ../Deep_learning_lecture`)  
 - define the class MonArg as follows
```
class MonArg(object):
   def __init__(self, train, val):
        self.train_dir = train
        self.val_dir = val
        self.nb_epoch = NB_EPOCHS
        self.batch_size = BAT_SIZE
        self.output_model_file = "inceptionv3-ft.model"
        self.plot = "store_true"
```
- define some constants
```
IM_WIDTH, IM_HEIGHT = 299, 299 
NB_EPOCHS = 25
BAT_SIZE = 32
FC_SIZE = 1024
NB_IV3_LAYERS_TO_FREEZE = 172
```
- import the TP_Deep_3_fine_tuning.py file and run it     
```
import TP_Deep_3_fine_tuning
TP_Deep_3_fine_tuning.train(MonArg("train_cheese","test_cheese"))
```
## To go further

- [A 'Brief' History of Neural Nets and Deep Learning, December 24, 2015 by Andrey Kurenkov](http://www.andreykurenkov.com/writing/ai/a-brief-history-of-neural-nets-and-deep-learning/)
- [Deep Learning 101 - Part 1: History and Background, February 23, 2017 by Andrew L. Beam](http://beamandrew.github.io/deeplearning/2017/02/23/deep_learning_101_part1.html)
- [A History of Deep Learning, May 30, 2018 by Andrew Fogg](https://www.import.io/post/history-of-deep-learning/)
- [Deep Learning in Neural Networks: An Overview, 2015 by Jürgen Schmidhuber](http://people.idsia.ch/~juergen/deep-learning-overview.html)
- [Timeline of machine learning on wikipedia](https://en.wikipedia.org/wiki/Timeline_of_machine_learning)

<!--- https://cloud.withgoogle.com/build/data-analytics/explore-history-machine-learning/ --->

# Scene_classify
Scene_classify is a deep CNN classification project that presents the implementation of Inception_-ResNet_v2 model http://download.tensorflow.org/models/resnet_v1_152_2016_08_28.tar.gz as a feature extractor in classifying scene images with concentration to the visualisation of the feature vectors that are instrumental in both spatial and local recognition. We use the pretrained Inception_ResNet_v2 checkpoint that was trained on ImageNet dataset.

# Libraries and Dataset
The CNN was built using Tensorflow slim and the classification was performed on 6000 images from 15 categories of places365 dataset. The task was performed against three classes obtained from categorizing the 15 categories into three categories; a custom word-map of (i) Conveyor, (ii) Indoor and (iii) outdoor.
The training process is simplify for the sake of this project:
One can simply retrain or implement the network with a new testing data:

## How to train the model (This is for evaluation purpose)

We assume the no or basic idea of Neural Network hence the implementation interface is built for off the shelf users.
All what is required is the basic parameters which includes:

--dataset_dir: A dataset dir where the tfrecord files are stored.
--log_dir: A log directory where the training graph is stored.

--evaluation_dir: A directory where the evaluation steps will be saved because the model performs the training and evaluation under supervsion.

--action: The predefined operation to perform e.g 
        train(dataset_dir, log_dir, tfrecord_filename)
        evaluation(dataset_dir, log_dir, evaluation_dir, tfrecord_filename),
        visualise(dataset_dir, log_dir, tfrecord_filename, convlayer) and 
        create_dataset(dataset_dir, tfrecord_filename)')

##Output filename for the naming the TFRecord file

tfrecord_filename: The output filename that holds the TFRecord file

##The Convolutional layer to visualise

convlayer: The convolutional layer to visualise When calling Visualise

##Training or evaluation
Having set the parametres all that is required is to run:

scene_classify.py -- --action= 'action' --*
then the corresponding parameters required by each action *


##Recall Our goal is to implement a pre-trained neural network that is trained on Imagenet for Scene Classification.

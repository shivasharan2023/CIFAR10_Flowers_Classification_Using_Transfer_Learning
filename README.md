# CIFAR10_Flowers_Classification_Using_Transfer_Learning

CIFAR10 flower classification

Dataset folders structure is as fallows
Flowers
|___Daisy
|___Dandelion
|___rose
|___Sunflower
|___Tulip

The code will create the train & test folders with classes as subfolders under it

Resnet50 architecture is used,
Model 1: 
all layers except last classification layer freezed

Model 2:
First 140 layers freezed


Keras data generators are used to create the batches of data for training
train_data_gen = ImageDataGenerator()
train_generator = train_data_gen.flow_from_directory(dir_name, image_size)
model.fit_generator()

Result : Got better accuracy on model 2
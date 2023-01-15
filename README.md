# Image Classification using Deep learning models using CUB-200-2011 dataset. 

## Description:
This project uses deep laerning models to classify images using "Caltech-UCSD Birds-200-2011" dataset which contain about 200 classes, This is a figure to the dataset.
!['CUB-200-2011 dataset'](Picture/CUB-200-2011.jpeg)
,then splitting the data into 70% train , 30% test.
## Conclosion:
- I implement a fully connected neural network (multi-layer perceptron) and the accuracy was low when using the 'relu' activation function and The 'sgd' optimizer in the model, and after converting the activation function to 'Leaky Relu', the optimizer to 'adam' with image size= (32 x 32),the accuracy has been increased.it became 38%. And from the graph loss, the training decreases and validation increases , and in the graph accuracy:the training increases and validation changes alittle so, there are overfitting espeicially,it will be shown more if i increased the number of epochs.

- This project adapt the ResNet-101 network for the current task using tranfer learning and fine-tuning.
#### In Step one:
I used the base model Resnet with (32x32) image size.It includes some parameters like Include_top = false which means that i'm not interested in the last layer of the model,weights="imagenet" means to have the pre-trained weights for the imagenet dataset. I freezed the layers by using(layer.trainable = False) which moves all the layer's weights from trainable to non-trainable.and trained the model. I tried to use activation function"leaky relu"but it gave lower accuracy than "relu",so i used 'relu'.
the overall loss decreases, the overall accuracy increases so,on my point of view,increasing layers or neurons may avoid underfitting and also increasing the number of the epochs can make the model learn more.
#### In step two:
After unfreezing the last two layers,The training loss remains constant ,the validation loss increased,then decreased and then remained a constant and the overall accuracy increases,so the model after unfreezing two layers is better than the model with freezing all layers as there are more trainable weights and .but the dataset in general is very bad so,the overall results of the models are low .




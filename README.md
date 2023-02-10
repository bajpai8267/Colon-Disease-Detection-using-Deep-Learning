# Colon-Disease-Detection-using-Deep-Learning
THE FOLLOWING STEPS ARE INVOLVED IN THE ENTIRE PROCESS OF IMAGE CLASSIFICATION
1.IMPORTING LIBRARIES - Importing essential libraries tensorflow is a deep learning framework suitable for applications involving neural networks. Using tensorflow we can build,train,evaluate and predict our neural network.

2.IMAGE PROCESSING - The training, testing and validation datasets are taken from the given dataset. The imagedatagenerator is used to implement data augmentation. We can process the image as we want and create batches of image data. The images in digital world have pixels whose intensities range from 0 to 255 where black being 0 and white being 255.The rescaling of 1./255 allows it to convert to decimals values ranging from 0 to 1. The flow_from_directory allow us to use the images availabe in the google colab files section. The dataset contains images of variable size. hence it is essential to reshape them to (224,224). (the input dimensions for pretrained model). The batch size is an important parameter which can affect the training time and accuracy. Less batch size increases accuracy and training time and vice versa. The batch size is taken as powers of two.

3.MODEL CREATION - We are using the pretrained cnn meaning that the cnn is already trained on the imagenet dataset and has the weights stored in it. We are going to customise the model by adding additional layers of our choice(remember more layers can increase parameters leading to overfitting). We are using the MobileNetV2 model for this application. This model was developed by google in 2017 and is known for its light memory. This model is ideal for devices with less RAM and processing power like microcomputers and mobiles.
input_shape=(224,224,3) => this is the input dimensions of the model. this is the parameter mentioned in the processing part.Tthe 3 refers to the three channels R,G,B. We are training it partially so as to reduce the traning time on the stake of accuracy. (it is better to train model fully for better results)

4.MODEL COMPILATION - The built neural network has to be compiled before training. It is compiled using a loss function, optimizer and metrics. Here, crossentropy loss function, adam optimizer and accuracy, precision, recall and AUC are the different metrics.

5.MODEL TRAINING - Ensure that the gpu (Graphics Processing Unit) is used so as to boost the training speed.

6.MODEL EVALUATION - The trained model is evaluated on training, validation and test dataset.

7.MODEL PREDICTION - In this part the trained model is used to predict the intestinal abnormalities present in the input image.

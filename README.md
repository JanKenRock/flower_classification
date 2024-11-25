# flower_classification

**Abstract** *We train the pretrained ResNet50 model on a dataset consisting of images of classes of flowers. Given an image of an arbitrary flower from any of these classes, the resulting model will be able to predict - with a certain accuracy - which exact class the flower belongs to.*

We train a neural network to classify images of different types of flowers. Instead of training a new neural network from scratch we make use of the concept of transfer learning. In transfer learning, a pretrained model, which has been trained previously for a specific task, is fine-tuned for a new but related task. This is achieved by freezing early layers and retraining only the later layers of the pretrained model. In this way, much of the knowledge the model had gained during its original training is preserved. For example, when a model is trained to classify images of cars, it often learns to extract low-level features such as edges or local textures in its early layers. But if the model is later retrained to classify images of busses, the extraction of such general features is likely to be still useful. The preservation of the knowledge of the pretrained model leads to an essential advantage in transfer learning. Namely, starting from a pretrained model typically requires much smaller amounts of data, computational resources and time to achieve similar results as in the training of an entirely new model.

In our specific setting, we make use of the pretrained ResNet50 model. This model is a convolutional neural network consisting of 50 layers which has been trained for image classification tasks on the ImageNet dataset, containing more than 14 million images from 1000 classes. We retrain this model on a set of 102 flower classes, which can be accessed via the link

http://www.robots.ox.ac.uk/~vgg/data/flowers/102/

Our procedure consists of the following four steps:

    1.) We download the necessary data.
    2.) We split the data into training, validation and test sets and prepare it for the training of the model.
    3.) We train the model.
    4.) We evaluate the model.

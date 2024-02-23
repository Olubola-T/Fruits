# Fruits
A simple neural network for sorting fruits

INTRODUCTION

This project is a simple neural network for sorting fruits. There are three kinds of fruit in the mix: peaches, pomegranates, and strawberries. A model was trained to identify the image of each fruit and assign the right label to it.

DATA COLLECTION AND PROCESSING

Images of  three kinds of fruit were extracted from a Kaggle dataset (https://www.kaggle.com/datasets/alihasnainch/fruits-dataset-for-classification?resource=download). The os module was used to assess the folder containing each type of fruit. A function was defined to vectorize each image with the cv2 module (OpenCV) and assign a label to it. Each image vector and its label constituted an array; the arrays of all images in each fruit folder constituted a list. After treating each fruit folder this way, the three fruit lists were combined and shuffled. 

MODELING

The data was split into training and testing data, and a simple neural network was built and trained with the training data. As this is a single-label multi-class classifcation problem, categorical crossentropy was the loss function of choice, and softmax activation was used for the ouput layer of the network.

RESULTS

With 30 training epochs and a batch size of 10, the model achieved accuracies of 0.64 and 0.61 on the training and test data respectively.

LIMITATIONS

An attempt to visualize the test set image vectors yielded non-satisfactory output. Many of the images were whitened out. This is indicative of defective vectorization of the images and may have affected the efficacy of model training. Similar results were obtained when the original images were vectorized with imageio. Future versions of this project will address this problem and explore hidden layers in the neural network. 

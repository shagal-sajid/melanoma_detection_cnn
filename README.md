Project Description:
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

Table of Contents:
* CNN models were developed using the dataset.
* Python technology is used
* Different models were tried to get the model with better accuracy.


General Information:
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following diseases:

Actinic keratosis
Basal cell carcinoma
Dermatofibroma
Melanoma
Nevus
Pigmented benign keratosis
Seborrheic keratosis
Squamous cell carcinoma
Vascular lesion

Steps Done:

Data Reading/Data Understanding :
Read the images fromthe paths

Dataset Creation:
Create train & validation dataset from the train directory with a batch size of 32. And with image height and width as 180.

Dataset visualisation :
visualized one instance of all the nine classes present in the dataset 

 

Model Building & training : 
1st Model: 
Created a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescaled images to normalize pixel values between (0,1).

It has 4 convolution layers.After every set of convolutional layers, there is a max pooling layer. All the pooling layers in the network use a window of 2 x 2 pixels.  Finally, the output of the last pooling layer is flattened and fed to a fully connected (FC) layer,followed by another FC layer of 4096 neurons, and finally to a 9-softmax output. The softmax layer uses the usual categorical_crossentropy loss function, adam optimiser and accuracy as metrics. All layers apart from the softmax use the ReLU activation function.

Trained  the model for ~20 epochs. Training accuracy is around 0.7 and validation accuracy i 0.6.

2ndModel:

2nd Model is developed same as first model , and added dropouts after mapooling layer.Validation accuracy is improved.

Handling class imbalances: 

Rectified class imbalances present in the training dataset with Augmentor library.
Model Building & training on the rectified class imbalance data :
Same model is developed pn recitified  data.
Train the model for ~30 epochs

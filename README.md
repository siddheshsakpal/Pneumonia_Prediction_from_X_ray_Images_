# Pneumonia_Prediction_from_X_ray_Images_

 working on a project for pneumonia prediction from X-ray images using a VGG16 model. Here's a summary of code and the encountered error:

Overview of the Code:
 defined a custom preprocessing function preprocess_image for the X-ray images.
 imported the VGG16 model with ImageNet weights, froze the existing weights, and added custom fully connected layers for binary classification.
 set up data generators for training and testing, applying the custom preprocessing function to the training data.
 defined callbacks for ModelCheckpoint, EarlyStopping, and TensorBoard.
 compiled the model with the Adam optimizer and binary crossentropy loss.
 attempted to train the model using the fit method on the training and validation datasets.
Error Encountered:
You encountered a RuntimeWarning: overflow encountered in ubyte_scalars during the custom image preprocessing step. This warning is likely related to the use of the cv2.threshold function and suggests that there may be an issue with the data type of the image.

During the training of the model, you encountered a FailedPreconditionError. This error seems related to writing summary data for TensorBoard and may be caused by an issue with the specified log directory ('/content/drive/MyDrive/logs'

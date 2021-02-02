+++
title = "Training"
chapter = true
weight = 20
+++

## Training the model

After you label your images, you’re ready to train your model.

Training a model is how Amazon Rekognition can learn to detect puppies in photos based on your dataset. As with humans, computers take a while to learn as well!

As part of model training, Amazon Rekognition Custom Labels requires a labeled test dataset. Amazon Rekognition Custom Labels uses a test dataset to verify how well your trained model predicts the correct labels and generate evaluation metrics. Images in the test dataset are not used to train your model and should represent the same types of images you will use your model to analyze.

1. Choose **Projects**.
2. Choose your project **PuppyChallenge**
3. Choose **Train new model**.
![Train new model](40_training/images/training-01.png "Train new model")
4. For *Choose project*, choose your **PuppyChallenge** project.
5. For *Choose training dataset*, choose your **Puppies** dataset.
6. For *Create test set*, choose **Split training dataset**. Amazon Rekognition will hold back 20% of the images for testing and use the remaining 80% of the images to train the model.
![Choose training dataset](40_training/images/training-02.png "Choose training dataset")
7. Choose **Start training**

{{% notice warning %}}
Our model took approximately one hour to train. The training time required for your model depends on many factors, including the number of images provided in the dataset and the complexity of the model.
{{% /notice %}}

When training is complete, Amazon Rekognition Custom Labels outputs key quality metrics including F1 score, Average precision, Overall recall, and the Assumed threshold for each label.

![Choose training dataset](40_training/images/training-03.png "Choose training dataset")

Each person will have a different quality metrics based on the photos they used for training. A model with better quality metrics will be better at recognizing a puppy. The metrics will be explained in more detail in the next section.

{{% notice info %}}
Share a screenshot of your highest score on the chat.
{{% /notice %}}

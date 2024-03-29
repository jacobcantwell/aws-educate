+++
title = "Training"
chapter = true
weight = 50
+++

## Training the model

After you label your images, you’re ready to train your model.

Training a model is how Amazon Rekognition can learn to detect puppies in photos based on your dataset. As with humans, computers take a while to learn as well!

As part of model training, Amazon Rekognition Custom Labels requires a labeled test dataset. Amazon Rekognition Custom Labels uses a test dataset to verify how well your trained model predicts the correct labels and generate evaluation metrics. Images in the test dataset are not used to train your model and should represent the same types of images you will use your model to analyze.

If you are still in your *PuppyChallenge* project page:

1. Choose **Train new model**.

If you are back on the *Amazon Rekognition Custom Labels* page,

1. Choose **Projects**.
2. Choose your project **PuppyChallenge**
3. Choose **Train new model**.
![Train new model](50_training/images/training-01.jpg "Train new model")
4. For *Choose project*, choose your **PuppyChallenge** project.
5. For *Choose training dataset*, choose your **PuppyPhotos** dataset.
6. For *Create test set*, choose **Split training dataset**.

With a *Split training dataset*, Amazon Rekognition will hold back 20% of the images for testing and use the remaining 80% of the images to train the model.
![Choose training dataset](50_training/images/training-02.jpg "Choose training dataset")
7. Choose **Train**

Amazon Rekognition will return to the *PuppyChallenge* project page. You should see that there is now a new model with a Model Status *TRAINING_IN_PROGRESS* and status message *The model is being trained.*
![Training in progress](50_training/images/training-03.jpg "Training in progress")

{{% notice warning %}}
Our model took approximately one hour to train. The training time required for your model depends on many factors, including the number of images provided in the dataset and the complexity of the model.
{{% /notice %}}

Refresh the page after waiting a while and eventually the *Model status* should change to *TRAINING_COMPLETED*.

Choose **PuppyChallenge.2021-02-11T##.##.##** when the model is trained to view the evaluation results.

![Training completed](50_training/images/training-04.jpg "Training completed")

In the next step, we will evaluate the quality of your model.

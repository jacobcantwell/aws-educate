+++
title = "Evaluating"
chapter = true
weight = 60
+++

## Evaluating the model

After the puppy classifier model is trained, you can review the model performance by accessing the *Evaluation results* in the console.
![Choose training dataset](60_evaluating/images/training-03.jpg "Choose training dataset")

You can better understand the metrics for evaluating the model performance from our guide below. Each person will have a different quality metrics based on the photos they used for training. A model with better quality metrics will be better at recognizing a puppy.

{{% notice info %}}
Share a screenshot of your highest score on the chat.
{{% /notice %}}

During testing, Amazon Rekognition Custom Labels predicts if a test image contains a custom label. The confidence score is a value that quantifies the certainty of the model’s prediction. If the confidence score for a custom label exceeds the threshold value, the model output will include this label.

### Precision

Our model has been trained to detect only the puppies and not the kittens.

*Precision* is the fraction of correct predictions (true positives) over all model predictions (true and false positives) at the assumed threshold for an individual label. For example, the fraction of puppies correctly identified among the total number of puppies the computer program thinks is in the photo.

![Some kittens and puppies](60_evaluating/images/evaluation-results-01.jpg "Some kittens and puppies")

For example, when the model predicts that a puppy is present in an image, how often is that prediction correct? Suppose there’s an image with 8 puppies and 5 kittens. If the model predicts 9 puppies—8 correctly predicted and 1 false positive—then the precision for this example is 0.89 (8/9). However, if the model predicted 13 puppies in the image with 8 correct predictions and 5 incorrect, then the resulting precision is lower.

![A cat labelled as a dog](60_evaluating/images/evaluation-results-02.jpg "A cat labelled as a dog")

![Average precision](60_evaluating/images/evaluation-results-03.jpg "Average precision")

### Recall

Recall is the fraction of your test set labels that were predicted correctly.

If an image contains 8 puppies, how many of them are detected correctly? An example where an image has 8 puppies and 5 kittens, if the model detects 5 of the puppies, then the recall value is 0.62 (5/8). If after retraining, the new model detected 9 puppies, including all 8 that were present in the image, then the recall value is 1.0.

#### Overall model performance

Amazon Rekognition Custom Labels provides an average model performance score for each label and an average model performance score for the entire test dataset.

Model performance is an aggregate measure that takes into account both precision and recall over all labels (for example, F1 score or average precision). The model performance score is a value between 0 and 1. The higher the value, the better the model is performing for both recall and precision.

A high value for F1 score indicates that the model is performing well for both precision and recall. If the model isn't performing well, for example, with a low precision of 0.30 and a high recall of 1.0, the F1 score is 0.46. Similarly if the precision is high (0.95) and the recall is low (0.20), the F1 score is 0.33. In both cases, the F1 score is low and indicates problems with the model.

Read more information on [Metrics for Evaluating Your Model](https://docs.aws.amazon.com/rekognition/latest/customlabels-dg/tr-metrics-use.html)

In the next step, we will start our model and start testing.

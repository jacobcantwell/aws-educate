+++
title = "Evaluating"
chapter = true
weight = 60
+++

## Evaluating the model

When training is complete, Amazon Rekognition Custom Labels outputs key quality metrics including F1 score, Average precision, Overall recall, and the Assumed threshold for each label.

![Choose training dataset](60_evaluating/images/training-03.jpg "Choose training dataset")

Each person will have a different quality metrics based on the photos they used for training. A model with better quality metrics will be better at recognizing a puppy. The metrics will be explained in more detail in the next section.

{{% notice info %}}
Share a screenshot of your highest score on the chat.
{{% /notice %}}

### What do your Evaluation results mean?

#### Overall Score

The F1 score is the measure of the overall accuracy of your model. It combines the precision and recall scores. A high F1 score means that your computer can accurately detect if puppies are in a photo.

A score 0.667 means that the computer can accurately detect puppies in 66.7% of all photos.

#### Average Precision

Below is a photo of *two kittens* and *three puppies* being best friends.
![Some kittens and puppies](60_evaluating/images/evaluation-results-01.jpg "Some kittens and puppies")
Our model has been trained to detect only the puppies and not the kittens.
Suppose our model for recognizing puppies mistakenly identified four puppies in a picture that only contains three puppies and two kittens. Of the four puppies it identified, only three are actually puppies and the other one is a kitten the model mistakenly identified as a puppy.
![A cat labelled as a dog](60_evaluating/images/evaluation-results-02.jpg "A cat labelled as a dog")
The *Average precision* is the percentage of puppies correctly identified among the total number of puppies the computer program thinks is in the photo.
![Average precision](60_evaluating/images/evaluation-results-03.jpg "Average precision")

In the next step, we will test our model.

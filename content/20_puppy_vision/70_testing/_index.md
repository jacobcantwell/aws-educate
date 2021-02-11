+++
title = "Testing"
chapter = true
weight = 70
+++

## Testing the model

You trained model is now ready to integrate into a website, software applications, mobile phone apps, any way that you think you can use it.

### How to use your model

In the *Use your model* section, there is sample code for starting your model, analyzing and image, and stopping your model.

![Use your model](70_testing/images/testing-01.jpg "Use your model")

There are multiple methods and programming languages that you can use to do this so that you can integrate it into your business.

#### Starting and stopping a model

See the full instructions for [Starting or Stopping an Amazon Rekognition Custom Labels Model (Console)](https://docs.aws.amazon.com/rekognition/latest/customlabels-dg/rm-start-model-console.html)

{{% notice warning %}}
There are some costs to training and running the model. [Amazon Rekognition Custom Labels pricing](https://aws.amazon.com/rekognition/pricing/). Search the pricing page for *Pricing example 1 – Image Labeling for a Website*
{{% /notice %}}

#### Amazon Rekognition Custom Labels Demo

There is also a demonstration web application that you can deploy to view your model in a web application. [Amazon Rekognition Custom Labels Demo](https://github.com/aws-samples/amazon-rekognition-custom-labels-demo)

Deploying the web application will be part of our next workshop and for now we will test a trained model that we started earlier.

{{% notice info %}}
You have done all of the hardwork creating a dataset, labelling your data, training a model, and evaluating the model results. Post in the chat how you would use your own custom label model in your own software.
{{% /notice %}}

### Use a pretrained model

We have deployed a puppy model using the instructions above and deployed it with a *Amazon Rekognition Custom Labels Demo* web application above.

1. Open a new web browser tab and go to **https://d18nql8vde59kw.cloudfront.net/**
2. Login with the username **puppy**
3. Use password **puppy4#**
4. Choose the model
5. Upload an image of a puppy
6. View the results of the custom label

{{% notice info %}}
Post in the chat if the model detected your puppy image.
{{% /notice %}}

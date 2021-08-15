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

* Select your model
* Select *Use Model*
* Select number of Inference units, choose *1 inference unit*
* Select *Start Model*

{{% notice info %}}
When your model is starting. It might take up to 30 minutes to start running.
{{% /notice %}}

See the full instructions for [Starting or Stopping an Amazon Rekognition Custom Labels Model (Console)](https://docs.aws.amazon.com/rekognition/latest/customlabels-dg/rm-start-model-console.html)

{{% notice warning %}}
There are some costs to training and running the model. [Amazon Rekognition Custom Labels pricing](https://aws.amazon.com/rekognition/pricing/). Search the pricing page for *Pricing example 1 – Image Labeling for a Website*
{{% /notice %}}

#### Amazon Rekognition Custom Labels Demo

Deploying the web application will be part of our next step and for now we will test a trained model that we deployed earlier.

{{% notice info %}}
You have done all of the hardwork creating a dataset, labelling your data, training a model, and evaluating the model results. Post in the chat how you would use your own custom label model in your own software.
{{% /notice %}}

### Use a pretrained model

We have deployed a puppy model using the instructions above and deployed it with a *Amazon Rekognition Custom Labels Demo* web application above.

1. Open a new web browser tab and go to **https://dwizm1fya2bik.cloudfront.net/**
2. Login with the username **puppy2**
```bash
puppy2
```
3. Use password **puppy2#**
```bash
puppy2$
```
4. Choose the **PuppyChallenge.2021-##-##T##.##.##** model
5. Upload an image of a puppy.
6. View the results of the custom label.

![Output of the model](70_testing/images/testing-02.jpg "Output of the model")

You can see the *Results* from the train model output. The labels and confidence scores are listed and this web application draws a box around any puppies it has detected.

Look at the response to see the label applied to your image.

```json
{
  "CustomLabels": [
    {
      "Confidence": 83.60199737548828,
      "Geometry": {
        "BoundingBox": {
          "Height": 0.6938999891281128,
          "Left": 0.2750700116157532,
          "Top": 0.23050999641418457,
          "Width": 0.4900299906730652
        }
      },
      "Name": "Puppy"
    }
  ]
}
```

{{% notice info %}}
Post in the chat if the model detected your puppy image.
{{% /notice %}}

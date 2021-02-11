+++
title = "Amazon Rekognition"
chapter = true
weight = 10
+++

## Amazon Rekognition

Let’s get started on the Puppy Challenge journey!

{{% notice warning %}}
To complete this challenge (and the rest of the workshop) please follow the instructions. The buttons which you need to press are circled in **red** and have our fun pet, Monty, hanging on as well. If you get lost, please ask your teacher or raise your hand in the chat.
{{% /notice %}}

To understand more about what Amazon Rekognition can do, let’s try the out-of-the box demonstrations. Let’s try a celebrity challenge first.

1. To begin, type *Amazon Rekognition* in the AWS Management Console search bar.
```bash
Amazon Rekognition
```
![AWS Management Console search bar](10_rekognition/images/rekognition-01.jpg "AWS Management Console search bar")
You are now on the Amazon Rekognition homepage. Amazon Rekognition can detect specific people, celebrities and even objects from photos you upload.

### Celebrity recognition

1. On the left-hand side of the page, choose **Celebrity Recognition**.
![Celebrity Recognition](10_rekognition/images/rekognition-02.jpg "Celebrity Recognition")

On the Celebrity recognition page, you will find this picture of Amazon founder Jeff Bezos. If you look to the right, you can see that AWS Rekgonition has identified that the person in the photo is Jeff Bezos with 100% confidence.
![Jeff Bezos](10_rekognition/images/rekognition-03.jpg "Jeff Bezos")

3. Choose the **Upload** button.
4. Upload a photo of a famous celebrity and see if Rekognition can recognise them.

### Object and scene detection

Rekognition automatically labels objects, concepts and scenes in your images, and provides a confidence score.

1. Choose **Object and Scene Detection** and try uploading another photo to see what objects Amazon Rekognition can detect.

### Facial analysis

Get a complete analysis of facial attributes, including confidence scores.

1. Choose **Facial Analysis** and try uploading another photo to see what facial features Amazon Rekognition can detect.

### Text in image

Rekognition automatically detects and extracts text in your images.

1. Choose **Text in image** and try uploading another photo to see what text Amazon Rekognition can extract.

### Personal Protective Equipment (PPE) detection

Amazon Rekognition can automatically detect Personal Protective Equipment (PPE) such as face covers, head covers, and hand covers on persons in images.

1. Choose **PPE detection** and try uploading another photo to see what text Amazon Rekognition can extract.

Try the *Video analysis* demonstration to see similar object detection features in videos. You can also expand this technology to detect objects in live video streams.

## Other AWS AI Services

### Amazon Translate

* Search the AWS Management Console, for **Amazon Translate**
* Choose **Launch real-time translation**
* Try translating some words into different languages.

### Amazon Polly

* Search the AWS Management Console, for **Amazon Polly**
* Choose **Get started**
* Type in some plain text words and choose **Listen to speech**

### Amazon Textract

* Search the AWS Management Console, for **Amazon Textract**
* Choose **Try Amazon Textract**
* You can upload an image of a document and Amazon Textract will extract the text into a structured format.

**Fantastic! How amazing is the Cloud?**

The steps above show how Amazon Rekognition and the other AWS machine learning services are pretrained to detect certain things. But what should you do if you want to find objects and scenes that are unique to your own business?

After today, you will know how to create you very own model that can detect whatever you want in a photo or video, like a puppy!

+++
title = "Custom Labels"
chapter = true
weight = 20
+++

## Amazon Rekognition Custom Labels

Amazon Rekognition Custom Labels is a feature of Amazon Rekognition that enables customers to build their own specialized machine learning (ML) based image analysis capabilities to detect unique objects and scenes integral to their specific use case. 

Instead of having to train a model from scratch, which requires specialized machine learning expertise and millions of high-quality labeled images, customers can use Amazon Rekognition Custom Labels to achieve state-of-the-art performance for their unique image analysis needs.

### Get started

Let’s get started building a model that can detect puppies.

1. Type *Amazon Rekognition* in the AWS Management Console search bar.
![AWS Management Console search bar](20_custom_labels/images/create-project-01.jpg "AWS Management Console search bar")
2. You are now on the Amazon Rekognition homepage. On the left-hand side of the page, choose **Use Custom Labels**.
![Choose Use Custom Labels](20_custom_labels/images/create-project-02.jpg "Choose Use Custom Labels")
3. You are now on Amazon Rekognition Custom Labels page. Choose **Get Started** to continue.
![Choose Get Started](20_custom_labels/images/create-project-03.jpg "Choose Get Started")
4. You might see a *First time set up* popup window. Amazon Rekognition requires an S3 bucket to store your project files. Choose **Create S3 bucket**.
![Create S3 bucket](20_custom_labels/images/create-project-04.jpg "Create S3 bucket")
6. Select *Projects*, in the left menu.
7. Select *Create Project*
8. To start the project, we need to give it a name. Type in *PuppyChallenge*.
```bash
PuppyChallenge
```
![Enter project name](20_custom_labels/images/create-project-05.jpg "Enter project name")
1. Choose **Create project**.
![Choose Create project](20_custom_labels/images/create-project-06.jpg "Choose Create project")
2. Select *Projects*, in the left menu.
3. Select your *PuppyChallenge* project.

We are now ready to move on to the next stage of the Puppy Challenge.

+++
title = "Puppy Vision Workshop"
chapter = true
weight = 20
+++

## Creating the project

To create the project, complete the following steps! The buttons you need to press are circled in red and have our AWS mascot, Peccy, hanging on as well! If you get lost, ask us for help.

1. Search Amazon Rekognition in the AWS management console search bar.
2. On the Amazon Rekognition Console, choose **Use Custom Labels**
3. Click **Get Started**
4. For Project name, type in *PuppyChallange*. Do not leave a space.
5. Choose **Create project**

## Creating the dataset

To train our program to detect puppies, we need to create a dataset first. A dataset is collection of data which is needed to train the cloud to detect puppies in photos.

It is like learning at school; in order to remember a fact you need to repeat it.

Go and find the following photos of puppies on the internet.

* 5 photos of puppies by themselves
* 5 photos of puppies at the beach
* 5 photos of puppies with people

1. To create the data set click on **Create data set**
2. Select *Upload pictures from your computer*
3. Choose **Add images**
4. Drag your chosen photos into the box to upload them  

## Labelling

To tell the machine what it needs to learn, you need to teach it what it has to recognize! We do this by drawing boxes around the puppies in your photos.

1. Click on **Add** and type in *Puppies*.
2. Select on all the images by clicking the small blue square and click draw bounding box.
3. Use the mouse to draw a box around the puppies.
4. After you have drawn a box around all the puppies in all the photos, click done.

## Training the model

Now it’s time to train your model.

1. Click on train model
1. For choose training dataset, choose your *Puppy* dataset

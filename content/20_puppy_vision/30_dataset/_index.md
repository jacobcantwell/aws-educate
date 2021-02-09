+++
title = "Dataset"
chapter = true
weight = 30
+++

## Creating the dataset

In this part of the challenge we will choose the images we want Amazon Rekognition to use to train our machine learning model. We need to first create a dataset. The dataset will be a collection of puppy photos that Amazon Rekognition will learn from in order to detect puppies in photos.

![Two very cute puppies](30_dataset/images/two-cute-puppies.jpg "Two very cute puppies")

To train Amazon Rekognition how to detect puppies, we need to give it a set of puppy photos first so it can learn what they look like.

You have ten minutes to find the following photos of puppies on the internet. Search the free stock photos [Pexels website](https://www.pexels.com/search/puppy) to find some photos of puppies.

* Five cute photos of golden puppies
* Five photos of puppies at the beach
* Five funny photos of puppies

Make sure to save all pictures to your desktop.

1. We need to start by creating the data set. Choose **Create dataset** to begin.
![Create data set](30_dataset/images/create-dataset-01.jpg "Create data set")
2. Like when you have a puppy, it is also important to name our data set. Type in *PuppyPhoto* into the data set name box.
```bash
PuppyPhoto
```
![Create data set](30_dataset/images/create-dataset-02.jpg "Create data set")
3. We need to upload the pictures you found earlier to the data set! Choose **Upload images from your computer**.
![Upload images from your computer](30_dataset/images/create-dataset-03.jpg "Upload images from your computer")
4. To add photos into the dataset, you can either drag your photos from the desktop into the data set or click **Choose files** and select your puppy photos from the desktop.
![Choose files](30_dataset/images/create-dataset-04.jpg "Choose files")
5. Choose **Submit**.

In the next step, we will start labelling our photos.

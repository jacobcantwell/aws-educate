+++
title = "Labelling"
chapter = true
weight = 40
+++

## Labelling

You tell Amazon Rekognition what it needs to learn by creating labels in each photo. To create a puppy label we need to draw a bounding box around the puppy in the photo.

### Edit labels

1. We need to create a label. Choose **Add labels** and a popup window will appear.
![Add labels](40_labelling/images/labelling-01.jpg "Add labels")
2. Choose **Add labels** and type in *Puppies*.
```bash
Puppies
```
3. When you are done choose **Add label**.
4. Choose **Save**.
![Add Puppies label](40_labelling/images/labelling-02.jpg "Add Puppies label")

You should see a *Puppies* label appear in the *Filter by labels* section.

## Assign labels

1. Choose all the images by selecting the **small blue checkbox** in each photo. Choose as many photos as you can, the photo background will change to a light blue colour.
2. Choose **Draw bounding box**.
![Select the images](40_labelling/images/labelling-03.jpg "Select the images")
3. Use your mouse to draw a box around each puppy. Choose **Next** to move to the next photo.
![Draw a bounding box](40_labelling/images/labelling-04.jpg "Draw bounding box")
4. Go through all your pictures. After you have drawn a box around all the puppies in all the photos, choose **Done**.
![Choose Done when finished](40_labelling/images/labelling-05.jpg "Choose Done when finished")

In the next step, we will start training our model.

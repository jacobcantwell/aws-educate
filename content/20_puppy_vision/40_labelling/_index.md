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
3. The first time you label photos you might get a popup for *Tips for Drawing Bounding Boxes*. Read the tips and choose **Next** until the popup closes.
4. Use your mouse to draw a bounding box around each puppy. Try to keep the bounding box as close to the puppy as possible.

{{% notice info %}}
If there are multiple puppies in a photo, add a bounding box for each puppy. e.g. Four puppies = four bounding boxes.
{{% /notice %}}

5. Choose **Next (shift + ->)** to move to the next photo.
![Draw a bounding box](40_labelling/images/labelling-04.jpg "Draw bounding box")
6. Repeat drawing the bounding box and choosing next through all your pictures.
7. After you have drawn a box around all the puppies in all the photos, choose **Done (shift + d)**.
![Choose Done when finished](40_labelling/images/labelling-05.jpg "Choose Done when finished")
8. Choose **Save changes**
9. You should see a page filled with puppies and labels. We now need to repeat this process for the rest of your images.
10. Choose **2** to move to the page 2 of images.
11. Repeat the process above for all of your images until we label 30 images.

{{% notice info %}}
Remember to **Save changes** after adding a bounding box.
{{% /notice %}}

12. When you are done, choose **Exit**.

If you exit, you can always come back and add more labels by choosing **Start Labelling**.

In the next step, we will start training our model.

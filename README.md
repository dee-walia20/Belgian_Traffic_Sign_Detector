# Belgian_Traffic_Sign_Detector
Image Classification on Traffic signal signs

The goal is to build a model that can detect and classify traffic signs in a video stream taken from a moving car. 
Given an image of a traffic sign, our model should be able to tell it's type (e.g. Stop sign, speed limit, yield sign). 
We'll work with images that are properly cropped such that the traffic sign takes most of the image. 
So don't worry about edge cases as of now.

We will use the Belgian Traffic Sign Dataset because it is big enough to train on, and yet small enough to be easy to work with.

You can download the dataset from : http://people.ee.ethz.ch/~timofter/traffic_signs/index.html

There are a lot of datasets on that page, but you only need the two files listed under BelgiumTS for Classification (cropped images):

BelgiumTSC_Training
BelgiumTSC_Testing

The images in this dataset are in an old .ppm format. So old, in fact, that most tools don’t support it. 
Which meant that we cann’t casually browse the folders to take a look at the images. 
Luckily, the Scikit Image library recognizes this format. 
This code below will load the data and return two lists: images and labels.

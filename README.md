
# Brain Tumor Classification Using Deep Learning

The process of Classification is divide into two parts:
1. Image Pre-processing stage
2. Image Classification using CNN stage

## Overview of dataset
<li> The dataset consist of two type of images(MRI scans)
<li> The types are:
<ul>
<li> Scans with brain tumor labelled as "YES"
<li> Scans without brain tumor labelled as "NO"
</ul>
<li> Image size: Variable
<li> Image color: Gray Scale

## Image Pre-processing stage
<p>
For segmenting the images we have used K-means clustering with number of clusters equals to 3. The process of segmentation helped us to 
render the region of interest. The sgemented images helped us to visualise the ROI(region of intrest) with excellent details
</p>
<p>
The processing of the images are done with openCV module of python. The sole reason to perform semantic image segmentation on MRI 
scans was to reduce the over all complexity of the model from training to testing.
</p>
After segmenting all the images we have fed the images to our CNN(convolutional neural netwok) in order to do the training.

## Image Classification using CNN stage

<p> For image classificattion we have used a 27 layered Deep neural network with 5 Convolution blocks and 2 dense blocks.</p>
<li> Each convolution block consist of three layers: 2D convolution followed by Batch-normalisation then 2D Max pooling.
<li>Each dense block consist of a dense layer followed by batch normalisation.
<li>Remaining are some regularisation and dropout layers.

<p>The implementation of the CNN is done with tensorflow and keras

<b>All the stats and logs are present in the Classification report folder.</b>
<hr>
<p>Research Paper Draft Link: https://docs.google.com/document/d/1yZPBoo7TFp-tvtQ3xOm5ZyYZZVuuHbHtu_1n4fZYrw8/edit?usp=sharing</p>

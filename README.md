# Car Damage Detection and Segmentation using Mask R-CNN

This is a project of detecting damages from the images of car. The codes are based on implementation of Mask R-CNN by (https://github.com/matterport/Mask_RCNN) on Python 3, Keras, and TensorFlow. The model generates bounding boxes and segmentation masks for each instance of an object in the image. It's based on Feature Pyramid Network (FPN) and a ResNet101 backbone.

![Instance Segmentation Sample](assets/street.png)

The repository includes:
* Source code of Mask R-CNN built on FPN and ResNet101.
* Instruction and Training code for Car Damage Detection
* Jupyter notebooks to visualize the detection pipeline at every step
* Example of training on your own dataset

# Examples

<p float="left">
  <img src="images/val/val1.jpg" width="415" height=315"/>
  <img src="predicted%20images/val1.png" width="415" height=315" /> 
</p>
<p float="left">
  <img src="images/val/val2.jpg" width="415" height=315"/>
  <img src="predicted%20images/val2.png" width="415" height=315" /> 
</p>
<p float="left">
  <img src="images/val/val3.jpeg" width="415" height=315"/>
  <img src="predicted%20images/val3.png" width="415" height=315" /> 
</p>
<p float="left">
  <img src="images/val/val4.jpg" width="415" height=315"/>
  <img src="predicted%20images/val4.png" width="415" height=315" /> 
</p>
<p float="left">
  <img src="images/val/val5.jpg" width="415" height=315"/>
  <img src="predicted%20images/val5.png" width="415" height=315" /> 
</p>

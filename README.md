# Car Damage Detection and Segmentation using Mask R-CNN

This is a project of detecting damages from the images of car. The codes are based on implementation of Mask R-CNN by (https://github.com/matterport/Mask_RCNN) on Python 3, Keras, and TensorFlow. The model generates bounding boxes and segmentation masks for each instance of an object in the image. It's based on Feature Pyramid Network (FPN) and a ResNet101 backbone.

The repository includes:
* Source code of Mask R-CNN built on FPN and ResNet101.
* Instruction and Training code for Car Damage Detection
* Jupyter notebooks to visualize the detection pipeline at every step
* Example of training on your own dataset

# Collecting Data

* I have collected all the images from google images.
* I split the images in 223 train images and 15 validation images.
* I annotate the images using [VIA (VGG Image Annotator)](http://www.robots.ox.ac.uk/~vgg/software/via/via-1.0.6.html) because of its simplicity.It’s a single HTML file that you download and open in a browser.
* The VIA tool saves the annotations in a JSON file, and each mask is a set of polygon points.

# Training

* I make the file [car_damage.py](car_damage.py) using the instruction from [this blogpost](https://engineering.matterport.com/splash-of-color-instance-segmentation-with-mask-r-cnn-and-tensorflow-7c761e238b46).
* I used Transfer Learning, which simply means that, instead of training a model from scratch, I start with a weights file that’s been trained on the COCO dataset.
* Mask R-CNN is a fairly large model. Especially that our implementation uses ResNet101 and FPN. So you need a modern GPU with 12GB of memory. I used Google Colab's Tesla K80 GPU to train this model.
* I train the model for 100 epochs, after which I got 0.1894 - training loss and 1.9137 - validation loss.

You can find the training steps in [car_damage_training.ipynb](car_damage_training.ipynb).

# Result

* You can inspect the result in [car_damage_inspect_data.ipynb](car_damage_inspect_data.ipynb), [car_damage_inspect_model.ipynb](car_damage_inspect_model.ipynb), [car_damage_inspect_weights.ipynb](car_damage_inspect_weights.ipynb).

* Below are some predicted images from validation dataset. 

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
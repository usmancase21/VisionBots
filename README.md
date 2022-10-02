# VisionBots

## Problem: Weeds are an unwanted intruder in the agricultural business. They steal nutrients, water, land, and other critical resources to grow healthy crops. These intruders can lead to lower yields and inefficient deployment of resources by farmers.




## Factors: One known approach is to use pesticides to remove weeds, but aggressive pesticides create health risks for humans. 



## Solution: Computer vision technology can automatically detect the presence of weeds and use targeted remediation techniques to remove them from fields with minimal environmental impact.

We used opensource Dataset from RoboFlow and here is link 
Data is acquired by Roboflow:
#### DataSet :

# https://universe.roboflow.com/augmented-startups/weeds-nxe1w


We haved Used YOLOV7 


YOLOv7 infers faster and with greater accuracy than its cohorts, pushing the state of the art in object detection to new heights.


The YOLOv7 sought to set the state of the art in object detection by creating a network architecture that would predict bounding boxes more accurately than its peers at similar inference speed


# Extended Efficient Layer Aggregation
In YOLOv7, considers memory it takes to keep layers in memory along with the distance that it takes a gradient to back-propagate through the layers - the shorter the gradient, the more powerfully their network will be able to learn. The final layer aggregation they choose is E-ELAN, an extend version of the ELAN computational block

# Model Scaling Techniques

Object detection models are typically released in a series of models, scaling up and down in size, because different applications require different levels of accuracy and inference speeds

YOLOv7  we scale the network depth and width in concert while concatenating layers together. Ablation studies show that this technique keep the model architecture optimal while scaling for different sizes.


# Re-parameterization Planning

Re-parameterization techniques involve averaging a set of model weights to create a model that is more robust to general patterns that it is trying to model. In research, there has been a recent focus on module level re-parameterization where piece of the network have their own re-parameterization strategies.


The YOLOv7 uses gradient flow propagation paths to see which modules in the network should use re-parameterization strategies and which should not.


Auxiliary Head Coarse-to-Fine


The YOLO network head makes the final predictions for the network, but since it is so far downstream in the network, it can be advantageous to add an auxiliary head to the network that lies somewhere in the middle. While you are training, you are supervising this detection head as well as the head that is actually going to make predictions.

YOLOv7 experiment with different levels of supervision for this head, settling on a coarse-to-fine definition where supervision is passed back from the lead head at different granularities.




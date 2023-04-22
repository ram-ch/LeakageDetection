## Introduction:       
In this notebook I have performed transfer learning on custom dataset with a pretrained object detection model. The dataset is a collection of images of water leaking from different faucets & fittings. This is a simulation model to detect leakages of liquids in an industrial setup.   
## Dataset:   
The data set contains 74 images dowloaded from the internet. I have labelled these images using an open source annotation tools called VGG image annotator 
There is another set of 24 images kept aside for testing. The target class is water droplet leaking out of a pipe fitting/joint.   
The data set is available [Here](https://drive.google.com/drive/folders/1fx7FTiTXmBxInhokokyc5G9oG6wurfaN?usp=share_link)     
The train and test labels are available in train.csv and test.csv files respectively
   
**Train Sample**    
   
![train sample](img/train_sample.png)

## Algorithm:
The algorithm is a pretrained FasteRCNN model with a RestNet50 network as backbone. This is a pretrained model on coco dataset. Only the final detection layers are modified to suit the number of target classes in our custom dataset. The accuracy of this model is good but the model suffers with slow inference speed. For realtime detection faster networks like ssd and yolo are more suitable 


**Test Results**   
![test results](img/test_1.png)
![test results](img/test_2.png)
![test results](img/test_3.png)
![test results](img/test_4.png)
![test results](img/test_5.png)
![test results](img/test_6.png)
![test results](img/test_7.png)

Even though the model is trained on a very less number of images and epoch, the detection is good.
**Next Steps**   
* Since this exercise is limited to a very small data set. I have not included any performance metrics.     
* Relevant plots of metrics like MaP, precision, recall , IoU, ROC-AUC curves can be included when the model is trained with more data and more numbre of epochs    
* Models like Yolov8 can be tried for faster and more accurate predictions   

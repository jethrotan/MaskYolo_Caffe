# YOLO Caffe version with MaskRCNN

### Reference

> You Only Look Once: Unified, Real-Time Object detection http://arxiv.org/abs/1506.02640

> YOLO9000: Better, Faster, Stronger https://arxiv.org/abs/1612.08242

> YOLOv3: An Incremental Improvement https://pjreddie.com/media/files/papers/YOLOv3.pdf

### Data preparation
* Prepare data lsit just like the way of original darkenet

* Use train.txt to generate lmdb for training

* yolo v2 (RegionLossLayer) and v3 (YoloLossLayer) are supported

### Object Detection with YOLO
support to use yolo v2 or v3 to detect objects in images
1. prepare lmdb for object detection 
```
cd ROOT
sh ./data/yolo/convert_detection.sh  #generate lmdb for detection
cd ./maskyolo/models/mobilenetv2-yolo/
nohup sh yolo_train.sh > train.log &

```

2. objection demo
```
tbd
```
examples of detection on KITTI
![](assets/detection1.png)


### Instance mask and Keypoint recognization with MaskRCNN combined YOLO

Use yolo results as input to feed to `roi_ppooing` or `roi_alignment` layer 
1. prepare lmdb for mask regression
```
xxx
```

2. yolo with mask demo
```
xxx
```

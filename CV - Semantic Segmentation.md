
### Faster R-CNN
- it uses ROI Pooling


IoU
- it is a measure of overlapping between the bounding boxes

Non-max suppression
### Mask R-CNN
- it uses ROI-Align

1. Backbone - ResNet50 + FPN
- FPN - Feature Pyramid Network

1. RPN - Region Proposal Network

2. ROI Classifier and Bounding Box Regressor

3. Segmentation Mask

[original repo- tf-1.x](https://github.com/matterport/Mask_RCNN/tree/master)
[medium article](https://jonathan-hui.medium.com/image-segmentation-with-mask-r-cnn-ebe6d793272)
[tutorial](https://www.youtube.com/watch?v=WuvY0wJDl0k)
#### use with tensorflow
- [install tutorial](https://www.youtube.com/watch?v=Fu_km7FXyaU), take care of the numpy version
- [forked repo tf-2.x](https://github.com/ahmedfgad/Mask-RCNN-TF2)

Annotatio tools
- MaskSense
- [label-studio](https://www.youtube.com/watch?v=UUP_omOSKuc)

# Computer vision 3: Detection, Segmentation, and Tracking

## Object detection

Bounding box + class

Non-Maximum Suppression(NMS)\
Problem: if 2 objects are highly overlapping
  
Intersection over Union(IOU), Jaccard Index:\
J = |A and B| / |A or B|
  
- One-stage detectors
  Feature extraction -> classification (Softmax loss, calls cross entropy loss), localization (L2 loss) \
  - YOLO, SSD, RetinaNet(Focal loss, handle foreground-background imbalance)
  - CenterNet, CornerNet, ExtremeNet
  
- Two-stage detectors  
  Feature extraction -> extraction of object proposals -> classification, localization
  - R-CNN, Fast R-CNN, Faster R-CNN

### Detection evaluation
- Presicion: how accurate your predictions are
  Presicion = TP/(TP+FP)
- Recall: how good you are at finding all positives
  Recall = TP/(TP+FN)
  
  
  
### Human pose estimation
- Direct regression
- heatmap prediction

Hourglass-Unet-Autoencoder

## Object tracking
Why? To model objects when detection fails, predict trajectory

- Matching/correspondence problem
- appearance learning
- prediction problem
  ROLO = CNN + LSTM
  
Online tracking:
1. Track initialization (using a detector)
2. Prediction of the next person (motion model)
3. Matching predictions with detections (appearance model)

#### Similarity learning
Learn a function that measures how similiar 2 objects are\
Use the same network to encode the image\
Compare the encodings

Siamese network = shared weights

Hinge loss\
Contrastive loss\
Triplet loss: allows to learn a ranking

## Semantic segmentation
Do not differentiate between the instances

### Autoencoder-style
SegNet\
Encoder:normal convolutional filters + pooling\
Decoder: Upsampling + convolutional filters\
Transposed convolution

Upsampling:\
- Interpolation
- Fixed unpooling

### Skip connections(U-Net)

### 3 challenges of semantic segmentation
- Reduced feature resolution

  Dilated(atrous) convolutions -> larger receptive field
- Obejct exist at multiple scales
- Pool localization of the edges

## Instance segmentation

- Proposal-based
  1. Proposals
  2. Assign a class

- FCN-based
  1. Segmantic segmentation
  2. Find instances (clustering)
  
Mask-RCNN: Faster R-CNN + FCN for segmentation

## Panoptic Segmentation
Semantic segmentation + Instance segmentaion\
Labels to uncountable objects ("stuff", sky, road)
differentiates instances of the countable objects ("things", people, cars)








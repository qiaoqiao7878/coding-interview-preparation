# Summary of Practical course
Visual based navigation

### Camera calibration

We know the 3D coordinates of calibration pattern (chess board)\
Minimize the differnces between detected points and projected points\
Optimize the camera calibration and camera position with respect to calibration pattern

### Representation of Rotation
- SO(3) matrics
- Angle-axis
- Euler angles
- Quanternions

Gimbal lock:
Singularity always exist if we use 3 parameters to describe rotation

Distortion:
- Barrel distortion
- Pincushion distortion

### Optimization
#### First order methods
Grdient Descent

#### Second order methods
Newton's method
Gauss-Newton method
Levenberg-Marquardt Method

Ceres:
for least-squares optimization

### Keypoint detection

Corner has significant change in all directions

SSD: Sum of Squared Differences

Harris Detector
FAST Detector: relation of brightness values to center pixel along circle

### Keypoint Descriptors:
Goal: match keypoints regardless of image transformation

#### SIFT
"Scale Invariant Feature Transform"

- Take 16x16 square window 
- computer angle of the gradient for each pixel
- Create histogram of surviving edge orientations

16 cells * 8 orientations = 128 dimensional descriptor

Can handle up to 60 degree of plane rotation

#### BRIEF
“Binary Robust Independent Elementary Features”

Binary Descriptors

#### ORB
“Oriented Fast and Rotated BRIEF”

FAST detector and BRIEF descriptor

rotation-invariant BRIEF

### Matching distance

match should be "unique"

### RANSAC
RANdom SAmple Consensus

1. Computer required number of iterations
2. for N iterations:
  1. randomly select a subset of data points
  2. fit model on the subset
  3. count inliers and keep the best model/subset with largest number of inliers
3. refit the model using found inlier set


### Epipolar Constraint
Outliers can be filtered

### Motion estimation from point correspondences
#### 2D-2D
Determine relative motion between the frames\
reprojection error

Algorithm: 8-point, 5-point
#### 2D-3D
Determine camera pose in world frame
Reprojection error

Algorithm: DLT PnP \
DLT:Direct linear transform \
PnP: Perspective-n-Points
#### 3D-3D

### Place recogtion with Bag of Words

### Structure from Motion
3D reconstruction using a set of unordered images

Localization with known map(2D-3D)
Mapping with known poses (2D-2D) -> Triangulation
Joint refinement -> Bundle adjustment

#### Triangulation
reconstrut 3D point from 2D image observations for known camera poses

#### Bundle adjustment

Jointly estimating 3D coordinates of points and camera parameters.

camera localizations and sparse geometrical reconstruction, given a strong
network of matches and good initial guesses are provided.

Aims to minimize the reprojection errors

### Simultaneous Localization and Mapping (SLAM)
Estimate 6 DoF poses and map from sequential image data

### Covisibility Graph
undirected weighted graph.\
Each node is a keyframe and an egde exists if they share observation of same map points, weight is the number of common points.

### Loop closing
1. Loop candidates detection, computer the similarity between the bag of words vector of keyframes.
2. compute the transformation between these 2 frames
3. Loop fusion, fuse duplicated map points and insert new edges in the covisibility graph
4. Essential graph optimization

### Lifelong operation
Detect redundant keyframes and delete them.\
Because Bundle adjustment complexity grows with the number of keyframes.\
Imagine if the camera stays there or move in a small area.





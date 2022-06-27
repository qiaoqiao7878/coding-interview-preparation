# 3D Scanning & Motion Capture

## Capture devices
Passive:
- RGB
- Stereo and Multi-view

Active:
- Time of Flight: Kinect V2
- Struture light: Kinect V1
- Laser Scanner, LIDAR

## Camera distortion
- Radial: e.g. "fish eye" effect
- Tangential: if image plane and lens are not parallel


## Project
Load SMPL model in Unity\
SMPL blendshapes script to control the body shape and pose in Unity\
KinectSDK package transform the human motion to SMPL model\
Compare poses using joint angle\
25 joints

## 3D representations
- Voxels
- Point clouds
- Meshes
- Parametric surfaces
- Implicit surfaces, e.g. SDF signed distance field


## Features
- SIFT\

Scale-Invariant feature transform
128 dimensional, costly to compute, 8-bin orientation histograms
- SURF
- ORB

### Properties of good features
- Fast comparisions
- Scale invariant
- View invariant
- Lighting invariant

## 3D reconstruction

- Visual Hull Carving
- Structure from Motion
m images, n points in 3D\
Number of unknowns: 6(m-1) unknown camera poses, 3n for points, possibly intrinsics\
Number of constraints: 2mn (constraints are in 2D)
- Multi-view Stereo
  Goal: create an as-dense-as-possible point cloud

  Final reconstruction: 
  - Use point cloud as input, compute normals
  - Surface fitting, such as poisson surface reconstruction
  - Texture

- RGB-D reconstruction
  - frame to frame tracking
  - frame to model tracking

Reading list: https://github.com/openMVG/awesome_3DReconstruction_list

### Poisson surface reconstruction
Input: point cloud with normals
Output: Implicit function  -> mesh

## Optimization
Non-linear least squares\
First order, second order\
- Gradient Descent
- Newton's method
- Gauss-Newton
- Levenberg: "damped version of Gauss-Newton" -> Trust region
- Levenberg-Marquardt (LM)

## Iterative Closest Points (ICP)
- Selecting source points
- Matching to points in other scan
- Weighting the correspondences
- Rejecting outlier point pairs
- Assgining an error metric to the current transform
- Minimizing the error metrix with respect to transformation

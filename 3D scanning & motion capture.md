# 3D Scanning & Motion Capture

## Capture devices
Passive:
- RGB
- Stereo and Multi-view

Active:
- Time of Flight: Kinect V2
- Struture light: Kinect V1
- Laser Scanner, LIDAR


## Project
Load SMPL model in Unity\
SMPL blendshapes script to control the body shape and pose in Unity\
KinectSDK package transform the human motion to SMPL model\
Compare poses using joint angle\
25 joints

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


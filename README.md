# depth_fusion_kinectfusion
fuse noisy depth information from a low cost rgb-d scanner or MVS into a clean mesh , my implementation of "Hernandez, M., Choi, J., & Medioni, G. (2015). Near laser-scan quality 3-D face reconstruction from a low-quality depth stream. Image and Vision Computing, 36, 61-69."

The central ideal is to project a collection of depth images or back-projected point cloud, onto a virtual cyclindrical surface surrounding the object of interest. The cylinder has a discretized surface, analogous to a image wrapped in a cylinder. When multiple depth values ar projected onto a single pixel, their mean is taken. Next, this virtual image is filtered using a bilateral filter. Finally, neighbouring "pixels" are connected to form a mesh represntation of the surface.

#  Data or field connection 

 1. Data connection: Connect two different point clouds to the same point cloud. Before performing the connection operation, ensure that the fields in the two datasets have the same type and equal dimensions. Example 1: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574252575
  ```  
 Example 2: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574252575
  ```  
 2. Field connection: For the connection of two fields (e.g. color, normal) with different point clouds, there is a mandatory constraint that the number of points in the two datasets must be the same. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574252575
  ```  
#  Code implementation 

 1. Data connection 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574252575
  ```  
 2. Field connection 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574252575
  ```  


--------------------------------------------------------------------------------

#  First, the code implementation 

##  1. Fit to obtain cylinder parameters 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574284543
  ```  
##  2. Directly specify the cylindrical parameters 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574284543
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574284543
  ```  
 ![avatar]( c44478e3107b490888f25ec81216476a.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Algorithm overview 

   The current 3D convolution computation is too large and the development is not particularly mature. Point cloud projection to a 2D plane can be processed with the help of image algorithms. Of course, some point cloud information will be lost. If multiple dimensions are projected, the lost information can be reduced to a relatively low level. At present, one of the most widely used projection methods for point cloud projection is to generate top views. 

##  2. Projection to the plane 

   The general equation of the three-dimensional space plane is: assume that the coordinates of the three-dimensional space that is not on the plane are, and the coordinates of the projection point on the plane are. Because the projection point to the current point is perpendicular to the plane, according to the vertical constraint condition, the following conditions are satisfied: Substituting (2) and (3) into (1) can be solved: substituting (4) into (2), (3), we can get: 

   Projection coordinates from three-dimensional point to plane are obtained. 

##  3. Formula corresponding code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574273118
  ```  
#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574273118
  ```  
#  III. Display of results 

 ![avatar]( 20210207111039708.png) 

#  IV. Python code 

 Open3D - Point Cloud Projection to Fitting Plane (Python Detailed Procedure Edition) 



--------------------------------------------------------------------------------

 Point cloud projection to the sphere, is an application example of PCL projection filter, PCL1.11.1 is not implemented. This blog handwritten code implementation. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574271760
  ```  
#  III. Display of results 

##  1. Primitive point cloud 

 ![avatar]( dba2ac429b0d443aa3cfc018d9a3bb45.png) 

##  2. Point cloud after projection 

 ![avatar]( 522dd20229d44679a36b5109bedacdb6.png) 



--------------------------------------------------------------------------------

#  I. Overview 

 ![avatar]( 22159f48335140f3909dae8a5f26a666.png) 

    Aiming at the point cloud random rendering and color assignment function in CloudCompare software, this paper gives the code implementation of random color assignment using PCL for some point clouds.  

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574294817
  ```  
#  III. Display of results 

 ![avatar]( 84f87da4a80747b6857f5f7fedd129e7.png) 



--------------------------------------------------------------------------------

#  Visual rendering 

   First get a pcd point cloud of type PCL :: Point XY ZL, then render according to the categorization label. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574278785
  ```  
#  III. Display of results 

 ![avatar]( 489634a0e37048029b8e5dc5536c6bbf.png) 



--------------------------------------------------------------------------------

#  Visual rendering 

   First extract the time from the las point cloud data with the time index according to the custom point type, and then render according to the time. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574273396
  ```  
>  MyPointCloud.h, MyPointCloud.cpp See: PCL extracts scan lines according to time index 

#  III. Display of results 

 ![avatar]( 0460714d7cf640749514ba0b29afc363.png) 

#  IV. Save the rendering results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574273396
  ```  
  Here is a PCL point cloud according to the elevation rendering method for color rendering according to the time index, the final effect is inconsistent with the above color rendering results. 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

>  First, the extreme elevation value (including the maximum and minimum elevation values) of the point cloud where it is located is calculated according to the Z-axis direction, and the median elevation is calculated; then the values of the rendered red, green and blue colors are selected. Finally, from top to bottom, the process of gradual change of the three colors of red, green and blue is performed, that is, the minimum coordinate of the point cloud is set to blue, the middle value is set to green, and the maximum value is set to red. In the lower half of the point cloud, the ratio of the elevation value of each laser point in the interval where the median value and the minimum value are located is calculated in turn, and then green is increased according to the ratio on the basis of blue; similarly, each laser point in the upper half of the point cloud increases red according to the ratio on the basis of green. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574270986
  ```  
#  III. Display of results 

 ![avatar]( ec6433308dc24402b6df093dec9e52cf.png) 

#  CloudCompare 

 ![avatar]( 20201231103449200.gif) 

 Related implementation operations in CloudCompare software  

#  V. Remarks 

   If you only visualize the results of point cloud rendering by elevation without saving the rendered results, you can directly call the PointCloudColorHandlerGenericField function in PCL to achieve. For specific usage methods, see: Color to distinguish depth. 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Overview 

 ![avatar]( 20200727195559873.jpg) 

   The image information perceived by human vision is not obtained from an isolated pixel, but from an area composed of a large number of pixels. Isolated single pixels have no specific practical significance, only many pixels are combined together to make sense for human visual perception. It can be seen that pixels are not the focus of visual perception. Under this demand, the concept of "super pixels" was born in the field of two-dimensional image processing. The so-called super pixel is a small area composed of many pixels, which are adjacent in position and have certain similarities in certain features (such as image brightness, color, texture, etc.). Most of these small areas do not destroy the boundary information of the image, but also retain effective information for further segmentation of the image. Nowadays, superpixels are more and more widely used in the field of computer vision, and as the initial stage of image segmentation and pattern recognition, the most fundamental reasons are: on the one hand, the use of superpixels can effectively reduce the redundancy of local image information, which greatly reduces the complexity and computation of image processing; on the other hand, traditional image processing methods based on pixel level cannot accurately locate the boundary of the target area, and can only give an approximate position. In the field of 3D point cloud data processing, the concept of superpixels is borrowed from the concept of superpixels in 3D space. In this section, we will learn how to use pcl:: SupervoxelClustering to segment a point cloud into a number-addressed hypervoxel cluster, and learn how to use and visualize the adjacency graph information with the hypervoxel itself.  

##  2. Super pixel 

   Superpixel segmentation algorithms divide pixels in an image into semantic regions that conform to the boundaries of the target object. Graph-based algorithms, such as MRF and CRF, have become popular because they can better integrate high-level semantic knowledge with low-level image features. Instead of eliminating the computationally intensive pixel-level graph operations, they have turned to a mid-level inference framework that does not deal directly with pixels, but uses groups of pixels, which are called superpixels. Using small regions that have been segmented, superpixels are formed through local low-level features. Note that the pixels here correspond to points in the point cloud. The difference is that point clouds are generally disordered, while pixels are ordered, but they can be understood as a discrete sampling representation of space. Superpixels have some very important characteristics. Among them, the superpixel's avoidance of crossing object boundaries is its most important feature. Because violating object boundaries will reduce the accuracy of subsequent classification. Another useful property is the regular distribution of superpixels after segmentation, as this produces a simple graph for subsequent merge optimization segmentation steps. 

##  3. Super Body Element 

 ![avatar]( 20200727195922708.jpg) 

   PCL :: SupervoxelClustering implements VCCS (Voxel Cloud Connectivity Segmentation) method, which belongs to a super pixel method. This method can generate voxel-level segmentation of 3D point cloud data, and the obtained segmentation result is called hypervoxel. In terms of processing object boundaries, hypervoxels are better than existing methods based on 2D images. At the same time, the method maintains high efficiency. Using the spatial octree structure, VCCS uses the regional growth of k-means clustering to directly perform hypervoxel segmentation on point clouds. The resulting hypervoxels have two important properties: first, they are uniformly distributed in 3D space, which is achieved by uniformly setting seeds in point cloud space; second, hypervoxels cannot cross boundaries unless the voxels are spatially connected. The octree structure can be used to determine whether leaf nodes are adjacent. In the 3D space of voxelization, hypervoxels maintain an adjacent relationship, which means that these voxels share common faces, edges and vertices, as shown in the figure below.  

 ![avatar]( 20200727200408162.jpg) 

   The Adjacency Graph of hypervoxels can be effectively maintained by using the R_voxel nearest voxels of the octree, in which the R_voxel specifies the resolution of the octagonal leaf nodes. The adjacency graph is used not only for the region growth process during hypervoxel generation, but also to determine the adjacency relationship between hypervoxels. VCCS is a region growth algorithm. Under a three-dimensional spatial grid with a spatial resolution of R_seed, the algorithm grows seed points uniformly distributed in space to form hypervoxels. In order to improve efficiency, VCCS does not perform a global search and only considers points within the R_seed radius centered on the seed, as shown in the figure below. In addition, by searching with the seed as the center, the seeds that do not have enough neighboring voxel addresses are deleted within a certain radius.  

 ![avatar]( 20200727200545913.png) 

   The extension of the seed point is determined by the feature distance, which takes into account the space, color, and the feature space calculation of the normal vector. The space is achieved by seed resolution normalization, and the color distance is D_c the Euclidean distance in the normalized RGB space. The normal batch distance D_n the angle of the surface normal address between the seeded seed and the candidate point. The general process is as follows: Start with the voxels closest to the cluster center and flow towards the neighboring voxels. Using the above-mentioned distance formula to evaluate the neighboring voxels, calculate the characteristic distance between these neighboring voxels and the super-voxel center. If the distance is minimal, label the voxel as belonging to the superexel, and in the adjacency diagram, add the voxel's neighbors to the search sequence for this label. The next iteration processes the next superexel, with each outward iteration from the center of the superexel defined as being the same temporal hierarchy for all superexels. The 2D version, as shown in the diagram below, iterates outward with the center of the seed voxel until the edge of the search volume for each superexel is reached (or there are no other adjacent points to traverse).  

 The edges connected to the seed point in the proximity graph do not need to be traversed, and the default seed is already in the traversal queue. 

##  4. References 

>  [1] doc：Clustering of Pointclouds into Supervoxels - Theoretical primer [2] PCL：;pcl::SupervoxelClustering 

#  Code implementation 

>  There are two versions of the widely aborted hypervoxel segmentation code on the Internet, as follows: 

##  1. Official website code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574176071
  ```  
##  2. My code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574176071
  ```  
#  III. Display of results 

 ![avatar]( 1ffcb26cda564b818083da91ce3d121c.png) 

>  The blue ball is the center of each super voxel, the green line and the blue ball constitute the graph structure formed by the super voxel, and the point cloud collection and spatial sampling area in each super voxel represented by different color point clouds. 

#  IV. Application cases 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574176071
  ```  
#  V. Display of results 

 ![avatar]( bd45e8e9f15e4fe480d7d5a191aa99d3.png) 

#  VI. Related Links 

 [1] pcl::SupervoxelClustering< PointT > Class Template Reference [2] Clustering of Pointclouds into Supervoxels - Theoretical primer [3] PCL点云库学习笔记（6）：点云超体素化(VCCS) 



--------------------------------------------------------------------------------

#  I. Overview 

   Point cloud de-centroid is an important step in computing point cloud covariance. Find out the out-point cloud centroid point, subtract the coordinates of the centroid point from each point, and finally save it as point cloud data. It can play a role in hiding the real coordinate information of the point cloud. It is used in SVD transformation matrix, principal component analysis covariance matrix and other operations. 

#  Second, the main function 

 PCL :: de mean Point Cloud () subtracts a centroid from the point cloud and returns the result of de-averaging 

>  To use this function, add: #include < pcl/common/centroid.h > header file 

 overload method 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574272175
  ```  
#  III. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574272175
  ```  
#  IV. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574272175
  ```  


--------------------------------------------------------------------------------

 + 1. Orderly point cloud 

 + 2. Disordered point cloud 

#  First, orderly point cloud 

##  1、pcd2png 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574257022
  ```  
   The implementation converts ordered point clouds into images. When calling the savePNGFile function, if the third parameter is not filled in, it defaults to "rgb". Other available attribute information is: "normal", "label", "z", "curvature", and "intensity". 

##  2. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574257022
  ```  
##  3. Display of results 

   No ordered point cloud with intensity, not achieved. 

#  Disordered point cloud 

##  1. Algorithm principle 

   First, the point cloud is two-dimensional grid (see the implementation principle: PCL point cloud two-dimensional grid), and then the maximum intensity value in each grid is used as the color of the image (of course, you can also use inverse distance weighting for intensity calculation, if you are interested, please do it yourself!!). 

##  2. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574257022
  ```  
##  3. Display of results 

 ![avatar]( b2ccf6cffed8437484bc305c0c59a467.png) 



--------------------------------------------------------------------------------

 + 1. Pan (translate) 

 + 1. Theoretical foundation 2. Code implementation 3. Results display

 + 2. Rotation 

 + 1. Theoretical foundation 2. Code implementation 3. Results display

 + 3. Scale 

 + 1. Theoretical foundation 2. Function analysis 3. Code implementation 4. Results display

 Transformation matrix (General transformation) 

 + 1. The meaning of the transformation matrix

 + 5. Euclidean transformation 

 + 1. Theoretical foundation 2. Code implementation

 + 5. Affine transformation 

 + 1. Theoretical foundation 2. Code implementation

#  Translation (translated) 

##  1. Theoretical basis 

   Translation is the operation of moving a point a certain distance in a specific direction. Moving the point along the vector direction is obtained by writing this equation in the form of homogeneous coordinates as: where: Therefore, the conversion process to which can be obtained is expressed as:, the transformation matrix is: The matrix is generally called a translation vector. It is easy to verify that the inverse of the translation vector is:  

##  2. Code implementation 

 Translate 0.1m along the X-axis, 0.2m along the Y-axis, and 0.3m along the Z-axis. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574225694
  ```  
##  3. Display of results 

 ![avatar]( 9fb5e2d2ff5341adba29ac521cdc126f.png) 

 Red is the original point cloud, green is the transformed point cloud  

#  Second, rotation (Rotation) 

##  1. Theoretical basis 

   Rotation depends on the angle at which the axis of rotation rotates around the axis of rotation. 

 ![avatar]( 7bb1f61b66174d18865f607a5e1b08e2.png) 

   Both translation and rotation are rigid body motions that do not change the size and size of the object. 

##  2. Code implementation 

 There are various expressions of rotation, which can be obtained by rotation vector, Euler angle, quaternion, direct assignment, etc. Here only the rotation matrix is constructed from rotation vector. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574225694
  ```  
##  3. Display of results 

 ![avatar]( 9c9f739efe2d46879ee1a1db0680434d.png) 

 Red is the original point cloud, green is the transformed point cloud  

#  Scaling (Scale) 

##  1. Theoretical basis 

 ![avatar]( c5b718d3629846b0a275d35a8cb582a7.png) 

   Scaling can be independently applied to three coordinate axes, such as converting a point to a new point: This results in the corresponding matrix: its inverse is: If the scaling factor is equal, then the scaling change is equal scale, and the object retains the shape but changes the size. Otherwise, it is called non-equal scale when scaling transformation, and the object deforms.  

##  2. Function analysis 

 The Scaling function supports matrix and quaternion operations, and is mainly called in the following ways: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574225694
  ```  
##  3. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574225694
  ```  
##  4. Display of results 

 ![avatar]( b63e2e317ab84c688d30ce8b236b9897.png) 

 Red is the original point cloud, green is the transformed point cloud  

#  IV. Transformation matrix (General transformation) 

##  1. The meaning of the transformation matrix 

 ![avatar]( 2021020521363056.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

 ![avatar]( d931218ecd5b4463862129384cd0e0e9.png) 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574292456
  ```  


--------------------------------------------------------------------------------

 + 1. Display the color characteristics of the point cloud itself 

 + 2. Customize point cloud color characteristics 

 + 3. Randomly generate colors 

 + 4. Differentiate the depth by color 

 + 5. Intensity rendering 

 + 6. Time rendering 

 + 7. Label rendering 

 + 8, gradual change rendering 

 + 9. Visualization of corresponding point pairs 

 CloudViewer class 

 + 11. Code summary 

 + 12. Related Links 

#  First, display the color characteristics of the point cloud itself 

   PointCloudColorHandlerRGBField requires that the point cloud type contains three color components of RGB, that is, the method directly displays the RGB attribute field information of each point in the point cloud, rather than displaying different colors by coloring the point cloud. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574224067
  ```  
 ![avatar]( 20201110135345434.png) 

#  Second, custom point cloud color characteristics 

   PointCloudColorHandlerCustom works with any format point cloud, it is not required that the point cloud type contain three RGB color components, that is, the point cloud with id "sample cloud" is colored as a whole. The value range of custom RGB colors is [0,255] 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574224067
  ```  
   setPointCloudRenderingProperties the same effect as the above code, the RGB value range of the custom color is [0,1] 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574224067
  ```  
 ![avatar]( 2020111013550869.png) 

#  Third, randomly generate colors 

   PointCloudColorHandlerRandom applies to any point cloud and renders it by randomly generating a color. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574224067
  ```  
 ![avatar]( 20201110134929638.png) 

#  Fourth, distinguish the depth by color 

   PointCloudColorHandlerGenericField display different depth values as different colors to achieve the purpose of distinguishing the depth by color; the difference of the point cloud according to the depth value ("x", "y", "z" can be used) is implemented as a code of different colors as follows: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574224067
  ```  
 ![avatar]( 20201110135201698.png) 

#  V. Intensity rendering 

   PointCloudColorHandlerGenericField < PointT > extracts 1D data using fields given by the user and displays colors at each point using a min-max look up table. The implementation code is as follows: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574224067
  ```  
 ![avatar]( 20210515204539354.png) 

#  Six, time rendering 

 PCL point cloud rendering by time coloring 

#  Label rendering 

 PCL point clouds render by categorization label 

#  Eight, gradual change rendering 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574224067
  ```  
 ![avatar]( 20210530170051273.png) 

#  Nine, corresponding point pair visualization 

   PCL :: registration :: CorrespondenceEstimation < pcl :: Po int T, pcl :: Po int T > correspond_est; After calculating the corresponding point pair, the index of the corresponding point of source and target will be stored in vector < int > A or pcl :: Correspondences A. To display the correspondence of the point pair, just view- > addCorrespondences < pcl :: PointXYZ > (source, target, A, "corresponding", v1); where pcl :: PointXYZ indicates that the type of the corresponding point pair added is PointXYZ type, the first two parameters represent the target point cloud and the source point cloud, A stores the index of the corresponding point from the target point cloud to the source point cloud, "correspondence" is a custom label, v1 represents which window to add to. In order to make the corresponding point more personalized, we can "customize" it: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574224067
  ```  
 Set the thickness of the corresponding point connection. PCL_VISUALIZER_LINE_WIDTH, indicating the line operation, the width of the line segment is 2 (the width of the line segment should not exceed the size of the custom point), "corresponding" means yes, the corresponding label, do processing. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574224067
  ```  
 Set the color of the corresponding dot connection, ranging from 0 to 1. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574224067
  ```  
 ![avatar]( 20201115085215984.png) 

#  CloudViewer class 

   CloudViewer is a straightforward, simple way to visualize a point cloud with as little code as possible. However, CloudViewer does not support multi-threaded applications. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574224067
  ```  
#  Code summary 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574224067
  ```  


--------------------------------------------------------------------------------

#  First, the main function 

##  1、std::sort 

 Defined in the header file < algorithm > 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574237691
  ```  
   Sort elements in the range [first, last) in undescending order. The order of equal elements is not guaranteed to be maintained. If comp (* (it + n), * it) evaluates to false for any iterator that points to a sequence and any non-negative integer n such that it + n is a legal iterator that points to a sequence element, the sequence is said to be sorted with respect to comp. 

#  Point cloud sorting 

 The code is sorted from small to large according to the size of the Z coordinate as an example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574237691
  ```  
#  III. Display of results 

>  It can be seen that the Z coordinates are arranged in ascending order. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574237691
  ```  
#  IV. Reference link 

 std::sort std::sort 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Algorithm overview 

   IterativeClosestPointWithNormals default uses a transformation based on point-to-plane distance estimation, the implementation uses a traditional point-to-plane target and calculates the point-to-plane distance using the normals of the target point cloud. 

>  It also provides the option to use the symmetric objective function [Rusinkiewicz 2019] (implemented by setUseSymmetricObjective, see Symmetric-ICP for more details). This objective uses the normals of the source and target point clouds, and has similar computational costs to traditional point-to-plane targets, while also improving convergence speed and wider convergence range. 

##  2. Algorithm flow 

 The implementation of this blog is: Yang Chen, and Gerard Medioni. Object Modeling by Registration of Multiple Range Images. International Journal of Image and Vision Computing, 10 (3), pp. 145-155, 1992. The method in this article. 

 ![avatar]( 20210516145658292.png) 

   The traditional ICP algorithm adopts minimizing the distance between the corresponding points of the source point cloud and the target point cloud as the registration criterion, as shown in Figure (a). The point-to-plane ICP adopts minimizing the distance from the point in the source point cloud to the plane where the corresponding point in the target point cloud is located as the registration criterion, in which the transformation matrix is represented; the corresponding points in the source point cloud and the target point cloud are represented respectively; and the normal vector of the corresponding points is represented. Its principle is shown in Figure (b). Compared with the traditional ICP algorithm, the point-to-plane ICP can better reflect the spatial structure of the point cloud; can better resist erroneous corresponding point pairs; and has a faster iterative convergence speed.  

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574228564
  ```  
#  III. Display of results 

 ![avatar]( 20210209114254286.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. References 

>  [1] Low K L . Linear Least-Squares Optimization for Point-to-Plane ICP Surface Registration[J]. Chapel Hill, 2004. [2] Yang Chen, and Gerard Medioni. Object Modeling by Registration of Multiple Range Images. International Journal of Image and Vision Computing, 10(3), pp. 145–155, 1992. 

##  2. Nonlinear least squares optimization 

 PCL :: registration :: TransformationEstimationPointToPlane uses Levenberg Marquardt optimization to find the transformation that minimizes the point-to-plane distance between a given correspondence. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574261589
  ```  
#  III. Display of results 

 ![avatar]( 20201123155047370.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Algorithm overview 

>  Point-to-plane metrics are often solved using standard non-linear least squares methods, such as Levenberg-Marquardt. Each iteration of the point-to-plane ICP algorithm is usually slower than the point-to-point algorithm, but converges significantly faster. The relative rotation between the two point clouds is less than 30 °. To improve the numerical stability of the calculation, a distance comparable to the size of the rotation angle needs to be used. The simplest approach is to re-scale and move the two input point clouds so that they are bounded within a unit sphere or cube centered at the origin.

##  2. Linear optimization 

    In 2004, et al. proposed using the linear least squares method to calculate the point-to-surface ICP registration algorithm. It was confirmed that the ICP method using the point-to-surface method to calculate the conversion matrix is faster and has higher registration accuracy than the ICP method using the point-to-surface method to calculate the conversion matrix. The point-to-surface method to calculate the conversion matrix is to use the least squares method to optimize the calculation of the conversion matrix between two input 3D models in each iteration of the ICP algorithm. Given a source model and a target model, the ICP algorithm is used to find the nearest point as the corresponding point of the point. The point-to-surface method is to find the tangent plane with the minimum distance from the source point to the corresponding target point. Let, is a source point, is the target point of the response, is the unit normal direction, our goal is to find the formula (1) in each ICP iteration. 3-D rigid body transformation matrix is composed of rotation matrix = and translation moment matrix.  

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574240573
  ```  
#  III. Display of results 

 ![avatar]( 20201121112723788.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

>  This blog simply records the implementation of the code. Poisson surface reconstruction is an extremely complex algorithm. In practical applications, there are quite professional processing software and algorithms for point cloud 3D reconstruction, which are basically not based on PCL. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574299826
  ```  
#  III. Display of results 

 ![avatar]( 91304882046f42d9942180a8dffcf0bf.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Algorithm overview 

   The Poisson surface reconstruction method commonly used in PCL is limited in practical application due to its high computational complexity and low algorithm efficiency. In order to change this situation, the algorithm was optimized in PCL 1.13.0 version, and multi-threaded parallel was added on the basis of the original algorithm. 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957427464
  ```  
 Note: This function was added to PCL1.13.0 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957427464
  ```  
#  III. Display of results 

 ![avatar]( 31340dc7d1374c1da23dc9e41461635e.png) 



--------------------------------------------------------------------------------


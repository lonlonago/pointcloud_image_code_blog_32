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


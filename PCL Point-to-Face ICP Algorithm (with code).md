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


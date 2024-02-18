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


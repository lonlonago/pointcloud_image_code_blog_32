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


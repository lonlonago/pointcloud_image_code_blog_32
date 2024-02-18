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


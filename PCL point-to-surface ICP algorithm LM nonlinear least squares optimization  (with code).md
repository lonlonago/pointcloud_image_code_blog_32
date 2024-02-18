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


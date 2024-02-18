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


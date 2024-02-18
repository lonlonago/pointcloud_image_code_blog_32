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


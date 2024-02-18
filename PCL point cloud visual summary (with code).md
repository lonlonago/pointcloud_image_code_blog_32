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

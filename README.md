### Radius-measurement-of-a-turning-circle-in-ELTE-parking-lot-based-on-GPS-locations

Recorded data when the car took full circles in the parking lot. There are two circles, one of those should be processed. 

GPS data is given in the CSV file. The lateral (lat) and longitudinal (lon) coordinates can be read from the corresponding columns.  

 
The task is to automatically and robustly segment the points corresponding to one of the turning circles and then to estimate the radius of the circle. 

 
Conversion of GPS lat/lon coordinates to spatial locations: 

x = R * cos(lat) * cos(lon) 
y = R * cos(lat) * sin(lon) 
z = R *sin(lat) 

Where R=6.371.000m (radius of Earth) 


Step 1: Data loading  and conversion  of GPS locations to spatial coordinates are the initial tasks. 

Step 2: Project the 3D points onto the plane of the ground plane to obtain 2D coordinates.

Step 3: The implementation for RANSAC algorithm itself costs, that for circle estimation. The radius is estimated from all the inliers. Finally, save the results in xyz format, then visualize the selected inliers in Meshlab. 

![Best_fitted_Circle](https://github.com/syma-afsha/Radius-measurement-of-a-turning-circle-in-ELTE-parking-lot-based-on-GPS-locations/blob/main/best_fitted_circle.png)

![Final Result](https://github.com/syma-afsha/Radius-measurement-of-a-turning-circle-in-ELTE-parking-lot-based-on-GPS-locations/blob/main/Step3.png)

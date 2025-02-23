# Storefront Visibility Assessment Using Google Maps API
Storefront Visibility Assessment Using Google Maps API
Overview:
This project evaluates storefront visibility from the street by leveraging the Google Maps Street View Static API. It captures street-level images of storefronts from multiple angles and assesses visibility based on factors like obstructions, angle, and seasonality.

Approach:

Location Identification:

Collect latitude and longitude of the storefront.
API Request for Street View Images:

Request images from four angles (0°, 90°, 180°, 270°) using the Google Maps Street View Static API.
Image Processing and Visibility Scoring:

Obstruction Detection: Identify objects like trees, cars, and signs using OpenCV or YOLO.
Storefront Exposure: Calculate visible storefront area using edge detection and contour analysis.
Angle-Based Scoring: Average visibility scores from all angles.
Seasonal Adjustment (Optional): Adjust visibility based on historical imagery.
Visibility Score Formula:

Visibility Score
=
(
Visible Storefront Area
Total Storefront Area
)
×
100
Visibility Score=( 
Total Storefront Area
Visible Storefront Area
​
 )×100
Implementation:

Used Python for API calls, image retrieval, and processing.
YOLOv8 model analyzed images for obstruction and visibility scoring.
Final scores combined AI results with dataset features like traffic volume.
Results:

Captured images from multiple angles.
Analyzed visibility and assigned a final visibility score between 0 and 100.

Key Features:
* Efficient data sampling to avoid API overuse.
* Robust coordinate extraction and error handling.
*  AI-based visibility detection with Google Street View images.
* Integrated traffic volume for final score calculation.

Next Steps:

Optimize API calls and add rate limiting.
Implement address verification using Google Reverse Geocoding.
Enhance detection by combining AI and coordinate-based methods.

# Storefront Visibility Assessment Using Google Maps API
The Storefront Visibility Assessment project evaluates storefront visibility from the street by leveraging the Google Maps Street View Static API. The goal is to provide a data-driven solution for commercial realtors to assess how well a storefront can attract passersby based on its visibility. By capturing street-level images from multiple angles and processing them with AI-based image recognition, the project generates a visibility score for each location. This approach ensures more accurate assessments by considering factors such as obstructions, viewing angles, and seasonal changes.

Project Workflow:

Location Identification:

Collect latitude and longitude of the storefront.
Example Coordinates: 40.748817, -73.985428 (Empire State Building).
API Request for Street View Images:

Use the Google Maps Street View Static API to retrieve images from four angles (0°, 90°, 180°, 270°).
Image Processing and Visibility Scoring:
=
(Visible Storefront Area
Total Storefront Area)×100
Visibility Score=( 
Total Storefront Area
Visible Storefront Area
​
 )×100
Final Visibility Assessment:

For each storefront, images are captured from multiple angles.
Visibility is analyzed, and a final score between 0 and 100 is assigned, with higher scores indicating better visibility.
Key Features:

Efficient Data Sampling: Smart sampling across different road types to avoid excessive API usage.
Robust Image Processing: AI-based visibility detection using YOLOv8 and OpenCV.
Coordinate Extraction: Accurate retrieval of location data for API calls.
Error Handling: Proper exception handling for missing or malformed coordinates.
Automated Workflow: Developed and executed in Jupyter Notebook for streamlined processing.
Traffic-Aware Scoring: Integrated traffic volume with visibility scores for more accurate results.
Tech Stack:

Languages: Python
APIs: Google Maps API (Street View, Places, Reverse Geocoding)
Machine Learning: YOLOv8
Libraries: OpenCV, Pandas, Requests
Development Environment: Jupyter Notebook
Results:

Captured street-level images from multiple angles.
Detected obstructions and analyzed storefront visibility.
Assigned visibility scores between 0 and 100.
Combined AI results with traffic data to refine final scores.
Next Steps:

API Optimization: Implement rate limiting and optimize API calls.
Address Verification: Use Google Reverse Geocoding to verify storefront addresses.
Hybrid Detection: Combine AI-based detection with coordinate-based methods for maximum accuracy.
Scalability: Automate the process for large datasets and multiple storefronts.
Potential Use Cases:

Real Estate: Enable commercial realtors to evaluate storefront visibility before listing properties.
Urban Planning: Assist city planners in assessing pedestrian visibility for new developments.
Retail Analysis: Help retailers choose prime locations with high visibility for new stores.

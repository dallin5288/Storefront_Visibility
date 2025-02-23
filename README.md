Storefront Visibility Assessment 
The Storefront Visibility Assessment project evaluates storefront visibility from the street using the Google Maps Street View Static API. This solution provides a data-driven approach for commercial realtors to assess how well a storefront can attract passersby. By leveraging AI-based image processing and traffic data, the project generates a comprehensive visibility score that considers multiple factors, including viewing angles, obstructions, and seasonal variations.

The project begins with location identification, where the latitude and longitude of the storefront are collected. Using the Google Maps Street View Static API, images are captured from four primary angles: north (0°), east (90°), south (180°), and west (270°). Each image is analyzed to identify potential obstructions, such as trees, parked cars, and signs, using computer vision techniques powered by YOLOv8 and OpenCV. Additionally, edge detection and contour analysis are performed to determine how much of the storefront is visible compared to the total storefront area. To account for varying perspectives, visibility scores from all angles are averaged, ensuring a balanced evaluation.

An optional seasonal adjustment feature further refines the score by comparing historical Street View images, adjusting for conditions like foliage in summer versus bare branches in winter. 

This score, ranging from 0 to 100, provides an intuitive measure of visibility, with higher scores indicating better storefront exposure.

The project was implemented using Python, YOLOv8 for object detection, and OpenCV for image processing. Development was carried out in Jupyter Notebook, streamlining the workflow. The Google Maps API facilitated image retrieval, while Pandas and Requests libraries managed data processing and API calls. The system also incorporates traffic volume data to refine the final score, ensuring that storefronts in high-traffic areas are prioritized for visibility evaluation.

For example, a typical storefront assessment might show visibility scores like 85% from the north, 70% from the east (partially obstructed by a tree), 90% from the south, and 60% from the west (obstructed by a parked car). The final averaged visibility score in this case would be 76%. Such detailed scoring enables realtors and business owners to make informed decisions about property listings and site selection.

To enhance efficiency, the project features smart data sampling, ensuring that API requests are limited to necessary images. Robust error handling prevents disruptions from malformed coordinates, and rate limiting avoids exceeding API quotas. A hybrid approach combining AI detection with coordinate-based verification further ensures accuracy, even if the exact storefront location is slightly off.

Moving forward, potential improvements include optimizing API calls, integrating Google Reverse Geocoding for address verification, and automating the process for large datasets. This project can be scaled to support real estate platforms, urban planning initiatives, and retail site selection, empowering stakeholders with actionable insights into storefront visibility.

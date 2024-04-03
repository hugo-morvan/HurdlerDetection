# HurdlerDetection
Project aimed to develop a tool to track hurdlers during 100/110m hurdles races and extract useful information out of it. 

## Sources and Resources: 


| Source/Resource | Description |
|-----------------|-------------|
| [World Athletics research center](https://worldathletics.org/about-iaaf/documents/research-centre) | Final reports on scientific projects in the areas of biomechanics, coaching and development initiated by World Athletics, with help from the IAF (International Athletics Foundation)  |
| [Sports Analytics](https://www.ida.liu.se/research/sportsanalytics/resources/) | Resources for Sports Analytics from Linköping University|


## Brainstorming (using a LLM):

1. Lane Detection:

Implement lane detection algorithms to identify and distinguish between different lanes on the track. This can involve techniques like edge detection, Hough transforms, or deep learning-based methods.
Once lanes are detected, assign each athlete to their respective lane based on their position within the lanes.

2. Dynamic Distance Measurement:

Use reference points in the video, such as the dimensions of the hurdles, to calibrate distance measurements dynamically.
Measure the distance between reference points (e.g., hurdles) in each frame and use this information to scale other dimensions in the video.
Implement algorithms to track the movement of reference points throughout the video to account for any changes in perspective or distance.

3. Hurdle Detection and Dimension Extraction:

Develop algorithms to detect hurdles in each frame using techniques like template matching, edge detection, or deep learning-based object detection.
Extract dimensions of the hurdles from the detected regions in the video.
Use these dimensions as reference points for distance calibration and extrapolation.

4. Lane Tracking and Athlete Assignment:

Implement algorithms to track the movement of athletes within their respective lanes over time.
Assign each athlete to their corresponding lane based on their trajectory and position relative to the detected lanes.

5. Data Extraction and Analysis:

Extract relevant data such as time, speed, ground contact times, etc., from the tracked athletes using similar techniques as mentioned before.
Use calibrated distance measurements to calculate accurate speeds and distances covered by the athletes.
Analyze the extracted data to derive insights and visualize the performance of each athlete.

6. Validation and Testing:

Validate the accuracy of lane detection, distance measurement, and athlete tracking algorithms using ground truth data or manual annotations.
Test the entire system on a variety of videos with different camera angles and conditions to ensure robustness and accuracy.

7. Deployment and Continuous Improvement:

Deploy the system and gather feedback from users to improve its performance over time.
Continuously refine algorithms, optimize performance, and add new features based on user feedback and evolving requirements.

Implementing these steps will require a combination of computer vision, image processing, and algorithm development skills. Experiment with various techniques and fine-tune parameters to achieve the best results for your specific application. Additionally, consider leveraging existing libraries and frameworks to expedite development and ensure compatibility with your chosen programming environment.

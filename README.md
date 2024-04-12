# HurdlerDetection
Project aimed to develop a tool to track hurdlers during 100/110m hurdles races and extract useful information out of it. 

## Sources and Resources: 

| Source/Resource | Description |
|-----------------|-------------|
| [World Athletics research center](https://worldathletics.org/about-iaaf/documents/research-centre) | Final reports on scientific projects in the areas of biomechanics, coaching and development initiated by World Athletics, with help from the IAF (International Athletics Foundation)  |
| [Sports Analytics](https://www.ida.liu.se/research/sportsanalytics/resources/) | Resources for Sports Analytics from Linköping University|
| [Towards Data Science (Article)](https://towardsdatascience.com/implementing-real-time-object-detection-system-using-pytorch-and-opencv-70bac41148f7) | Implementing real time object detection system using pytorch and openCV. |
|[Detecting straight lines using Hough transform in Python (Video)](https://youtu.be/5zAT6yTHvP0?si=-rKqnaN4vGY5J-PU)|Youtube video. Could be useful to detect lanes|
|[Object Tracking from scratch with OpenCV and Python (Video)](https://youtu.be/GgGro5IV-cs?si=zSC2PTiJCVPXXYP3)|Could be used to track runners|
|[Dima Sports Hurdles](https://www.dimasport.fr/en/158-hurdles)|Dima catalog. Can be used to find hurdles dimensions|
|[AAE Sports Hurdles](https://www.aaesports.com/track-hurdles-s/170.htm)|AAE catalog. Can be used to find hurdles dimensions|
|[NordicSports Hurdles](https://nordicsport.se/en/collections/hurdles/Hurdles)|Nordic Sports. Can be used to find hurdles dimenions|
|[Gills Athletics hurdles](https://www.gillporter.com/gill_store/track-and-field-equipment.html#&cat=hurdles)|Gills. Can be used to find hurdles dimenions|

## Data:

| Report | Video |
|--------|-------|
|[Men's 110m hurdles - 2017 IAAF World Championships Biomechanical report](https://worldathletics.org/download/download?filename=e7427e94-e7b6-472b-bd67-a1f2d7307f88.pdf&urlslug=Men%27s%20110m%20hurdles%20-%202017%20IAAF%20World%20Championships%20Biomechanical%20report)|[video (final)](https://youtu.be/EyaDyJZU75M?si=-9lWBAwHFTz10bl2&t=266)|
|[Men’s 60m hurdles – 2018 IAAF Indoor Championships Biomechanical Report](https://worldathletics.org/download/download?filename=0d4bc5cd-4a8b-4faa-81e0-898e90a091c5.pdf&urlslug=Men%E2%80%99s%2060m%20hurdles%20%E2%80%93%202018%20IAAF%20Indoor%20Championships%20Biomechanical%20Report)|[video (final)](https://youtu.be/t0zF74w6GBs?si=Ckxd3IRuq0cGpHoz&t=300)|
|[Women’s 60m hurdles – 2018 IAAF Indoor Championships Biomechanical Report](https://worldathletics.org/download/download?filename=6a66447c-900f-49ff-9330-0d1c9d975dec.pdf&urlslug=Women%E2%80%99s%2060m%20hurdles%20%E2%80%93%202018%20IAAF%20Indoor%20Championships%20Biomechanical%20Report)|[video (final)](https://youtu.be/AqJjeyxf3mM?si=tyK0sUpBKd2ForXc&t=250)|
|[Biomechanics Report WC Berlin 2009 Hurdles Men](https://worldathletics.org/download/download?filename=afbf4956-27ef-452c-8af2-4040c6c7232a.pdf&urlslug=2%20-%20Biomechanics%20Report%20WC%20Berlin%202009%20Hurdles%20Men)|[video (final)](https://youtu.be/Nsp2U3rtCBQ?si=lwzs43lTvPojKdWk),[video (SF1/3)](https://youtu.be/WxXwmSye9SI?si=_gvnloWQ5p5UhBdR),[video (SF2/3)](https://youtu.be/_151EPRnpCg?si=IGczWYauEoFD7zwA), [video (SF3/3)](https://youtu.be/Y4Utfnu40GQ?si=RfwcRbNL82fnK6TI)|
|[]()|[video]()|
|[]()|[video]()|


## Brainstorming (using a LLM):

1. Lane Detection:

**Keywords**: centerline extraction, Hough transforms
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

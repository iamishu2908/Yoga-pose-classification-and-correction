## Workflow of pose detection and identification of wrong poses:

1. Mark necessary joints on input images with the help of Medipapipe library for images of all yoga types
https://ai.google.dev/edge/mediapipe/solutions/vision/pose_landmarker
2. The landmarks are coordinates of the joints of person in the image. Angles like 'left_elbow_angle','right_elbow_angle','left_shoulder_angle' can be found out using these coordinates.
3. the angles pertain to a certain yoga class and thus feed forward networks can be used to find patterns between hese angles and thus classify them
4. the model is trained to identify a yoga class depending on the 14 different angles from a yoga pose. The model achieved near 97.3% accuracy in classifying 5 yoga poses
thus,
input data: Image
processing: image -> landmarks -> angles
output data: yoga pose type
6. After classification of a yoga pose, the joints where there is a slight deviation from the joints for a correct yoga pose are identified and marked in the image for further correction of wrong yoga pose.

## Tech used:
TensorFlow, scikit learn, numpy , pandas, Mediapipe 

## References:

### Inspiration:

https://www.researchgate.net/publication/360950640_Yoga_Pose_Detection_and_Correction_using_Posenet_and_KNN

### Mediapipe library documentation:

https://ai.google.dev/edge/mediapipe/solutions/vision/pose_landmarker

### Other research papers:

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9623892/
https://ieeexplore.ieee.org/document/10104781

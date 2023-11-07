# Detection Files
Test results of excellent YOLOX detectors are used as detection files. Each row represents an object, and each row contains nine values. Examples of detection files are as follows:  
1, −1, 174, 243, 12, 12, 1, −1, −1, −1  
1, −1, 215, 326, 13, 14, 1, −1, −1, −1  
1, −1, 235, 167, 13, 14, 1, −1, −1, −1  
1, −1, 273, 250, 11, 12, 1, −1, −1, −1   
The first number indicates which frame the object appears in.   
The second number represents the ID of the object (set to ‘−1’ in the detection files, because the ID has not been assigned), by assigning a unique ID, each object can only be specified to a trajectory.   
The next four numbers represent the position of the UAV bounding box in the two-dimensional image coordinates, representing the upper left corner coordinates x, y and the width and height of the bounding box.   
The seventh number represents its confidence score.   
The last three digits of the detection files are represented as the ignored state (set to ‘−1’).  

# Annotation Files
Each row represents an object, and each row contains nine values. Examples of annotation files are as follows:  
1, 1, 352, 20, 11, 11, 1, 1, 1  
2, 1, 352, 20, 11, 11, 1, 1, 1  
3, 1, 352, 20, 11, 11, 1, 1, 1  
4, 1, 352, 20, 11, 11, 1, 1, 1  
The first six digital meanings are the same as the first six digital meanings of the test files.   
The seventh number represents the confidence score and serves as a symbol of whether input is considered (‘0’ means that this object is ignored in calculation, ‘1’ means that this object is marked as an activity, and this value is set to ‘1’ in annotation files).   
The eighth number represents the type of annotated object (since there is only one UAV category in this dataset, the values are set to ‘1’).   
The ninth number represents the visibility ratio of each bounding box, ranging from 0 to 1, which is judged by the occlusion degree of another static or moving object or by the clipping of image boundary (the value in annotation files is set to ‘1’).   

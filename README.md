# UAVSwarm-dataset
## Description:
UAVSwarm dataset was manually collected and annotated for UAV swarm detection and tracking, in which thirteen different scenes and more than nineteen types of UAV were recorded, including 12,598 annotated images—the number of UAV in each sequence is 3 to 23.
![Figure 1. Sample annotated images of the UAVSwarm dataset](https://github.com/UAVSwarm/UAVSwarm-dataset/assets/149923222/2a2eedcc-c06f-4a2b-b35f-f26ec6ae974e)
*Figure 1. Sample annotated images of the UAVSwarm dataset*
![Figure 2. Sample images of some UAV in the UAVSwarm dataset](https://github.com/UAVSwarm/UAVSwarm-dataset/assets/149923222/44f043a7-56c6-4872-917a-3a98916ad985)
*Figure 2. Sample images of some UAV in the UAVSwarm dataset*

## Motivation:
In recent years, with the rapid development of unmanned aerial vehicles (UAV) technology and swarm intelligence technology, hundreds of small-scale and low-cost UAV constitute swarms carry out complex combat tasks in the form of ad hoc networks, which brings great threats and challenges to low-altitude airspace defense. Security requirements for low-altitude airspace defense, using visual detection technology to detect and track incoming UAV swarms, is the premise of anti-UAV strategy. Therefore, this study first collected many UAV swarm videos and manually annotated a dataset named UAVSwarm dataset for UAV swarm detection and tracking; thirteen different scenes and more than nineteen types of UAV were recorded, including 12,598 annotated images—the number of UAV in each sequence is 3 to 23. Then, some state-of-the-art multi-object tracking (MOT) models are used to conduct comprehensive tests and performance verification on the dataset and evaluation metrics. The experimental results show that the dataset has good availability, consistency, and universality. The UAVSwarm dataset can be widely used in training and testing of various UAV detection tasks and UAV swarm MOT tasks.

## Detection Files：
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

## Annotation Files：
Each row represents an object, and each row contains nine values. Examples of annotation files are as follows:  
1, 1, 352, 20, 11, 11, 1, 1, 1  
2, 1, 352, 20, 11, 11, 1, 1, 1  
3, 1, 352, 20, 11, 11, 1, 1, 1  
4, 1, 352, 20, 11, 11, 1, 1, 1  
The first six digital meanings are the same as the first six digital meanings of the test files.   
The seventh number represents the confidence score and serves as a symbol of whether input is considered (‘0’ means that this object is ignored in calculation, ‘1’ means that this object is marked as an activity, and this value is set to ‘1’ in annotation files).   
The eighth number represents the type of annotated object (since there is only one UAV category in this dataset, the values are set to ‘1’).   
The ninth number represents the visibility ratio of each bounding box, ranging from 0 to 1, which is judged by the occlusion degree of another static or moving object or by the clipping of image boundary (the value in annotation files is set to ‘1’).   
## Authors:
Chuanyun Wang;  
Yang Su;   
Qian Gao;   
Linlin Meng; et al.
## Citation:
1. [Chuanyun Wang; Yang Su; Jingjing Wang; et al. UAVSwarm Dataset: An Unmanned Aerial Vehicle Swarm Dataset for Multiple Object Tracking. Remote Sensing. 2022, 14, 2601.](https://www.mdpi.com/2072-4292/14/11/2601)
2. [Chuanyun Wang; Linlin Meng; Qian Gao; et al. A Lightweight UAV Swarm Detection Method Integrated Attention Mechanism. Drones 2023, 7, 13.](https://www.mdpi.com/2504-446X/7/1/13)
3. [Chuanyun Wang; Yang Su; Linlin Wang; et al. Multiple object continuous robust tracking algorithm for Anti-UAV swarm.Acta Aeronautica et Astronautica Sinica, doi: 10.7527/S1000-6893.2023.29017(in Chinese).](https://hkxb.buaa.edu.cn/CN/10.7527/S1000-6893.2023.29017)

---
title: "Dataset info"
permalink: /datasetinfo/
layout: home
summary: "Information about data usage, data and labeling"
---
### <a id="Data_Usage" class="uncolored_link">Data Usage</a>
By **registering** in the challenge, each team agrees (1) to use the data provided only in the
scope of the challenge and (2) to neither pass it on to a third party nor to use it for any additional publication or for commercial use. 

After the challenge, the data will be made publicy available for non-commercial use (CC BY NC SA). 
An **embargo period** until the availability of the planned journal paper will be put in place.

### <a id="Data" class="uncolored_link">Data</a>

Mitral valve repair is a heart surgery, which is aimed at re-storing the function of the mitral valve. During the surgery, the valve is not replaced but an annoloplasty ring is inserted to stabilize the mitral annulus. The prosthetic ring is anchored by white and blue matress sutures stitched in a particular pattern into the annulus. 
The goal of this challenge is to detect the points where these sutures enter or exit the tissue before the ring is sewed. 

The challenge cohort splits into two endoscopic sets:
1. data acquired during simulating mitral valve repair on a surgical simulator ("Sim-Domain“),
2. intraoperative endoscopic data from real minimally invasive mitral valve repair ("Intraop-Domain").

<u>Training Sim-Domain:</u>  
2708 mono frames from 10 simulations (192-374 frames each) with approx. 33500 annotated landmarks.

<u>Training Intraop-Domain:</u>  
2376 mono frames from 4 patients (372-794 frames each) with almost 24000 annotated landmarks.

<u>Testing Intraop-Domain:</u>  
500 mono frames from 5 patients (100 frames from each). Patients are different from the training set.

The idea behind the challenge is to keep the number of intraoperative patients low to force participants to incorporate the frames from Sim-Domain in the training process to achieve better generalization performance.


Besides the frames themselves, we release to which (anonymized) patient and domain the frame belongs to. Additionally, for the training set, the image coordinates of the target landmarks are provided. Image format varied and was reduced to 512 x 288 to reduce storage and computational costs.

The number of frames per simulation/patient in the training data set are not equal, but are on the same scale. We balanced the number of frames per patient in the test data. Therefore, each patient in the test set has a similar influence on the final score.

### <a id="Labeling" class="uncolored_link">Labeling</a>

Annotating the frames is not trivial due to the thin nature of these sutures, heavy occlusions by instruments, self-occlussions, color changes on the sutures (they turn red during the surgery) and blood in the scene. 
The ground truth was produced by two students with basic knowledge of the surgical steps. They both followed a pre-defined labeling strategy and used the software „[label me](https://github.com/wkentaro/labelme)“.  
Training set: Annotations were additionally checked by two other experts and unclear cases where discussed until a consenus could be reached.
Test set: Annotations were made by student1 and student2 independently and the mean was computed to determine the final landmark position. Annotations were additionally checked by two other experts and unclear cases where discussed until a consenus could be reached.

The annotation was conducted in temporal order on the stereo images. More information about the labeling strategy can be found <a href="/assets/files/Labeln_ENG-v1.pdf">here</a>.

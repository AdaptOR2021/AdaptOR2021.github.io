---
permalink: /submissiondetails/
title: "Submission details"
layout: home
summary: "Information about the submission and the evaluation"
---
## Submission
For the purpose of result verification and to encourage reproducibility and transparency, all entries must submit the following:

- **Docker container on the Synapse platform**. More information and links will be provided soon.

    - (Mandatory:) When running a pre-defined command on novel input data of size 512x288 from the Intraop-Domain, the model should output a **JSON file**, which should include the input file name and a list of the x- and y-coordinates of the detected landmarks.

    - (Optional:) When running a pre-defined command on a Sim-Domain image, the model should output an image, which was **transformed** into the Intraop-Domain and vice versa. These results do not play a role in the final rankings, but should provide insights on the quality of image-to-image transformation. Example images will be shown during the workshop event and in the joint publication. Depending on the number of submissions, an additional user-study with domain experts might be conducted at a later stage.

Teams are encouraged to provide their code open source and to add the URL in the LNCS paper.  
Participants agree that the challenge organizers are allowed to use their submitted docker containers to run further meta-analysis.


The challenge will be split into **three phases**: Training phase, Platform testing phase, Testing phase.

During **training phase**, the participating teams will be able to independently validate their results using crossvalidation on the training data.

During the platform **testing phase**, they are allowed to use the official submission platform to resolve potential technical issues. We will use dummy datasets for sanity checks, e.g. to ensure the submission is in the correctformat.

During the **test phase**, participants are allowed to make in total three submissions. The best result out of these three is selected as final result.

<img src="/assets/images/submission_details.png">

### Evaluation

#### Metrics And Reporting

We will make the code available on the synapse platform that will be used to compute the metrics for ranking.

We will report **true positives**, **false positives** and **false negatives**.
A landmark is counted as true positive, if it lies within a radius of 6 pixels around the manually labeled point, same as in [4]. This accounts for the fact that the region, where the suture enters or exits the tissue, is usually a small region and not just a single pixel. Finally, we report **sensitivity/recall** (TPR) and **precision** (PPV).

#### Ranking
Precision and Recall are computed over all landmarks in the test sets. It is not differentiated whether the prediction is particulary well for certain frames/patients/simulations and worse for others.  
The traditional F-score or **balanced F-score** (F1 score) presents the harmonic mean of precision and recall and will be used to determine the ranking (the higher the better).
We exclude false negative rate (FNR) in the ranking, since it is related to TPR by TPR = 1-FNR. In the case where all metrics are tied, we will accept to have multiple teams with the same ranking.

#### Result announcement
All the results will be made available publicly. The announcement of the winner will be made at the workshop and the website will be updated accordingly. 
All teams should participate in the workshop and will be invited to present their work in more detail, which we hope will foster detailed discussions. In case of a virtual event, we will seek for providing discussion opportunities in small groups.

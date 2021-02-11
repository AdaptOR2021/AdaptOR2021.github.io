---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
author_profile: true
---
## AdaptOR: Deep Generative Model Challenge for Domain Adaptation in Surgery
<img src="/resources/AdaptOR.png" width="200">

### Challenge Abstract 

Mitral regurgitation (MR) is the second most frequent indication for valve surgery in Europe and may occur for organic or functional causes [1]. Mitral valve repair, although considerably more difficult, is preferred over mitral valve replacement, since the native tissue of the valve is preserved.
However, it is a difficult and experience-based on-pump heart surgery, often conducted only by a handful of surgeons in high-volume centers. 
Minimally invasive procedures, which are accompanied by endoscopic video recordings, have become more and more popular in recent years. However, data availability and data privacy concerns are still an issue for the development of automatic scene analysis algorithms. The AdaptOR challenge aims to address these issues by formulating a domain adaptation problem “from simulation to surgery“: We provide a smaller number of datasets from real surgeries, and a larger number of annotated recordings of training and planning sessions from a physical mitral valve simulator. The goal is to reduce the considerable domain gap between simulation and intraoperative cases, e.g. by incorporating popular generative models, as in [2,3]. 
The task associated with the domain adaptation itself is to detect 2D landmarks with varying number of landmarks per frame in the target domain. The landmarks are defined by the placement of sutures during mitral annuloplasty (entry and exit points in the tissue), which renders useful for surgical skill assessment and detailed intraoperative documentation. Besides, the AdaptOR challenge provides a framework for comparison of the performance of different generative approaches, which need to learn how to successfully transform the scenes into an intraoperative appearance, thereby not altering already realistic parts of the image (surgical instruments, sutures, needles etc.). While this can be merely assessed visually, we hypothesize that the success of landmark detection may be an indicator for the quality of the transfer with respect to the consistency of sutures in both domains.


### Schedule

- Release date of the training cases: 01/04/2021
- Registration date: until 30/05/2021
- Platform testing: 1/06/2021-15/06/2021
- Submission of docker container: 15/06/2021-07/07/2021
- LNCS paper submission date: 15/07/2021
- Associated workshop days: (TBA)
- Release date of the results: (TBA)


### Organizers

- Jun. Prof. Dr. Sandy Engelhardt, University Hospital Heidelberg
- Dr. Anirban Mukhopadhyay, Technical University Darmstadt
- Prof. Dr. Raffaele De Simone, University Hospital Heidelberg
- Lalith Sharan, University Hospital Heidelberg
- Antonia Stern, University Hospital Heidelberg
- Julian Brand, University Hospital Heidelberg
- Henry Krumb, Technical University Darmstadt

### Labeling Strategy

Details on the Labeling Strategy can be found [here](https://github.com/AdaptOR2021/adaptor2021.github.io/blob/master/resources/Labeln_ENG-v1.pdf)

### References

[1] https://www.escardio.org/Journals/E-Journal-of-Cardiology-Practice/Volume-16/Mitral-valve-incompetence-epidemiology-and-causes

[2] Engelhardt S., De Simone R., Full P.M., Karck M., Wolf I. (2018) Improving Surgical Training Phantoms by Hyperrealism: Deep Unpaired Image-to-Image Translation from Real Surgeries. In: Frangi A., Schnabel J., Davatzikos C., Alberola-López C., Fichtinger G. (eds) Medical Image Computing and Computer Assisted Intervention – MICCAI 2018. MICCAI 2018. Lecture Notes in Computer Science, vol 11070. Springer, Cham, doi: 10.1007/978-3-030-00928-1_84

[3] Engelhardt, S., Sharan, L., Karck, M., De Simone, R., Wolf, I. (2019), Cross-Domain Conditional Generative Adversarial Networks for Stereoscopic Hyperrealism in Surgical Training. In: Shen D. et al. (eds) Medical Image Computing and Computer Assisted Intervention – MICCAI 2019. MICCAI 2019. Lecture Notes in Computer Science, vol 11768. Springer, Cham, pp 155-163, doi: https://doi.org/10.1007/978-3-030-32254-0_18

[4] Antonia Stern, Lalith Sharan, Gabriele Romano, Sven Koehler, Matthias Karck, Raffaele De Simone, Ivo Wolf, Sandy Engelhardt, Heatmap-based 2D Landmark Detection with a Varying Number of Landmarks, Bildverarbeitung für die Medizin, 2021 (accepted)

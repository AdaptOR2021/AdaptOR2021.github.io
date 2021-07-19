---
title: "Publications"
permalink: /publications/
layout: home
summary: "Publications"
---

<h2 class="divider">Papers about the same task by the organisers:</h2>

<h3><a id="Mutually_improved_endoscopic_image_synthesis_and_landmark_detection_in_unpaired_image-to-image_translation" class="uncolored_link">Mutually improved endoscopic image synthesis and landmark detection in unpaired image-to-image translation</a></h3>
<i>14 Jul 2021</i>  
Lalith Sharan, Gabriele Romano, Sven Koehler, Halvar Kelm, Matthias Karck, Raffaele De Simone, Sandy Engelhardt

<div class="centered">
      <a href="https://arxiv.org/pdf/2107.06941">
            <img src="/assets/images/Mutually_improved_endoscopic_image_synthesisand_landmark_detectionin_unpaired_image-to-image_translation-cover.png" srcset="/assets/images/Mutually_improved_endoscopic_image_synthesisand_landmark_detectionin_unpaired_image-to-image_translation-cover.png 1224w, /assets/images/Mutually_improved_endoscopic_image_synthesisand_landmark_detectionin_unpaired_image-to-image_translation-cover-medium.png 808w, /assets/images/Mutually_improved_endoscopic_image_synthesisand_landmark_detectionin_unpaired_image-to-image_translation-cover-small.png 404w, /assets/images/Mutually_improved_endoscopic_image_synthesisand_landmark_detectionin_unpaired_image-to-image_translation-cover-mini.png 122w" sizes="10vw" style="border: 1px solid">
      </a>
</div>

##### Abstract:
<div class="smaller-text">
The CycleGAN framework allows for unsupervised image-to-image translation of unpaired data. In a scenario of surgical training on a physical surgical simulator, this method can be used to transform endoscopic images of phantoms into images which more closely resemble the intra-operative appearance of the same surgical target structure. This can be viewed as a novel augmented reality approach, which we coined Hyperrealism in previous work. In this use case, it is of paramount importance to display objects like needles, sutures or instruments consistent in both domains while altering the style to a more tissue-like appearance. Segmentation of these objects would allow for a direct transfer, however, contouring of these, partly tiny and thin foreground objects is cumbersome and perhaps inaccurate. Instead, we propose to use landmark detection on the points when sutures pass into the tissue. This objective is directly incorporated into a CycleGAN framework by treating the performance of pre-trained detector models as an additional optimization goal. We show that a task defined on these sparse landmark labels improves consistency of synthesis by the generator network in both domains. Comparing a baseline CycleGAN architecture to our proposed extension (DetCycleGAN), mean precision (PPV) improved by +61.32, mean sensitivity (TPR) by +37.91, and mean F1 score by +0.4743. Furthermore, it could be shown that by dataset fusion, generated intra-operative images can be leveraged as additional training data for the detection network itself. The data is released within the scope of the AdaptOR MICCAI Challenge 2021 at <a href="https://adaptor2021.github.io/">https://adaptor2021.github.io/</a>, and code at <a href="https://github.com/Cardio-AI/detcyclegan_pytorch">https://github.com/Cardio-AI/detcyclegan_pytorch</a>. 
</div>

##### Link: 
[https://arxiv.org/abs/2107.06941](https://arxiv.org/abs/2107.06941)

##### Bibtex citation:
```
@misc{sharan2021mutually,
      title={Mutually improved endoscopic image synthesis and landmark detection in unpaired image-to-image translation}, 
      author={Lalith Sharan and Gabriele Romano and Sven Koehler and Halvar Kelm and Matthias Karck and Raffaele De Simone and Sandy Engelhardt},
      year={2021},
      eprint={2107.06941},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```
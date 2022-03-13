---
permalink: /index.html
layout: home
author_profile: true
title: "AdaptOR: Deep Image Generation Model Challenge in Surgery"
classes: wide
image: /assets/images/AdaptOR.png
sidebar:
  true
---
{% seo %}

<div class="centered">
  <img class="centered-image" src="/assets/images/SignatureImage.jpg" alt="Signature Image" srcset="/assets/images/SignatureImage.jpg 1541w, /assets/images/SignatureImage-medium.jpg 1017w, /assets/images/SignatureImage-small.jpg 509w, /assets/images/SignatureImage-mini.jpg 154w" sizes="50vw">
</div>

<p style="padding: 10px; border: 2px solid red;">
<b> +++ Website under construction. Not all information is updated +++ </b><br> </p>

### <a id="News" class="uncolored_link">News </a>
<ul>
<li> March 13th, 2022 - The 2nd Edition of the AdaptOR challenge will be held in conjunction with MICCAI 2022!
</div>
</ul>

### <a id="Challenge_Abstract" class="uncolored_link">Challenge Abstract </a>
Mitral regurgitation (MR) is the second most frequent indication for valve surgery in Europe and may occur for organic or functional causes [[1](#1)]. Mitral valve repair, although considerably more difficult, is prefered over mitral valve replacement, since the native tissue of the valve is preserved. It is a complex on-pump heart surgery, often conducted only by a handful of surgeons in high-volume centers. Minimally invasive procedures, which are performed with endoscopic video recordings, became more and more popular in recent years. However, data availability and data privacy concerns are still an issue for the development of automatic scene analysis algorithms. The AdaptOR challenge aims to address these issues by formulating a domain adaptation problem „from simulation to surgery“: We provide a smaller number of datasets from real surgeries, and a larger number of annotated recordings of training and planning sessions from a physical mitral valve simulator. The goal is to reduce the considerable domain gap between simulation and intraoperative cases, e.g. by incorporating generative models, as in [[2](#2),[3](#3)].

The task associated to the domain adaptation itself is to detect a varying number of 2D landmarks per frame [[4](#4)] in the target domain. The landmarks are defined by the placement of sutures during mitral annuloplasty (entry and exit points into the tissue), which renders useful for surgical skill assessment and detailed intraoperative documentation. The evaluation metrics of this challenge will be related to how well these points could be identified in unseen intraoperative scenes, therefore it is also possible to only come up with a solution to a landmark detection problem in a single domain. More complex methods, however, would leverage data from both domains and adapt them on input-, output-, and/or feature level. Due to the specific clinical motivation of improving the realism of surgical simulation [[2](#2),[3](#3)], the AdaptOR challenge especially aims to provide a framework for comparison of the performance of different image-to-image translation approaches. Such approaches need to learn how to sucessfully transform the images into an intraoperative appearance, thereby not altering already realistic entities of the image (surgical instruments, sutures, needles etc.). While this can be merely assessed visually, and we will show example results during the workshop, we hypothesize that the success of landmark detection may be an indicator for the quality of the transfer with respect to the consistency of sutures in both domains.


### <a id="More_Background" class="uncolored_link">More Background </a>
In our surgical training scenario, there is a clinical need for transforming not-so-realistic phantom data into more realistic surgical images [[2](#2),[3](#3)]. Therefore, we encourage the participants to use image-to-image translation approaches, however, this is not mandatory.  
In general, we think the underlying detection task could be solved differently:

1. Training of a landmark detection approach only on the intraoperative domain
2. Using the simulation domain for pre-training/dataset fusion
3. Incorporating the simulation domain by using a combination of more advanced input-, output-, feature-level domain adaptation approaches, possibly in an end-to-end training strategy
4. Others.

<span style="color:#B6B6B4">The authors should detail on their approaches in their submitted LNCS papers.</span><br>
In case an image-to-image translation task was solved, we will provide visual examples of the generative model's output for visual comparison. These results are qualitative and will not be considered in the ranking scheme. We hypothesize that the quantitative assessment for landmark detection may be an indicator for the quality of the domain transfer with respect to the consistency of sutures in both domains.

<div class="centered"><img src="/assets/images/example-medium.gif" srcset="/assets/images/example-medium.gif 1014w, /assets/images/example-small.gif 507w, /assets/images/example-mini.gif 154w" sizes="50vw"></div>
*Figure 1. Example of domain transfer done with tempCycleGAN from [[2](#2)]. Left: Original video from a simulator. Center: Frames transformed into intraoperative appearance. Right: Backtransformed video frames.*

### <a id="Challenge_Document" class="uncolored_link">Challenge Document</a>

DOI <a href="https://zenodo.org/record/4646979#.YGMXXD9CQ2w">10.5281/zenodo.4646979 (v2)</a>

### <a id="Keywords" class="uncolored_link">Keywords</a>
<div class="smaller-text">
Domain Adaptation, Generative Models, Landmark Detection, Deep Learning, Machine Learning
</div>

### <a id="References" class="uncolored_link">References</a>
<div class="smaller-text">
[<a id="1">1</a>] <a href="https://www.escardio.org/Journals/E-Journal-of-Cardiology-Practice/Volume-16/Mitral-valve-incompetence-epidemiology-and-causes">https://www.escardio.org/Journals/E-Journal-of-Cardiology-Practice/Volume-16/Mitral-valve-incompetence-epidemiology-and-causes</a><br><br>

[<a id="2">2</a>] Engelhardt S., De Simone R., Full P.M., Karck M., Wolf I. (2018) Improving Surgical Training Phantoms by Hyperrealism: Deep Unpaired Image-to-Image Translation from Real Surgeries. In: Frangi A., Schnabel J., Davatzikos C., Alberola-López C., Fichtinger G. (eds) Medical Image Computing and Computer Assisted Intervention – MICCAI 2018. MICCAI 2018. Lecture Notes in Computer Science, vol 11070. Springer, Cham, doi: <a href="https://doi.org/10.1007/978-3-030-00928-1_84">10.1007/978-3-030-00928-1_84</a> Preprint: <a href="https://arxiv.org/abs/1806.03627">1806.03627</a><br><br>

[<a id="3">3</a>] Engelhardt, S., Sharan, L., Karck, M., De Simone, R., Wolf, I. (2019), Cross-Domain Conditional Generative Adversarial Networks for Stereoscopic Hyperrealism in Surgical Training. In: Shen D. et al. (eds) Medical Image Computing and Computer Assisted Intervention – MICCAI 2019. MICCAI 2019. Lecture Notes in Computer Science, vol 11768. Springer, Cham, pp 155-163, doi: <a href="https://doi.org/10.1007/978-3-030-32254-0_18">https://doi.org/10.1007/978-3-030-32254-0_18</a> Preprint: <a href="https://arxiv.org/abs/1906.10011">1906.10011</a> <br><br>

[<a id="4">4</a>] Stern, A., Sharan, L., Romano, G., Koehler, S., Karck, M., De Simone, R., Wolf, I., Engelhardt, S. (2021), Heatmap-based 2D Landmark Detection with a Varying Number of Landmarks. In: Palm C., Deserno T.M., Handels H., Maier A., Maier-Hein K., Tolxdorff T. (eds) Bildverarbeitung für die Medizin 2021. Informatik aktuell. Springer Vieweg, Wiesbaden. <a href="https://doi.org/10.1007/978-3-658-33198-6_7">https://doi.org/10.1007/978-3-658-33198-6_7</a>
Preprint: <a href="https://arxiv.org/abs/2101.02737">2101.02737</a>
</div>

### <a id="Rules" class="uncolored_link">Rules</a>
- Only fully automatic approaches are allowed
- No additional training data and no models pre-trained on other datasets are allowed.
- Each team is only allowed to register once and all submissions must be done from the same account.
- A single participant is only allowed to be part of one team.
- The participants agree to participate in a challenge publication that will be planned by the organisers once a sufficient number of submissions are received.<br>
<span style="color:#B6B6B4">Participating teams must submit a LNCS paper with comprehensive descriptions of their methods via CMT one week after docker container submission deadline. Failure of submitting the paper will render the submission invalid.</span>

### <a id="Prizes" class="uncolored_link">Prizes</a>
The 1st Prize for the AdaptOR challenge was bagged by team <b>LS_Group</b> comprising of Jiacheng Wang, Haojie Wang, Ruochen Mu, and Liansheng Wang from Xiamen University, China. 
Their submission titled <b> Cross-Domain Landmarks Detection in Mitral Regurgitation </b> can be found <a href="https://link.springer.com/chapter/10.1007/978-3-030-88210-5_12">here</a>.
The 2nd Prize was won by Team Neko, comprising of Huifeng Yao, Ziyu Guo, Yatao Zhang, and Liansheng Wang from Shangdong University China, and Hongkong University.
Their submission titled <b> Improved Heatmap-Based Landmark Detection </b> can be found <a href="https://link.springer.com/chapter/10.1007/978-3-030-88210-5_11">here</a>.

The two top performing teams received certificates and prize money of 600€ and 400€ for the first and second place respectively. The awards are generously sponsored by [Fehling Instruments GmbH & Co. KG](https://www.fehling-instruments.de).
<div class="centered" ><a href="https://www.fehling-instruments.de"><img style="width:15vw" src="/assets/images/FI-KG_logo.jpg" srcset="/assets/images/FI-KG_logo.jpg 3779w, /assets/images/FI-KG_logo-medium.jpg 2494w, /assets/images/FI-KG_logo-small.jpg 1247w, /assets/images/FI-KG_logo-mini.jpg 378w" sizes="50vw"></a></div>

### <a id="Potential_Future_Plans" class="uncolored_link">Potential Future Plans</a>
Our envisioned goal is to extend the dataset with additional cases and potentially establish a recurring AdaptOR event to support progress in this application field.  
In 2022, we would like to focus on stereo tasks and method generalization.

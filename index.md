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

The continuing AdaptOR Challenge aims to spark methodological developments in deep image generation models
for the surgical domain. In this year’s edition, we again focus on video-assisted mitral valve repair [1](#1), which is
becoming the novel state-of-the art [2](#2). Especially the usage of 3D endoscopes, where data is captured with a left
and right camera and presented on a 3D-compatible monitor, has been proven very beneficial due to increased
depth perception. Moreover, it is possible when post processing to perform quantitative analyses by exploiting the
stereo relation.
Towards this end, and building upon the challenge in the previous year [7](#7), the AdaptOR Challenge 2022 proposes
a task of novel view synthesis for endoscopic data. During training, the participants are provided the left and the
right stereo camera images, and the test time task is to predict the corresponding image for a given image from the
left camera. This would serve the purposes of facilitating 3D perception when only 2D data is available and of
providing relevant information for depth reconstruction, as novel view synthesis is an integral subtask of
numerous existing cutting edge depth estimation methods [[5](#5),[6](#6)].
Intraoperative data sets in this challenge have varying camera angles, illumination, field of views and occlusions
from tissues, tubes, and increased light reflections from surgical headlights. Especially demanding in these scenes is
the view-dependent appearance of objects that are directly in front of the camera (e.g., sutures). They render it
difficult to train models that faithfully predict the missing image from the image pair or to define the correct
correspondences between associated pixels. Therefore, the proposed task of novel view synthesis is difficult to
solve.
To enhance the training split with data from a related domain, we additionally provide stereo frames from a mitral
valve surgical simulator. These frames have comparably stable illumination (less varying reflections) and a more
standardized view angle. Participants are invited to include a domain adaptation approach (e.g.,[8](#8)) into their
solution.
The dataset this year is an extension of our dataset we released in the previous year, where we now consider more
surgeries and additional phases of mitral valve repair to significantly increase the sizes of the single splits at higher resolutions.



### <a id="Challenge_Document" class="uncolored_link">Challenge Document</a>

--DOI <a href="https://zenodo.org/record/4646979#.YGMXXD9CQ2w">10.5281/zenodo.4646979 (v2)</a>

### <a id="Keywords" class="uncolored_link">Keywords</a>
<div class="smaller-text">
Novel View Synthesis, Stereo, Domain Adaptation, Generative Models, Deep Learning, Machine Learning
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

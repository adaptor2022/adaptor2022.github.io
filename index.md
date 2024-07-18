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

{% capture notice-close %} 
### ++ AdaptOR 2022 challenge is closed and the datasets are no longer available through this platform ++
{: style="text-align: center; background-color: red;"}
{% endcapture %}

<div class="notice" style="background-color: #ffcccc;">{{ notice-close | markdownify }}</div>

<div class="centered">
  <img class="centered-image" src="/assets/images/SignatureImage.jpg" alt="Signature Image" srcset="/assets/images/SignatureImage.jpg 1541w, /assets/images/SignatureImage-medium.jpg 1017w, /assets/images/SignatureImage-small.jpg 509w, /assets/images/SignatureImage-mini.jpg 154w" sizes="50vw">
</div>

[//]: # {% capture notice-1 %} 
[//]: # ### ++ AdaptOR 2022 challenge submission system is now open! ++
[//]: # {: style="text-align: center;"}

[//]: # More info [here](https://www.synapse.org/#!Synapse:syn29340309/wiki/617629)
[//]: # {: style="text-align: center;"}

[//]: # [Submit](https://www.synapse.org/#!Synapse:syn29340309/challenge/){: .btn .btn--info .btn--large}
[//]: # {: style="text-align: center;"}
[//]: # {% endcapture %}

[//]: # {% capture notice-3 %} 
[//]: # ### ++ AdaptOR 2022 platform testing phase is open ++
[//]: # {: style="text-align: center;"}

[//]: # You can now submit your docker containers to test the submission process. More info [here](https://www.synapse.org/#!Synapse:syn29340309/wiki/617629)
[//]: # {: style="text-align: center;"}
[//]: # {% endcapture %}

{% capture notice-2 %} 
### ++ Important announcement on the released training data (Updated June 2nd, 2022) ++ 
A small number of the sub-folders (7 out of 64) have the images of the left and right camera switched. This 
issue has now been fixed on synapse. Please run the ```download_files.py``` script on synapse again - this will download 
and replace only the changed files onto your system.
{% endcapture %}

<div class="notice">{{ notice-2 | markdownify }}</div>

### <a id="News" class="uncolored_link">News </a>
<ul>
<li> April 15th, 2022  - The AdaptOR challenge 2022 is now open! Please follow our <a href="https://adaptor2022.github.io/registration/">steps for registration</a>, and also check out details about the <a href="https://adaptor2022.github.io/submissiondetails/">submission</a>. </li>
<li> April 1st, 2022  - The AdaptOR challenge will be associated to the <a href="https://dgm4miccai.github.io/">DGM4MICCAI workshop</a> 2022! </li>
<li> March 13th, 2022 - The 2nd Edition of the AdaptOR challenge will be held in conjunction with MICCAI 2022!</li>
</ul>

### <a id="Timeline" class="uncolored_link">Timeline </a>

Next upcoming important dates:
<ul>
<li> July 01st, 2022  - Platform testing phase opens </li>
<li> July 15th, 2022  - Submission system opens </li>
</ul>
View the complete timeline [here](/timeline/). 


### <a id="Challenge_Abstract" class="uncolored_link">Challenge Abstract </a>

The continuing AdaptOR Challenge aims to spark methodological developments in deep image generation models
for the surgical domain. In this year’s edition, we again focus on video-assisted mitral valve repair [[1](#1)], which is
becoming the novel state-of-the art [[2](#2)]. Especially the usage of 3D endoscopes, where data is captured with a left
and right camera and presented on a 3D-compatible monitor, has been proven very beneficial due to increased
depth perception. Moreover, it is possible when post processing to perform quantitative analyses by exploiting the
stereo relation.

Towards this end, and building upon the challenge in the previous year [[7](#7)], the AdaptOR Challenge 2022 proposes
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
standardized view angle. Participants are invited to include a domain adaptation approach (e.g.,[[3](#3)],[[4](#4)],[[8](#8)]) into their
solution.

The dataset this year is an extension of our dataset we released in the previous year, where we now consider more
surgeries and additional phases of mitral valve repair to significantly increase the sizes of the single splits at higher resolutions.


### <a id="Challenge_Document" class="uncolored_link">Challenge Document</a>

DOI <a href="https://zenodo.org/record/6362269#.YnvK-SNBzmg">10.5281/zenodo.6362269</a>

### <a id="Keywords" class="uncolored_link">Keywords</a>
<div class="smaller-text">
Novel view synthesis, Image reconstruction, Image generation, Image synthesis, Generative models, Generative Adversarial Networks, Image transformation, Mitral Valve, Heart Valve, 3D Endoscopy, Surgical Training, Surgical Simulation
</div>

### <a id="References" class="uncolored_link">References</a>
<div class="smaller-text">

[<a id="1">1</a>]  Carpentier, A., Deloche, A., Dauptain, J., Soyer, R., Blondeau, P., Piwnica, A., Dubost,C., McGoon, D.C.: A new
reconstructive operation for correction of mitral and tricuspid
insufficiency. The Journal of Thoracic and Cardiovascular Surgery 61 (1), 1–13 (1971)<br><br>
  
[<a id="2">2</a>]  Casselman Filip P., Van Slycke Sam, Wellens Francis,
De Geest Raphael, Degrieck Ivan,Van Praet Frank, Vermeulen Yvette, Vanermen Hugo: Mitral Valve Surgery
Can Now Routinely Be Performed Endoscopically. Circulation 108 (10 suppl 1), II–48 (2003). <br><br>
  
[<a id="3">3</a>]  Sharan, L., Romano, G., Koehler, S., Karck, M., De Simone, R., Engelhardt, S.,
Mutually improved endoscopic image synthesis and landmark detection in  unpaired image-to-image translation. IEEE Journal of Biomedical and Health Informatics, 26(1), 2022, Pages 127 – 138, 10.1109/JBHI.2021.3099858. https://arxiv.org/abs/2107.06941 <br><br>
  
[<a id="4">4</a>]   Engelhardt, S., Sharan, L., Karck, M., De Simone, R., Wolf, I., Cross-Domain Conditional Generative Adversarial Networks for Stereoscopic Hyperrealism in Surgical Training. In: Shen D. et al. (eds) Medical Image Computing and Computer Assisted Intervention – MICCAI 2019. MICCAI 2019. Lecture Notes in Computer Science, vol 11768. Springer, Cham, pp 155-163, doi: https://doi.org/10.1007/978-3-030-32254-0_18, https://arxiv.org/abs/1906.10011 <br><br>
  
[<a id="5">5</a>] Watson, J., Mac Aodha, O., Turmukhambetov, D., Brostow, G. J., & Firman, M. (2020). Learning Stereo from
Single Images. ArXiv:2008.01484 [Cs]. http://arxiv.org/abs/2008.01484 <br><br>
  
[<a id="6">6</a>] Hou, Y., Solin, A., & Kannala, J. (2021). Novel View Synthesis via Depth-guided Skip Connections.
ArXiv:2101.01619 [Cs]. http://arxiv.org/abs/2101.01619 <br><br>
  
[<a id="7">7</a>] https://adaptor2021.github.io/ doi: 10.5281/zenodo.4646979 <br><br>
  
[<a id="8">8</a>] Engelhardt S., De Simone R., Full P.M., Karck M., Wolf I. (2018) Improving Surgical Training Phantoms by
Hyperrealism: Deep Unpaired Image-to-Image Translation from Real Surgeries. In: Frangi A., Schnabel J.,
Davatzikos C., Alberola-López C., Fichtinger G. (eds) Medical Image Computing and Computer Assisted
Intervention – MICCAI 2018. MICCAI 2018. Lecture Notes in Computer Science, vol 11070. Springer, Cham, doi:
10.1007/978-3-030-00928-1_84<br><br>
  
</div>

### <a id="Rules" class="uncolored_link">Rules</a>
- No additional training data and no models pre-trained on other datasets are allowed.
- Each team is only allowed to register once and all submissions must be done from the same account.
- A single participant is only allowed to be part of one team.
- The participants agree to participate in a challenge publication that will be planned by the organisers once a sufficient number of submissions are received.<br>

### <a id="Prizes" class="uncolored_link">Prizes</a>
Details about potential prizes will be announced in the future. Certificates will be provided for the top 3 performing teams.

<!--- The 1st Prize for the AdaptOR challenge was bagged by team <b>LS_Group</b> comprising of Jiacheng Wang, Haojie Wang, Ruochen Mu, and Liansheng Wang from Xiamen University, China. 
Their submission titled <b> Cross-Domain Landmarks Detection in Mitral Regurgitation </b> can be found <a href="https://link.springer.com/chapter/10.1007/978-3-030-88210-5_12">here</a>.
The 2nd Prize was won by Team Neko, comprising of Huifeng Yao, Ziyu Guo, Yatao Zhang, and Liansheng Wang from Shangdong University China, and Hongkong University.
Their submission titled <b> Improved Heatmap-Based Landmark Detection </b> can be found <a href="https://link.springer.com/chapter/10.1007/978-3-030-88210-5_11">here</a>.

The two top performing teams received certificates and prize money of 600€ and 400€ for the first and second place respectively. The awards are generously sponsored by [Fehling Instruments GmbH & Co. KG](https://www.fehling-instruments.de).
<div class="centered" ><a href="https://www.fehling-instruments.de"><img style="width:15vw" src="/assets/images/FI-KG_logo.jpg" srcset="/assets/images/FI-KG_logo.jpg 3779w, /assets/images/FI-KG_logo-medium.jpg 2494w, /assets/images/FI-KG_logo-small.jpg 1247w, /assets/images/FI-KG_logo-mini.jpg 378w" sizes="50vw"></a></div>
-->

### <a id="Potential_Future_Plans" class="uncolored_link">Potential Future Plans</a>
Our goal is to extend the dataset with additional cases and to establish a recurring AdaptOR event to support progress in this application field. The <a href="https://adaptor2021.github.io/">1st edition of AdaptOR</a> was held at MICCAI 2021. 


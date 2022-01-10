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
<b> +++ AdaptOR challenge re-opened December 2021 +++ </b><br>
The AdaptOR 2021 challenge will be further continued and is open to receiving submissions from Dec 6, 2021.
The participating teams continue to have a maximum of 3 submissions. 
The submissions will be evaluated periodically and updated on our <a href="/leaderboard/">leaderboard</a>. 
Please make note of our revised <a href="assets/files/Data_Access_Agreement_AdaptOR21_v2.0.pdf">data access form</a>. 
The joint challenge publication has not yet been carried out. 
This publication will be planned by the organisers, once a sufficient number of submissions 
are received from the participants. </p>

### <a id="News" class="uncolored_link">News </a>
<ul>
<li> December 6th, 2021 - The AdaptOR challenge is re-opened and is now accepting further submissions. Please take note of the revised <a href="assets/files/Data_Access_Agreement_AdaptOR21_v2.0.pdf">data access form</a>.
The results of the evaluation will be periodically updated on our <a href="/leaderboard/">leaderboard</a>.</li>
<div class="smaller-text">
<li> November 8th, 2021 - Find the recent work from the organisers, that proposes further methodological developments on the challenge dataset <a href="https://adaptor2021.github.io/publications/">here</a>.</li>
<li> September 25th, 2021 - Find the submissions of the participants, published in the proceedings of the DGM4Miccai Workshop, LNCS MICCAI 2021 <a href="https://adaptor2021.github.io/publications/">here</a>.</li>
<li> September 20th, 2021 - The final results are computed and will be announced at the DGM4Miccai Workshop on October 1st, 2021. The program can be seen <a href="https://dgm4miccai.github.io/">here</a>.</li>
<li> July 16th, 2021 - Find the recent work from the organisers, that proposes methodological developments on the challenge dataset <a href="https://adaptor2021.github.io/publications/">here</a>. Stay tuned for the challenge publication, coming soon.</li>
<li> July 05th, 2021 - The final Docker Container Submission must be submitted to the Evaluation Queue <a href="https://www.synapse.org/#!Synapse:syn25314439/challenge/">AdaptOR Challenge 2021 (MICCAI) Submission (9614850)</a> by July 07th 2021, as explained in the <a href="https://www.synapse.org/#!Synapse:syn25314439/wiki/610471">Submission Tutorial</a>.</li>
<li> June 25th, 2021 - Deadline extended to July 2nd 2021, 11:59 PM Pacific Time </li>
<li>
June 22nd, 2021 - Don't forget to choose the AdaptOR Challenge option under "Subject Areas", while creating a submission in the <a href="https://cmt3.research.microsoft.com/DGM4MICCAI2021">CMT platform</a> on June 25th. Read more about what to submit <a href="https://adaptor2021.github.io/timeline/#Publication">here</a> and use the opportunity of the Platform Testing Phase while it is still possible.</li>
<li> June 01st, 2021 - The Platform Testing Phase has started. <a href="https://adaptor2021.github.io/submissiondetails/">Submit</a> your models to test the submission process to the Evaluation Queue <a href="https://www.synapse.org/#!Synapse:syn25314439/challenge/">AdaptOR Challenge 2021 (MICCAI) Platform Test (9614808)</a> as explained in the <a href="https://www.synapse.org/#!Synapse:syn25314439/wiki/610471">Submission Tutorial</a>. The results of your test submissions will be visible <a href="https://www.synapse.org/#!Synapse:syn25314439/wiki/609452">here</a>.</li>
<li> May 27th, 2021 - <span style="color: #2f5697;">The last possible registration date is now 06/06/2021. Don't miss your chance and <a href="https://adaptor2021.github.io/registration/">register now</a>!</span></li>
<li> May 27th, 2021 - Find out how we will evaluate the output of submissions with our evaluation script on the <a href="https://www.synapse.org/#!Synapse:syn25806839">Synapse platform</a> and in the <a href="https://github.com/Cardio-AI/adaptor_docker_example/blob/main/evaluation.py">Docker Example GitHub Repo</a>!</li>
<li> May 12th, 2021 - We have now made more information about the <a href="https://adaptor2021.github.io/submissiondetails/">Submission Details</a> available. Check out the <a href="https://www.synapse.org/#!Synapse:syn25314439/wiki/610471">Submission Tutorial</a> and our <a href="https://github.com/Cardio-AI/adaptor_docker_example">Docker Example</a>!</li>
<li> May 11th, 2021 - We are happy to announce that <a href="#Prizes">Challenge Awards</a> will be provided for the three top performing teams. We thank <a href="https://www.fehling-instruments.de/">Fehling Instruments GmbH & Co. KG</a> for their support!</li>
<li> May 03rd, 2021 - AdaptOR is featured as challenge of the month on <a href="https://www.rsipvision.com/ComputerVisionNews-2021May/20/">Computer Vision News</a>!  </li>
<li> April 27th, 2021 - It's now official: The AdaptOR Challenge will be hosted by the <a href="https://dgm4miccai.github.io/">DGM4MICCAI Workshop</a>.  </li>
<li> April 09th, 2021 - To jump-start our participants' work, <a href="https://www.synapse.org/#!Synapse:syn25470804"> helper functions </a> in python can be found on the Synapse platform.  </li>
<li> April 01st, 2021 - Training phase starts: Datasets are now available and teams can register on the <a href="https://www.synapse.org/#!Synapse:syn25314439">Synapse platform</a>! </li>
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

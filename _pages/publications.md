---
title: "Publications"
permalink: /publications/
layout: home
summary: "Publications"
---

<h2 class="divider">Methodological developments on the challenge dataset from the organisers (we did not participate in the challenge):</h2>

<table style="border: 1px solid #d3d3d3; border-radius: 5px;">
      <tr>
            <td style=" border: 0px; width:30%">
                  <a href="https://arxiv.org/pdf/2107.06941">
                        <img src="/assets/images/Mutually_improved_endoscopic_image_synthesisand_landmark_detectionin_unpaired_image-to-image_translation-cover.png"
                              srcset="/assets/images/Mutually_improved_endoscopic_image_synthesisand_landmark_detectionin_unpaired_image-to-image_translation-cover.png 1224w, /assets/images/Mutually_improved_endoscopic_image_synthesisand_landmark_detectionin_unpaired_image-to-image_translation-cover-medium.png 808w, /assets/images/Mutually_improved_endoscopic_image_synthesisand_landmark_detectionin_unpaired_image-to-image_translation-cover-small.png 404w, /assets/images/Mutually_improved_endoscopic_image_synthesisand_landmark_detectionin_unpaired_image-to-image_translation-cover-mini.png 122w"
                              sizes="20vw" style="border: 1px solid; border-radius: 3px;">
                  </a>
            </td>
            <td style="vertical-align:top; border: 0px; width:70%">
                  <h1 style="margin: 0">
                        <a id="Mutually_improved_endoscopic_image_synthesis_and_landmark_detection_in_unpaired_image-to-image_translation"
                              class="uncolored_link" href="https://arxiv.org/abs/2107.06941"
                              style="text-decoration: none;">Mutually improved endoscopic image synthesis and landmark
                              detection in unpaired image-to-image translation</a>
                  </h1><br>
                  <i>14 Jul 2021</i><br>
                  Lalith Sharan, Gabriele Romano, Sven Koehler, Halvar Kelm, Matthias Karck, Raffaele De Simone, Sandy
                  Engelhardt<br>

                  <h2>Abstract:</h2>
                  <div style="font-size: 12px;">
                        The CycleGAN framework allows for unsupervised image-to-image translation of unpaired data. In a
                        scenario of
                        surgical training on a physical surgical simulator, this method can be used to transform
                        endoscopic images of
                        phantoms into images which more closely resemble the intra-operative appearance of the same
                        surgical target
                        structure. This can be viewed as a novel augmented reality approach, which we coined
                        Hyperrealism in previous
                        work. In this use case, it is of paramount importance to display objects like needles, sutures
                        or instruments
                        consistent in both domains while altering the style to a more tissue-like appearance.
                        Segmentation of these
                        objects would allow for a direct transfer, however, contouring of these, partly tiny and thin
                        foreground objects
                        is cumbersome and perhaps inaccurate. Instead, we propose to use landmark detection on the
                        points when sutures
                        pass into the tissue. This objective is directly incorporated into a CycleGAN framework by
                        treating the
                        performance of pre-trained detector models as an additional optimization goal. We show that a
                        task defined on
                        these sparse landmark labels improves consistency of synthesis by the generator network in both
                        domains. Comparing
                        a baseline CycleGAN architecture to our proposed extension (DetCycleGAN), mean precision (PPV)
                        improved by +61.32,
                        mean sensitivity (TPR) by +37.91, and mean F1 score by +0.4743. Furthermore, it could be shown
                        that by dataset
                        fusion, generated intra-operative images can be leveraged as additional training data for the
                        detection network
                        itself. The data is released within the scope of the AdaptOR MICCAI Challenge 2021 at <a
                              href="https://adaptor2021.github.io/">https://adaptor2021.github.io/</a>, and code at <a
                              href="https://github.com/Cardio-AI/detcyclegan_pytorch">https://github.com/Cardio-AI/detcyclegan_pytorch</a>. DOI:	10.1109/JBHI.2021.3099858. The link to the IEEE Early access article can be found here: <a
                                    href="https://ieeexplore.ieee.org/document/9496194">https://ieeexplore.ieee.org/document/9496194</a> , and the link to the preprint can be found here:<a
                                          href="https://arxiv.org/abs/2107.06941">https://arxiv.org/abs/2107.06941</a>

                  </div>
            </td>
      </tr>
      <tr>
            <td colspan="2">
                  <h2 style="margin: 0">
                        Bibtex citation:
                  </h2>  
<div markdown="1">


```
@article{sharan_mutually_2021,
	title = {Mutually improved endoscopic image synthesis and landmark detection in unpaired image-to-image translation},
	issn = {2168-2208},
	doi = {10.1109/JBHI.2021.3099858},
	journal = {IEEE Journal of Biomedical and Health Informatics},
	author = {Sharan, Lalith and Romano, Gabriele and Koehler, Sven and Kelm, Halvar and Karck, Matthias and De Simone, 
	Raffaele and Engelhardt, Sandy},
	year = {2021},
	note = {Conference Name: IEEE Journal of Biomedical and Health Informatics},
	keywords = {CycleGAN, Generative adversarial networks, Generative Adversarial Networks, Landmark Detection, Landmark 
	Localization, Maintenance engineering, Mitral Valve Repair, Semantics, Surgery, Surgical Simulation, Surgical 
	Training, Task analysis, Training, Valves},
	pages = {1--1},
}
```
</div>
            </td>
      </tr>
      <tr>
            <td style=" border: 0px; width:30%">
                  <a href="https://link.springer.com/article/10.1007/s11548-021-02523-w">
                        <img src="/assets/images/Point_detection_through_multi-instance_deep_heatmap_regression_for_sutures_in_endoscopy-cover.png"
                              srcset="/assets/images/Point_detection_through_multi-instance_deep_heatmap_regression_for_sutures_in_endoscopy-cover.png 1224w, /assets/images/Point_detection_through_multi-instance_deep_heatmap_regression_for_sutures_in_endoscopy-cover-medium.png 808w, /assets/images/Point_detection_through_multi-instance_deep_heatmap_regression_for_sutures_in_endoscopy-cover.png 1224w, /assets/images/Point_detection_through_multi-instance_deep_heatmap_regression_for_sutures_in_endoscopy-cover-medium.png 404w, /assets/images/Point_detection_through_multi-instance_deep_heatmap_regression_for_sutures_in_endoscopy-cover.png 1224w, /assets/images/Point_detection_through_multi-instance_deep_heatmap_regression_for_sutures_in_endoscopy-cover-medium.png 122w"
                              sizes="20vw" style="border: 1px solid; border-radius: 3px;">
                  </a>
            </td>
            <td style="vertical-align:top; border: 0px; width:70%">
                  <h1 style="margin: 0">
                        <a id="Point detection through multi-instance deep heatmap regression for sutures in endoscopy"
                              class="uncolored_link" href="https://link.springer.com/article/10.1007/s11548-021-02523-w"
                              style="text-decoration: none;">Point detection through multi-instance deep heatmap regression for sutures in endoscopy</a>
                  </h1><br>
                  <i>08 Nov 2021</i><br>
                  Lalith Sharan, Gabriele Romano, Julian Brand, Halvar Kelm, Matthias Karck, Raffaele De Simone, Sandy
                  Engelhardt<br>

                  <h2>Abstract:</h2>
                  <div style="font-size: 12px;">
                    Purpose:
                    Mitral valve repair is a complex minimally invasive surgery of the heart valve. In this context, 
                    suture detection from endoscopic images is a highly relevant task that provides quantitative 
                    information to analyse suturing patterns, assess prosthetic configurations and produce augmented 
                    reality visualisations. Facial or anatomical landmark detection tasks typically contain a fixed 
                    number of landmarks, and use regression or fixed heatmap-based approaches to localize the landmarks. 
                    However in endoscopy, there are a varying number of sutures in every image, and the sutures may 
                    occur at any location in the annulus, as they are not semantically unique.

                    Method:
                    In this work, we formulate the suture detection task as a multi-instance deep heatmap regression 
                    problem, to identify entry and exit points of sutures. We extend our previous work, and 
                    introduce the novel use of a 2D Gaussian layer followed by a differentiable 2D spatial Soft-Argmax 
                    layer to function as a local non-maximum suppression.

                    Results: 
                    We present extensive experiments with multiple heatmap distribution functions and two variants of 
                    the proposed model. In the intra-operative domain, Variant 1 showed a mean F1
                    of +0.0422 over the baseline. Similarly, in the simulator domain, Variant 1 showed a mean F1 
                    of +0.0865 over the baseline.
                    
                    Conclusion:
                    The proposed model shows an improvement over the baseline in the intra-operative and the simulator 
                    domains. The data is made publicly available within the scope of the MICCAI AdaptOR2021 Challenge 
                    <a href="https://adaptor2021.github.io/">https://adaptor2021.github.io/</a>, and the code at 
                    <a href="https://github.com/Cardio-AI/suture-detection-pytorch/">
                    https://github.com/Cardio-AI/suture-detection-pytorch/</a>.

                    DOI:10.1007/s11548-021-02523-w. The link to the open access article can be found here: 
                    <a href="https://link.springer.com/article/10.1007%2Fs11548-021-02523-w">https://link.springer.com/article/10.1007%2Fs11548-021-02523-w</a> 

                  </div>
            </td>
      </tr>
      <tr>
            <td colspan="2">
                  <h2 style="margin: 0">
                        Bibtex citation:
                  </h2>  
<div markdown="1">


```
@article{sharan_point_2021,
	title = {Point detection through multi-instance deep heatmap regression for sutures in endoscopy},
	issn = {1861-6429},
	url = {https://doi.org/10.1007/s11548-021-02523-w},
	doi = {10.1007/s11548-021-02523-w},
	language = {en},
	urldate = {2021-11-16},
	journal = {International Journal of Computer Assisted Radiology and Surgery},
	author = {Sharan, Lalith and Romano, Gabriele and Brand, Julian and Kelm, Halvar and Karck, Matthias and De Simone, 
	Raffaele and Engelhardt, Sandy},
	month = nov,
	year = {2021}
}
```
</div>
            </td>
      </tr>
</table>

<h2 class="divider">Submissions from the participants:</h2>

<table style="border: 1px solid #d3d3d3; border-radius: 5px;">
      <tr>
            <td style="vertical-align:top; border: 0px; width:70%">
                  <h1 style="margin: 0">
                        <a id="Cross-Domain Landmarks Detection in Mitral Regurgitation"
                              class="uncolored_link" href="https://link.springer.com/chapter/10.1007/978-3-030-88210-5_12"
                              style="text-decoration: none;">Cross-Domain Landmarks Detection in Mitral Regurgitation (1st Prize)</a>
                  </h1><br>
                  <i>25 Sep 2021</i><br>
                  Jiacheng Wang, Haojie Wang, Ruochen Mu, Liansheng Wang <br>
            </td>
      </tr>
      <tr>
            <td colspan="2">
                  <h2 style="margin: 0">
                        Bibtex citation:
                  </h2>  
<div markdown="1">


```
@inproceedings{wang_cross-domain_2021,
	address = {Cham},
	series = {Lecture {Notes} in {Computer} {Science}},
	title = {Cross-{Domain} {Landmarks} {Detection} in {Mitral} {Regurgitation}},
	isbn = {978-3-030-88210-5},
	doi = {10.1007/978-3-030-88210-5_12},
	language = {en},
	booktitle = {Deep {Generative} {Models}, and {Data} {Augmentation}, {Labelling}, and {Imperfections}},
	publisher = {Springer International Publishing},
	author = {Wang, Jiacheng and Wang, Haojie and Mu, Ruochen and Wang, Liansheng},
	editor = {Engelhardt, Sandy and Oksuz, Ilkay and Zhu, Dajiang and Yuan, Yixuan and Mukhopadhyay, Anirban and Heller, 
	Nicholas and Huang, Sharon Xiaolei and Nguyen, Hien and Sznitman, Raphael and Xue, Yuan},
	year = {2021},
	keywords = {Deep learning, Landmark detection, Mitral regurgitation},
	pages = {134--141},
}
```
</div>
            </td>
      </tr>
</table>

<table style="border: 1px solid #d3d3d3; border-radius: 5px;">
      <tr>
            <td style="vertical-align:top; border: 0px; width:70%">
                  <h1 style="margin: 0">
                        <a id="Improved Heatmap-Based Landmark Detection"
                              class="uncolored_link" href="https://link.springer.com/chapter/10.1007/978-3-030-88210-5_11"
                              style="text-decoration: none;">Improved Heatmap-Based Landmark Detection (2nd Prize)</a>
                  </h1><br>
                  <i>25 Sep 2021</i><br>
                  Huifeng Yao, Ziyu Guo, Yatao Zhang, Liansheng Wang <br>
            </td>
      </tr>
      <tr>
            <td colspan="2">
                  <h2 style="margin: 0">
                        Bibtex citation:
                  </h2>  
<div markdown="1">


```
@inproceedings{yao_improved_2021,
	address = {Cham},
	series = {Lecture {Notes} in {Computer} {Science}},
	title = {Improved {Heatmap}-{Based} {Landmark} {Detection}},
	isbn = {978-3-030-88210-5},
	doi = {10.1007/978-3-030-88210-5_11},
	language = {en},
	booktitle = {Deep {Generative} {Models}, and {Data} {Augmentation}, {Labelling}, and {Imperfections}},
	publisher = {Springer International Publishing},
	author = {Yao, Huifeng and Guo, Ziyu and Zhang, Yatao and Li, Xiaomeng},
	editor = {Engelhardt, Sandy and Oksuz, Ilkay and Zhu, Dajiang and Yuan, Yixuan and Mukhopadhyay, Anirban and Heller, 
	Nicholas and Huang, Sharon Xiaolei and Nguyen, Hien and Sznitman, Raphael and Xue, Yuan},
	year = {2021},
	keywords = {CycleGAN, Heatmap, Landmark detection},
	pages = {125--133}
}
```
</div>
            </td>
      </tr>

</table>
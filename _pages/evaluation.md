---
title: "Evaluation"
permalink: /evaluation/
layout: home
summary: "Information about evaluation"
usemathjax: true
---

### <a id="Evaluation" class="uncolored_link">Test dataset and ground-truth</a>

The evaluation is performed by computing a similarity metric between the predicted images from the right camera view, and the ground-truth images captured from the right-camera of a stereo-endoscope.
More information on the data acquisition process, can be found [here](/datasetinfo/). The test dataset comprises images from multiple surgeries in the intra-operative domain, with varying light illumination, camera angles and view of the scene.

#### <a id="Metrics_And_Reporting" class="uncolored_link">Evaluation metric</a>

The metric used for evaluation will be a combination of the *Structural similarity (SSIM)* and the *RMSE*, between the predicted and the ground-truth images.
A combination of local and perceptual metrics have been found to be a more reliable indicator of image similarity than only one of the metrics [[1](#1)].

* **Perceptual metrics**: Using a metric such as the *Structural similarity (SSIM)* accounts for the fact that the human visual system is sensitive to changes in local structure. 
The sensitivity of the human visual system to noise depends on local luminance, contrast, and structure [[2](#2)]. The metric takes into account the neighbourhood information of a pixel.

* **Local metrics**: such as the \\(L_p\\) norm are normally are convex and differentiable. and for this reason commonly also used as optimising functions.
However, they assume independence of pixels and ignore local context [[1](#1)]. 
An $$L_p$$ norm has the range \\([ 0, n^{1/p}\times{D} ]\\), where $$D$$ is the maximum pixel value of the image. To be able to use a metric in the range \\([0, 1]\\) that is easier to combine with other image similarity metrics of the same range,
we first normalise the pixel values between \\([0, 1]\\), and then compute the *RMSE* for each channel between the prediction and the ground-truth.
The final score for one sample is then averaged for each channel. In this case, the lower the score the better, since this is an error metric. Therefore, we compute (_1-RMSE_) so that it can be combined on the same scale with _SSIM_.

The final combination of this metric used will be: \\(0.5 * SSIM + 0.5 * (1-RMSE)\\). The implementation of this metric can be found in the Synapse platform [here](https://www.synapse.org/#!Synapse:syn30281269).
We would like to mention here, that no metric is perfect and both the individual metrics as well as the combined metrics have their own limitations. A more detailed analysis of these cases will further be presented in the potential journal publication.

#### <a id="Ranking" class="uncolored_link">Ranking</a>

Previous work [[3](#3)] that performs various analyses on the reporting of biomedical challenges, reveal that ranking performed after aggregation of the metric is more robust than aggregating ranking on independent metrics.
We follow the same strategy in this challenge, where the teams will be ranked based on the aggregate score computed by combining the metrics as outlined in the above section. 
In case the metrics are tied between two teams, the time stamp of the submission will be used for the ranking, and the earlier submission will have a higher ranking.
Further analysis of the ranking of the submission before and after aggregation will also be reported in the potential publication.

#### <a id="Result_announcement" class="uncolored_link">Result announcement</a>

After the registration phase opens, a leaderboard will be maintained on the website and the Synapse platform.
At the end of the challenge, all the results will be made available publicly. 
The announcement of the winner will be made at the workshop and the website will be updated accordingly.
All teams should participate in the workshop and will be invited to present their work in more detail, which we hope will foster detailed discussions. In case of a virtual event, we will seek for providing discussion opportunities in small groups.

### <a id="References" class="uncolored_link">References</a>

[<a id="1">1</a>] Zhang, L., Zhang, L., Mou, X., Zhang, D.: A comprehensive evaluation of full reference image quality assessment algorithms. In: IEEE International Conference on Image Processing. (2012) 1477–1480 1, 2, 3

[<a id="1">2</a>] Zhou Wang, A. C. Bovik, H. R. Sheikh and E. P. Simoncelli, "Image quality assessment: from error visibility to structural similarity," in IEEE Transactions on Image Processing, vol. 13, no. 4, pp. 600-612, April 2004, doi: 10.1109/TIP.2003.819861.

[<a id="1">3</a>] Maier-Hein, L., Eisenmann, M., Reinke, A., Onogur, S., Stankovic, M., Scholz, P., Arbel, T., Bogunovic, H., Bradley, A. P., Carass, A., Feldmann, C., Frangi, A. F., Full, P. M., van Ginneken, B., Hanbury, A., Honauer, K., Kozubek, M., Landman, B. A., März, K., ... Kopp-Schneider, A. (2018). Why rankings of biomedical image analysis competitions should be interpreted with care. Nature Communications, 9(1), 5217. https://doi.org/10.1038/s41467-018-07619-7




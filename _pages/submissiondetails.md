---
permalink: /submissiondetails/
title: "Submission details"
layout: home
summary: "Information about the submission and the evaluation"
---

## <a id="Submission" class="uncolored_link">Submission</a>

For the purpose of result verification and to encourage reproducibility and transparency, all entries must submit a **Docker container on the Synapse platform** with the following requirements:
  - (Mandatory:) Participants must submit a half-page write up of the challenge explaining their approach.
  - (Mandatory:) For each new input image of size 960x540 belonging to the left camera from the Intraop-Domain, the model should be able to generate an image of the same size belonging to the right camera.
  The docker container should output an image for **all images** in the hosts input directory via the command:
  ```
  $ docker run --gpus all -v "<absolute_host_input_directory>:/input" -v "<absolute_host_output_directory>:/output" adaptor_challenge view_synthesis
  ```

Please refer to our upcoming AdaptOR Submission Tutorial and the AdaptOR Docker Submission Example for more detailed information.

Teams are encouraged to provide their code open source.  
Participants agree that the challenge organizers are allowed to use their submitted docker containers to run further meta-analysis.

Each participating team is allowed to make a total of 3 submissions to the system. The evaluation after each submission will be communicated to the team. 
The best results out of the submissions will be considered as the final result, and the same will be updated on the leaderboard. The docker will run on a **24 Gb RAM Nvidia Titan RTX**. Please make sure the specified batch size in your code does not exceed the 24 Gb limit

The challenge will be split into **three phases**: Training phase, Platform testing phase, Testing phase.

During **training phase**, the participating teams will be able to independently validate their results using cross-validation on the training data.

During the platform **testing phase**, they are allowed to use the official submission platform to resolve potential technical issues. We will use dummy datasets for sanity checks, e.g. to ensure the submission is in the correct format.

During the **test phase**, participants are allowed to make in total three submissions. The best result out of these three is selected as final result. The docker will run on a **24 Gb RAM Nvidia Titan RTX**. Make sure the specified batch size in your code does not exceed the 24 Gb limit.

### <a id="Evaluation" class="uncolored_link">Evaluation</a>

#### <a id="Metrics_And_Reporting" class="uncolored_link">Metrics And Reporting</a>

We will make the code available on the synapse platform that will be used to compute the metrics for ranking.
The metric used for evaluation is a combination of local distance-based metric (L1) and a perceptual metric (SSIM).

#### <a id="Ranking" class="uncolored_link">Ranking</a>

The evaluation is performed on the intra-operative test dataset using weighted L1 and SSIM.
In case the metrics are tied between two teams, the time stamp of the submission will be used for the ranking, and the earlier submission will have a higher ranking.

#### <a id="Result_announcement" class="uncolored_link">Result announcement</a>

All the results will be made available publicly. The announcement of the winner will be made at the workshop and the website will be updated accordingly.
All teams should participate in the workshop and will be invited to present their work in more detail, which we hope will foster detailed discussions. In case of a virtual event, we will seek for providing discussion opportunities in small groups.

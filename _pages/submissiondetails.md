---
permalink: /submissiondetails/
title: "Submission details"
layout: home
summary: "Information about the submission and the evaluation"
---

## <a id="Submission" class="uncolored_link">Submission</a>

For the purpose of result verification and to encourage reproducibility and transparency, all entries must submit a **Docker container on the Synapse platform** with the following requirements:

  - (Mandatory:) For each new input image of size 512x288 from the Intraop-Domain, the model should be able to generate an output **JSON-File**. Each JSON-File should contain a JSON-Object with `folderName`, `subfolderName` and `imageFileName` string attributes as well as a `points` array. The `points` array should contain objects with `x` and `y` number attributes representing the pixel coordinates of each landmark. A JSON-File-Output-Example could look as follows:
  ```
  {
        "folderName": "aicm1",
        "subfolderName": "VID000_0",
        "imageFileName": "000000.png",
        "points": [
          {
            "x": 1,
            "y": 1
          },
          {
            "x": 2,
            "y": 2
          }
        ]
  }
  ```
  No detected landmarks should result in a JSON-Object with an empty `points` array.
  The docker container should detect landmarks in **all images** in the hosts input directory via the command:
  ```
  $ docker run --gpus all -v "<absolute_host_input_directory>:/input" -v "<absolute_host_output_directory>:/output" adaptor_challenge landmark_detection
  ```

  - (Optional:) For each new input image of size 512x288, the model should be able to output an image which was **transformed** into the Intraop-Domain and vice versa. These results do not play a role in the final rankings, but should provide insights on the quality of image-to-image transformation. Example images will be shown during the workshop event and in the joint publication. Depending on the number of submissions, an additional user-study with domain experts might be conducted at a later stage. The docker container should transform **all images** in the hosts input directory via the command:
  ```
  $ docker run --gpus all -v "<absolute_host_input_directory>:/input" -v "<absolute_host_output_directory>:/output" adaptor_challenge domain_transformation
  ```

**Please refer to the [AdaptOR Submission Tutorial](https://www.synapse.org/#!Synapse:syn25314439/wiki/610471) and the [AdaptOR  Docker Submission Example](https://github.com/Cardio-AI/adaptor_docker_example) for more detailed information.**

Teams are encouraged to provide their code open source.  
Participants agree that the challenge organizers are allowed to use their submitted docker containers to run further meta-analysis.

Each participating team is allowed to make a total of 3 submissions to the system. The evaluation after each submission will be communicated to the team. 
The best results out of the submissions will be considered as the final result, and the same will be updated on the leaderboard. The docker will run on a **24 Gb RAM Nvidia Titan RTX**. Please make sure the specified batch size in your code does not exceed the 24 Gb limit

<span style="color:#B6B6B4">The challenge will be split into **three phases**: Training phase, Platform testing phase, Testing phase</span>.

<span style="color:#B6B6B4">During **training phase**, the participating teams will be able to independently validate their results using crossvalidation on the training data </span>.

<span style="color:#B6B6B4">During the platform **testing phase**, they are allowed to use the official submission platform to resolve potential technical issues. We will use dummy datasets for sanity checks, e.g. to ensure the submission is in the correct format</span>.

<span style="color:#B6B6B4">During the **test phase**, participants are allowed to make in total three submissions. The best result out of these three is selected as final result. The docker will run on a **24 Gb RAM Nvidia Titan RTX**. Make sure the specified batch size in your code does not exceed the 24 Gb limit</span>.

### <a id="Evaluation" class="uncolored_link">Evaluation</a>

#### <a id="Metrics_And_Reporting" class="uncolored_link">Metrics And Reporting</a>

We will make the code available on the synapse platform that will be used to compute the metrics for ranking.

We will report **true positives**, **false positives** and **false negatives**.
A landmark is counted as true positive, if it lies within a radius of 6 pixels around the manually labeled point, same as in [[4]({{ site.url }}#4)]. This accounts for the fact that the region, where the suture enters or exits the tissue, is usually a small region and not just a single pixel. Finally, we report **sensitivity/recall** (TPR) and **precision** (PPV).

#### <a id="Ranking" class="uncolored_link">Ranking</a>

Precision and Recall are computed over all landmarks in the test sets. It is not differentiated whether the prediction is particularly well for certain frames/patients/simulations and worse for others.  
The traditional F-score or **balanced F-score** (F1 score) presents the harmonic mean of precision and recall and will be used to determine the ranking (the higher the better).
We exclude false negative rate (FNR) in the ranking, since it is related to TPR by TPR = 1-FNR. In the case where all metrics are tied, we will accept to have multiple teams with the same ranking.

#### <a id="Result_announcement" class="uncolored_link">Result announcement</a>

The results will be evaluated and updated on the [leaderboard](/_pages/leaderboard.md).

<span style="color:#B6B6B4">All the results will be made available publicly. The announcement of the winner will be made at the workshop and the website will be updated accordingly.
All teams should participate in the workshop and will be invited to present their work in more detail, which we hope will foster detailed discussions. In case of a virtual event, we will seek for providing discussion opportunities in small groups</span>.

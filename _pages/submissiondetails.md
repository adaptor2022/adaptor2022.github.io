---
permalink: /submissiondetails/
title: "Submitting to AdaptOR 2022"
layout: home
summary: "Information about submission "
usemathjax: true
---

### <a id="Submission" class="uncolored_link">What's Required</a>

1. For the purpose of result verification and to encourage reproducibility and transparency, all entries must submit a **Docker container on the Synapse platform** (more details in the below sections). 
2. Additionally, the participants must submit a half-page write up of the challenge explaining their approach.

### <a id="Submission" class="uncolored_link">Submission format</a>

1. The Docker container must meet the following requirements:
   - For each new input image of size \\(960 \times 540\\) belonging to the left camera from the Intraop-Domain, the model should be able to generate an image of the same size belonging to the right camera, following the same folder structure as the given test dataset.
   - The docker container should output an image for **all images** in the hosts input directory via the command:
     ```
     $ docker run --gpus all -v "<absolute_host_input_directory>:/input" -v "<absolute_host_output_directory>:/output" adaptor_challenge
     ```
   - Please refer to our [AdaptOR Docker example](https://github.com/Cardio-AI/adaptor_docker_example), to get easily set up with docker for your model. 

2. In addition to the half-page write-up, the participants also have an option to submit an \\(8\\)-page LNCS paper on their methods to the [DGM4MICCAI](https://dgm4miccai.github.io/) workshop in MICCAI 2022. More information can be found [here](/publications/).

### <a id="Submission" class="uncolored_link">How and where to submit</a>

1. The submissions of the Docker container are done via the [Synapse platform](https://www.synapse.org/#!Synapse:syn29340309/wiki/) of our challenge. Please refer to our [submission tutorial](https://www.synapse.org/#!Synapse:syn29340309/wiki/617629) on how you can submit your container to our challenge via the Synapse platform. The challenge will be split into **three phases**: Training phase, Platform testing phase, Submission phase.

   * **Training phase** (Until 30.06.2022): The participating teams can independently validate their results using cross-validation on the training data.

   * **Platform testing phase** (01.07.2022-01.08.2022): During the platform testing phase, the participants are allowed to use the official submission platform to resolve potential technical issues. We will use dummy datasets for sanity checks, e.g. to ensure the submission is in the correct format.

   * **Submission phase** (15.07.2022-15.08.2022): During the submission phase, participants are allowed to make in total three submissions. The best result out of these three is selected as final result. The docker will run on a **\\(24\\) GB RAM Nvidia Titan RTX**. Make sure the specified batch size in your code does not exceed the \\(24\\) GB limit.

2. More details about how to submit the half-page write-up will follow soon. 

### <a id="Evaluation" class="uncolored_link">Evaluation</a>

Please refer to our [evaluation page](/evaluation/) for details on how evaluation, ranking and reporting of the metrics will be performed.

{% capture notice-2 %} 
**Note**: Teams are encouraged to provide their code open source. The URL should be added in the half-page description and in the potential LNCS submission.
Participants agree that the challenge organizers are allowed to use their submitted docker containers to run further meta-analysis.
{% endcapture %}

<div class="notice--info">{{ notice-2 | markdownify }}</div>


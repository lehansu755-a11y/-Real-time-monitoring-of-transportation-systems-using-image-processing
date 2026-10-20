# Real-time Monitoring of Transportation Systems Using Image Processing

Name: Sulehan  
Neptun code: CRX1CQ

## My interpretation of the brief

I understand this project as the development of an image-processing system that turns camera footage into useful information about transportation activity.

As an initial proposal, I would focus on road traffic observed by a fixed camera. The system would detect vehicles, assign suitable categories, and track them across consecutive frames so that it can produce vehicle counts without repeatedly counting the same vehicle. The precise monitoring scenario and required outputs would be agreed with the supervisor.

## Why I am a good fit for this project

I am interested in how a computer can learn to recognise objects from examples and apply that knowledge to new images.

My initial idea is to use labelled data to teach a model to distinguish relevant vehicle categories. I would like to understand how the model learns useful visual features rather than simply remembering individual examples.

What interests me most is whether the recognition remains reliable when lighting, camera distance, vehicle appearance, or partial occlusion changes. I would also like to investigate the trade-off between recognition quality and processing speed, since a useful monitoring system needs to produce timely results.

## Relevant experience and background

Through my current Project Work, I am gaining experience in defining a software project, analysing technical problems, and maintaining documentation in GitHub.

I would like to build on this experience while learning about computer vision, supervised learning, video processing, and experimental evaluation. This project would allow me to connect these topics through a practical software prototype.

## Proposed approach

I would first confirm the monitoring scenario, target categories, and available video sources with the supervisor. I would then inspect suitable datasets and select footage with appropriate annotations and usage permissions.

I would establish a baseline using a suitable pretrained object detector. Detection would identify both the locations and categories of vehicles, rather than assign a single label to the entire frame. If the baseline is unsuitable for the selected footage, I would investigate fine-tuning it on representative labelled examples instead of assuming that training from scratch is necessary.

Next, I would add multi-object tracking to associate detections across frames. A virtual counting line or defined region could then be used to produce vehicle counts and counts by category.

The prototype would display annotated video and simple monitoring statistics. I would initially test recorded footage and measure whether the full pipeline can keep up with the source frame rate on the available hardware before testing a live input where accessible.

Evaluation would compare detections with annotations, vehicle counts with manually checked counts, and processing speed with the input rate. I would report suitable detection metrics, counting error, throughput, and processing latency, while examining missed detections, duplicate counts, and tracking failures.

Training and evaluation data would be separated by recording sequence, and by scene where feasible, to reduce leakage from near-identical neighbouring frames.

## Initial plan

1. Confirm the monitoring scenario, categories, and expected outputs.
2. Review suitable methods and inspect available datasets.
3. Prepare video input, annotations, and separate evaluation sequences.
4. Implement and evaluate a pretrained detection baseline.
5. Add tracking and a clearly defined counting rule.
6. Display annotated video and basic traffic statistics.
7. Compare accuracy and runtime under different conditions.
8. Document the results, limitations, and possible improvements.

## Additional information

The initial scope would cover a manageable fixed-camera scenario with a limited number of vehicle categories. Fine-tuning would depend on the available annotations and computing resources.

Speed estimation or congestion indicators could be considered later if suitable calibration data and clear evaluation criteria are available. Traffic-light control and a complete city-wide deployment would remain outside the initial scope.

The main deliverables would be a documented prototype, reproducible experiments, and an evaluation of the balance between monitoring reliability and processing speed.

GitHub repository:  
https://github.com/lehansu755-a11y/-Real-time-monitoring-of-transportation-systems-using-image-processing

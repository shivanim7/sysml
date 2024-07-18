# Improving Energy Efficiency in Video Analytics 📹⚡

## Authors
**Systems of Machine Learning (SysML) Lab:** Adam Yang, Shivani Manivasagan, Ket Hollingsworth

## Date
May 2023 - Aug 2023

## Summary
Video analytics, which involves using machine learning models to detect objects in videos, is energy-intensive, making it difficult to deploy on energy-constrained devices in applications such as traffic monitoring, wildlife tracking, precision agriculture, etc.

This research project investigates:
- Baseline energy consumption in various computer vision pipelines.
- Methods to reduce energy consumption, such as frame-filtering, frame-differencing, and using low-level video characteristics to adjust resolution and frame rate for analysis.

### Methodology
- Ran the YOLOv5 object detection ML model on a Raspberry Pi 4, using the UM25C power meter to measure energy consumption of analysis on different test videos.
- Explored impact of different ML models (YOLOv5n, YOLOv5s, YOLOv5x for videos; ResNet, 
SSD300 VGG16 for images).
- Selected videos to test combinations of fast-moving or slow-moving, large or small objects.
- Experimented with frame-filtering and frame-differencing during analysis.
- Built a testing pipeline from scratch.

### Observations
- **Linear relationships** identified between energy consumption and both resolution and frame rate of input video.
- Analyzed statistics for each test run, including:
  - Inference runtime and average time per frame
  - Total energy consumption and energy used per frame
  - Average power consumption
  - Accuracy (mean average precision)


### Future Work
We seek a low-energy method of analyzing frames to determine how much we can reduce resolution and frame rate for accurate yet energy-efficient analysis. Example: Videos with slow-moving objects can be processed at lower frame rate, and videos with large objects can be processed at a lower resolution, without compromising accuracy.

Others in the field have worked increasing computational efficiency of video analytics, but there is not much literature on energy. Our work helps advance understanding of how energy consumption relates to video characteristics, and in the future, this can help the transition to self-sustaining energy-harvesting devices capable of deploying vision models.

## Acknowledgements
- Professor Arthi Padmanabhan
- Various research papers on computationally-efficient video analytics techniques

---
title: Wildfire Spread Modeling
layout: page
---

We leverage deep learning and explainable AI to model short-term wildfire spread from satellite data and improve current prediction accuracies. The recent surge in wildfire incidents, exacerbated by climate change, demands effective prediction and monitoring solutions. This study introduces a novel deep learning model, the Attention Swin U-net with Focal Modulation (ASUFM), designed to predict wildfire spread in North America using large-scale remote sensing data. The ASUFM model integrates spatial attention and focal modulation into the Swin U-net architecture, significantly enhancing predictive performance on the Next Day Wildfire Spread (NDWS) benchmark. Additionally, we have developed an expanded dataset that encompasses wildfire data across North America from 2012 to 2023, providing a more extensive basis for model training and validation. Our approach demonstrates state-of-the-art performance in wildfire spread prediction, offering a promising tool for risk mitigation and resource allocation in wildfire management. Related code is in our [public repository](https://github.com/bronteee/fire-asufm).


## Results

<img src="images/pred_all_4.png" width=800>

<img src="images/table1_overall.png" width=600>

<img src="images/table3_extended_results.png" width=600>

## Discussion

### Limitations
Our work is an initial exploration of tailoring current state-of-the-art segmentation techniques on wildfire spread modeling with multi-spectral data. The challenging nature of this problem, compounded with ambiguity from the MODIS data leaves this an open research problem to be explored. Early experiments on various input bands suggest that some features may have confounding effects on the final prediction accuracy rather than improvement. While this study focuses on the input bands most likely to contribute to fire ignition and propagation, further examination of feature selection could be useful. On the other hand, due to the high variability and limited extensibility in available data sets for wildfire spread, comparison across multiple sources becomes difficult.  Other factors not explored include finer temporal resolution, other spatial resolution, and larger multi-modal models, which may offer additional capacity for extracting diverse information.

### Potential applications
Many previous studies have depended on specialized data that is challenging to acquire in real-time, consequently limiting their practical applicability in real-world scenarios. This work leverages GEE data which can be easily extended to apply to a real-time prediction map. In addition, we provide the pre-trained model weights that can be fine-tuned on region-specific data.
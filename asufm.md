---
title: Attention Swin U-net with Focal Modulation (ASUFM)
layout: page
---

## Introduction
Inspired by previous advances mentioned above, we present Attention Swin U-net with Focal Modulation (ASUFM) where each of the Transformer blocks consists of a normalization layer (LayerNorm), a focal modulation layer followed by a second normalization, and a shifted window multi-head self-attention, while the spatial attention travels along the skip connections between the encoder and decoder blocks to carry an emphasis on higher importance tokens. In combining these mechanisms of weighting, we ensure focus both across input bands and within an image layer such as the fire perimeter. Below shows the overall architecture of this approach. In addition, including updated information on wildfire events is crucial to providing and evaluating an expansive solution, to this end, we perform additional GEE data extraction to obtain broader spatial and temporal coverage to deal with the complexity of wildfire spread modeling. 

## Overall Architecture

<img src="images/asufm_overall.png" width="400">

## Focal Modulation

<img src="images/asufm_focal.png" width="200">

## Swin Block with Focal Modulation

<img src="images/asufm_swin.png" width="400">
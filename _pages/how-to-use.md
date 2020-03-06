---
layout: archive
title: "How to use"
permalink: /how-to-use/
author_profile: true
---

## 1. Auto3dgm UI in Slicer
The auto3dgm UI consists of three components:
* **setup**: load data and specifiy parameters used in the auto3dgm algorithm
* **run**: subsample and align the data
* **visualize**: the aligned data in a pop-up window

<img src="/images/auto3dgm_UI.png">

## 2. Path setups and parameters
In the **setup** tab, specify 
* input folder: location where you saved the downsampled gorilla skull dataset, e.g., 
```
/Users/ToothAndClaw/Data/Gorilla_Skulls
```
* output folder: location where you want to save the aligned data and the pseudolandmarks, e.g., 
```
/Users/ToothAndClaw/Results/
```

Then click on **Load Data**.

As we discussed in the previous lecture, auto3dgm uses a two-phase analysis for shape alignment. The algorithm first subsamples two sets of pseudolandmarks for each shape, and then aligns the subsampled points. In the algorithm, we will need to specify how many points we will subsample in each phase.  Due to time constraint in this tutorial, let's only use **20 points for phase 1** and **40 points for phase 2**. In general, a few hundred points will give pretty good shape alignment. The more points we use, the better the results. 

<img src="/images/autoinput.png">

There are some other parameters in the auto3dgm UI. In general, you can leave them as they are. 
* **Maximum iterations**: the max number of alignment 
* **Allow reflection**: if selected, mirror reflection will be allowed to optimize alignment. 
* **Subsampling**: 
* *Farthest point sampling* (FPS): select evenly-spreading points
* *Gaussian process landmarks* (GPL): select feature-aware points
* *FPS + GPL hybrid*: select feature-aware points and complemented with evenly-spreading points for optimal speed and accuracy
* **Optional FPS seed**: specify the first point to be selected in FPS. If not specified, the algorithm will use the first one.
* **Hybrid GPL points**: number of feature-aware points to be used in the analysis. The number should be smaller than phase 1 points. 
* **Processing**: options for parallel computing. This will be implemented in future release. 

## 3. Run auto3dgm
In the **run** tab, you can either run the entire analysis or run each step separately. Here I just click "run all steps". The aligned data and the registered pseudolandmarks (in .fcsv files) will be saved in the specified output folder. 

This will take about 5 minutes. 

## 4. Visualize aligned data
The **visualize** tab allows you to see how the aligned data look like. 

Click on **Start mesh visualization viewer**. 

You can select either **visualize phase 1 alignment** or **visualize phase 2 alignment**.
The aligned shapes will be shown in a pop-up browser window. 

Very Importantly, make sure you click on **Stop mesh visualization viewer** button after you finish the visualization. 

Launch your browser and direct it to `http://localhost:8000/index.html`

## 5. Output
You can find the aligned pseudolandmarks (.fcsv files) in the output folder you specified Step 2. Go to folder *Phase 2* and then folder *aligned_landmarks*.

# CBIAS_2021
Software demo for VollSeg for CBIAS 2021

![Triology of Segmentation, Tracking and Track Analysis tools](https://github.com/kapoorlab/CBIAS_2021/blob/main/images/logo.png)

Segmentation using Vollseg and Napari Visualization tool for Trackmate > 6.0 and bTrackmate XML files for 3D + time tracks.


## Installation
To use these notebooks install the following packages:

`pip install --user napatrackmater`
`pip install --user vollseg`

## Training Models
Train the segmentation models we need for running Vollseg notebooks, you can also optionally train a noise2void or a CARE based restoration model. 

## Model Prediction
In VollSeg setting sometimes weakness of Unet model is overcome by the denoising model, for this we have a boolean in the high level notebook, dounet = False

## Saving segmentation as csv
After doing the segmentation you can either input the segmentations with the Raw image for doing the tracking with Trackmate or for large datasets you can use BTrackmate with the csv file you created in this step. In this way only the Raw image needs to be opened in Fiji along with the csv file.

## Tracking
Our tracking solution in Fiji is called BTrackmate, to install this jar activate the update site MTrack in Fiji and then you can track growing branches of the tissue, track cells inside the tissue and then use the post analysis step to classify tracks as moving towards or away from the growing end points.

## Post track analysis
After doing tracking in Fiji the track visualization and anlysis is performed in Napari. Using our notebooks you can color code the cells with any track/spot attribute, classify tracks as random or directed and compute cell to tissue localization, perform track evaluation of GT vs automated tracks.

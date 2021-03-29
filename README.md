# Flow estimation
Code for the PyTorch implementation of "Estimating Nonplanar Flow from 2D Motion-blurred Widefield Microscopy Images via Deep Learning", submitted to IEEE ISBI, 2021

https://arxiv.org/abs/2102.07228

## Abstract
Optical flow is a method aimed at predicting the movement velocity of any pixel in the image and is used in medicine and biology to estimate flow of particles in organs or organelles. However, a precise optical flow measurement requires images taken at high speed and low exposure time, which induces phototoxicity due to the increase in illumination power. We are looking here to estimate the three-dimensional movement vector field of moving out-of-plane particles using normal light conditions and a standard microscope camera.
We present a method to predict, from a single textured wide-field microscopy image, the movement of out-of-plane particles using the local characteristics of the motion blur. We estimated the velocity vector field from the local estimation of the blur model parameters using an deep neural network and achieved a prediction with a regression coefficient of 0.92 between the ground truth simulated vector field and the output of the network. This method could enable microscopists to gain insights about the dynamic properties of samples without the need for high-speed cameras or high-intensity light exposure. 

## Requirements
The following python libraries are required. We advise the use of the conda package manager.
> numpy
> scikit-image
> pytorch
> matplotlib
> PyQt5
> pandas
> scikit-learn

For example, you can install all the requirements by using
> conda install --file requirements.txt

## Generating training dataset
Launch the file `generate_training_set.py` with the according parameters

## Training
Launch `train.py` and modify the parameters to match the training set folder.

## Deconvolution
The code for deconvolution is in the separate directory `https://github.com/idiap/semiblindpsfdeconv`

## Generating figures and tables
The benchmark table is in file `benchmark_models.py`; noise resistance figure in `figure_noise_resistance.py`, and the depth-from-focus figure in `figure_depth.py`

## Citation
For any use of the code or parts of the code, please cite:

@article{shajkofci_spatially-variant_2020,
  ids = {shajkofci\_spatially-variant\_2020},
  title = {Spatially-{{Variant CNN}}-{{Based Point Spread Function Estimation}} for {{Blind Deconvolution}} and {{Depth Estimation}} in {{Optical Microscopy}}},
  author = {Shajkofci, Adrian and Liebling, Michael},
  date = {2020},
  journaltitle = {IEEE Transactions on Image Processing},
  volume = {29},
  pages = {5848--5861},
  issn = {1941-0042},
  doi = {10.1109/TIP.2020.2986880},
  eventtitle = {{{IEEE Transactions}} on {{Image Processing}}},
  keywords = {blind deconvolution,Calibration,convolutional neural networks,Deconvolution,depth from focus,Estimation,Microscopy,Optical diffraction,Optical imaging,Optical microscopy,point spread function estimation}
}


## Licence
This is free software: you can redistribute it and/or modify it under the terms of the BSD-3-Clause licence.

# 📌 Code Availability

# The source code will be released upon acceptance of the manuscript submitted to *Scientific Reports*.

# CTINet: A Feature Interaction Network Integrating Transformer Modules for Partial-to-Partial Point Cloud Registration


## Abstract
Point cloud registration is a critical task in computer vision and robotics. Existing partial-overlap registration methods typically rely heavily on the precise estimation of overlapping regions; consequently, poor overlap extraction significantly degrades registration accuracy. To address this limitation, this paper proposes CTINet, a novel partial-to-partial registration method that eliminates the need for overlap detection or explicit mask estimation by incorporating multi-level feature interactions between the source and reference point clouds directly into the convolutional feature extraction stage. Specifically, CTINet employs a dual-branch feature interaction network, embedding multiple data-association modules within the feature extraction process to enhance inter-cloud correlations. Furthermore, these modules integrate both self-attention and cross-attention mechanisms, further improving feature alignment accuracy. Comparative experimental results demonstrate that CTINet outperforms OMNet—the top-performing baseline among seven evaluated methods—achieving reductions of approximately 8.86%, 18.1%, and 22.7% in RMSE(R), Error(R), and Error(t), respectively.

## Local Installation

Tested in the following environments:
* Ubuntu 22.04
* Python 3.8


## Dependencies

* coloredlogs==15.0.1
* h5py==3.5.0
* megengine==1.7.0
* numpy==1.21.4
* scipy==1.7.2
* tensorboardX==2.4
* termcolor==1.1.0
* tqdm==4.62.3
* transforms3d==0.3.1
* scikit-learn>=0.21.3
* torch==2.1.2

## Data

we use the OS and TS data of the ModelNet40 dataset.


## Training and Evaluation

### Begin training

you can just run:

```
python3 train.py --model_dir=./experiments/experiment_ModelNet40/
```

### Begin testing

you can just run:

```
python3 evaluate.py --model_dir=./experiments/experiment_ModelNet40 --restore_file=./experiments/experiment_ModelNet40/test_model_best.pth
```

## Acknowledgments

In this project we use (parts of) the official implementations of the following works:

* [RPMNet](https://github.com/yewzijian/RPMNet) (ModelNet40 preprocessing and evaluation)

We thank the authors for open sourcing their methods.

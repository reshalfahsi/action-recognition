# Action Recognition Using CNN + Bidirectional RNN


<div align="center">
    <a href="https://colab.research.google.com/github/reshalfahsi/action-recognition/blob/master/Action_Recognition.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="colab"></a>
    <br />
</div>


Given a video, we can undergo recognition or analysis to decide what action occurred in the clip. By nature, videos are a sequence of frames. Consequently, performing action recognition on video deals with processing spatio-temporal data. Here, we can make use of the HMDB51 dataset, consisting of 6k+ clips of 51 actions. This dataset has three separate train/test splits. Striving for simplicity, this project utilizes the first training split as the training set, the second testing split as the validation set, and the third testing split as the testing set. Regarding the action recognition model, CNN is customarily adopted to extract spatial information. Thus, a CNN architecture, MnasNet, is put into use. Next, to handle the temporal information, bidirectional RNN is employed. Succinctly, the action recognition model in this project is composed of CNN and bidirectional RNN.


## Experiment

Please take a look at this [notebook](https://github.com/reshalfahsi/action-recognition/blob/master/Action_Recognition.ipynb) to see the recognition in action.


## Result

## Quantitative Result

The following table conveys the quantitative performance of the model.

Test Metric  | Score
------------ | -------------
Loss         | 0.753
Accuracy     | 88.39%


## Loss and Accuracy Curve

<p align="center"> <img src="https://github.com/reshalfahsi/action-recognition/blob/master/assets/loss_curve.png" alt="loss_curve" > <br /> The loss curve on the (first) training split and the validation set (the second testing split) of the CNN + Bidirectional RNN model. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/action-recognition/blob/master/assets/acc_curve.png" alt="acc_curve" > <br /> The accuracy curve on the (first) training split and the validation set (the second testing split) of the CNN + Bidirectional RNN model. </p>


## Qualitative Result`

Here is a compilation of several video clips with an in-frame caption tailored to their predicted and actual actions.

<p align="center"> <img src="https://github.com/reshalfahsi/action-recognition/blob/master/assets/result.gif" alt="qualitative" > <br /> The action recognition results of the CNN + Bidirectional RNN model. Several actions are shown in the compilation video: <i>brush hair</i>, <i>throw</i>, <i>dive</i>, <i>ride bike</i>, and <i>swing baseball.</i> </p>


## Credit

- [Video Classification with a CNN-RNN Architecture](https://keras.io/examples/vision/video_classification/)
- [Bidirectional Recurrent Neural Networks](https://ieeexplore.ieee.org/document/650093)
- [MnasNet: Platform-Aware Neural Architecture Search for Mobile](https://arxiv.org/pdf/1807.11626.pdf)
- [HMDB: A Large Video Database for Human Motion Recognition](https://serre-lab.clps.brown.edu/wp-content/uploads/2012/08/Kuehne_etal_iccv11.pdf)
- [MoViNet-pytorch](https://github.com/Atze00/MoViNet-pytorch)
- [Gluon CV Toolkit HMDB51 Dataset](https://github.com/dmlc/gluon-cv/blob/master/gluoncv/data/hmdb51/classification.py)
- [Forked Torchvision by Henry Xia](https://github.com/ehnryx/vision/tree/be6f398c0612c245b0019a286a99f80aca81de7d/torchvision/transforms)
- [PyTorch Lightning](https://lightning.ai/docs/pytorch/latest/)

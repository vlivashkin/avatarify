![](docs/img/mona.gif)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/alievk/avatarify/blob/master/avatarify.ipynb)
[<img src="https://img.shields.io/badge/slack-join-brightgreen?style=flat&logo=slack">](https://join.slack.com/t/avatarify/shared_invite/zt-dyoqy8tc-~4U2ObQ6WoxuwSaWKKVOgg)

:arrow_forward: [Demo](https://youtu.be/Q7LFDT-FRzs)

:arrow_forward: [AI-generated Elon Musk](https://youtu.be/lONuXGNqLO0)

# Avatarify

Photorealistic avatars for video-conferencing [apps](#configure-video-meeting-app). Democratized.

Based on [First Order Motion Model](https://github.com/AliaksandrSiarohin/first-order-model).

See our [Install and run](https:/alievk.github.io/avatarify) guide for more details.

## News
- **22 May 2020.** Added [Google Colab](https://colab.research.google.com/github/alievk/avatarify/blob/master/avatarify.ipynb) mode. Now you can running Avatarify on any computer without GPU!
- **7 May 2020.** Added remote GPU support for all platforms (based on [mynameisfiber's](https://github.com/mynameisfiber) solution). [Demo](https://youtu.be/3Dz_bUIPYFM). Deployment [instructions](https://github.com/alievk/avatarify/wiki/Remote-GPU). 
- **24 April 2020.** Added Windows installation [tutorial](https://www.youtube.com/watch?v=lym9ANVb120).
- **17 April 2020.** Created Slack community. Please join via [invitation link](https://join.slack.com/t/avatarify/shared_invite/zt-dyoqy8tc-~4U2ObQ6WoxuwSaWKKVOgg).
- **15 April 2020.** Added [StyleGAN-generated](https://www.thispersondoesnotexist.com) avatars. Just press `Q` and now you drive a person that never existed. Every time you push the button – new avatar is sampled.
- **13 April 2020.** Added Windows support (kudos to [9of9](https://github.com/9of9)).

## Requirements

You can run Avatarify in two modes: *locally* and *remotely*.

To run Avatarify *locally* you need a CUDA-enabled (NVIDIA) video card. Otherwise it will fallback to the central processor and run very slowly. These are performance metrics for some hardware:

- GeForce GTX 1080 Ti: **33 frames per second**
- GeForce GTX 1070: **15 frames per second**
- GeForce GTX 950: **9 frames per second**

You can also run Avatarify *remotely* on [Google Colab](https://colab.research.google.com/github/alievk/avatarify/blob/master/avatarify.ipynb) (easy) or on a [dedicated server](https://github.com/alievk/avatarify/wiki/Remote-GPU) with a GPU (harder). There are no special PC requirements for this mode, only a stable internet connection.

Of course, you also need a webcam!

<!-- * [conda Python 3.7](https://docs.conda.io/en/latest/miniconda.html)
* [CUDA](https://developer.nvidia.com/cuda-downloads) -->

## Install and run
See the [Install](https:/alievk.github.io/avatarify/#/?id=install) and [Run](https:/alievk.github.io/avatarify/#/?id=run) sections of guide.

## Setup avatars
Avatarify comes with a standard set of avatars of famous people, but you can extend this set simply copying your avatars into `avatars` folder.

Follow these advices for better visual quality:
* Make square crop of your avatar picture.
* Crop avatar's face so that it's not too close not too far. Use standard avarars as reference.
* Prefer pictures with uniform background. It will diminish visual artifacts.

## Configure video meeting app

Avatarify supports any video-conferencing app where video input source can be changed (Zoom, Skype, Hangouts, Slack, ...). Here are a few examples how to configure particular app to use Avatarify.

### Skype

Go to Settings -> Audio & Video, choose `avatarify` (Linux), `CamTwist` (Mac) or `OBS-Camera` (Windows) camera.

<img src=docs/img/skype.jpg width=600>

### Zoom

Go to Settings -> Video and choose `avatarify` (Linux), `CamTwist` (Mac) or `OBS-Camera` (Windows) from Camera drop-down menu.

<img src=docs/img/zoom.jpg width=600>

### Teams

Go to your profile picture -> Settings -> Devices and choose `avatarify` (Linux), `CamTwist` (Mac) or `OBS-Camera` (Windows) from Camera drop-down menu.

<img src=docs/img/teams.jpg width=600>

### Slack

Make a call, allow browser using cameras, click on Settings icon, choose `avatarify` (Linux), `CamTwist` (Mac) or `OBS-Camera` (Windows) in Video settings drop-down menu.

<img src=docs/img/slack.jpg width=600>


## Contribution

Our goal is to democratize photorealistic avatars for video-conferencing. To make the technology even more accessible, we have to tackle the following problems:

* ~~Add support for more platforms (Linux and Mac are already supported).~~
* ~~Remote GPU support. This is a work in progress.~~
* Porting to non-CUDA GPUs (Intel integrated GPUs, AMD GPUs, etc) and optimization. The goal is to run Avatarify real-time (at least 10FPS) on modern laptops.

Please make pull requests if you have any improvements or bug-fixes.

## Troubleshooting

Please follow the [Wiki](https://github.com/alievk/avatarify/wiki/Troubleshooting) page.

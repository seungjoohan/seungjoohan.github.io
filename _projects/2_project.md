---
layout: page
title: Pose with Vision Transformers
description: experimenting pose models with vision transformers
img: assets/img/skel.webp
importance: 2
category: work
---

As people say how universal the vision transformers are, I am trying the pose estimation model with the vision transformer. 
I first started finetuning with DinoV2 backbone provided by Meta AI, but I am trying to add different transformers as well - FastViT by Apple implemented and more coming! Currently the model performances are not there to compare with CNN based pose models, but I'll keep going. You can take a look at the code [here](https://github.com/seungjoohan/dino_pose). I've also integrated custom Low Rank Adaptation(LoRA) models to optimizie finetuning.

Skills involved:
 - PyTorch
 - Vision Transformer
 - Pose Estimation
 - Low-Rank Adaptation

<!-- TODO: IMAGE of pose -->

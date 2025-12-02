---
layout: page
title: Web GUI based DNN Modeler
description: build with ease
img: assets/img/flow-chart.jpg
importance: 1
category: work
---

From my endeavor to modify and improve neural network model, I've experienced extreme frustration due to inconvenience of model building - training - testing cycle with limited resources. If you possess extensive resources, none of this matters! But if you are working on personal project or you have limited resources, one failed experiment costs too much.

So, I am trying to build a FREE neural network modeling tool based on web GUI with drag-and-drop interface. This modeler will come with following features:
_ Build / Modify existing model from web interface
_ Train model for few epochs with provided/custom data
_ Display validation results
_ Save and export the model / model building code

Still in progress at [dnn-modeler](https://github.com/seungjoohan/dnn-modeler)

Since the tool will only utilize free resources at the moment, it's not ideal for large scale network modeling. Building the model will face no interference even for the big model, but the resources will not be sufficient to train unless you come with the extensive resources. I recommend testing modules in your model if your model is big!

Skills involved:

- ML: Pytorch
- DevOps:
  - Backend: FastAPI
  - CI/CD:
  - Version Control:
  - Containerization:
- Web: React

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/modeler.jpg" title="working progress of dnn modeler" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

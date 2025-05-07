---
layout: page
title: 3d Pose Estimation
description: showcasing 3d pose estimation model
img: assets/img/skeleton.png
importance: 1
category: work
---

I am hereby presenting what I was able to achieve with 3D pose estimation at ViFive. You can test with your own image/camera [here](https://pose-estimation-app-974323386375.us-central1.run.app/) - though the app might take some time to load as I deployed using free resources!

Be mindful to use clear image/video to test the model. As I removed all pre & post processing, the model might struggle to locate you. I attached some test videos from myself.

Let's take a look at the front view of me walking.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/walking-front.jpg" title="walking image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>    
<div class="caption">
    Frontal view of my walking pose.
</div>
<div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/walking-front-inf.png" title="walking side inf image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Model estimates depth, so I can look at model's prediction of how my walking pose looks like from side view.
</div>

---
layout: page
title: Stock prediction system
description: let's predict stock prices!
img: assets/img/stock.jpg
importance: 2
category: work
---

This is my personal project to study ML system. You can check out the stock prediction app deployed [stock prediction system](https://itydvee55cjn8mbcjn3y4t.streamlit.app/).

Skills involved:
 - ML: ARIMA, Prophet, timeseries forecasting
 - DevOps:
    - API integration: yfinance
    - CI/CD: Github Actions
    - Version Control: Git
    - Containerization: Docker (Streamlit cloud community)
 - Web: Streamlit

Currently, my focus is developing the architecture where the system is self-sustainable. By self-sustainable, I mean entire ML system including the data flow, ML model building, and maintaining the models is done without any human intervention. Currently, data and model are updated every night for them to be ready to predict stocks tomorrow with the most current data.

Since my main goal is to study and develop the system than to come up with very accurate model, the model is not reliable. Otherwise, I'd be trading to earn money rather than building the app!

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/stock-prediction.gif" title="stock prediction app demo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The app is deployed with Streamlit
</div>


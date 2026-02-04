---
layout: page
title: ProPINGquity
description: SNS to make real connections
img: assets/img/ping-icon.png
importance: 1
category: work
app_url: https://testflight.apple.com/join/h3ssEK8c
---

Living in New York City, the toughest aspect of New Yorkers for me to get accustomed to was making an appointment with a friend to grab a dinner or a beer together. I prefer to text a friend "let's grab a dinner tonight" than to text "let's grab a dinner this friday at 6pm".

I know I'm spontaneous and I've built an app, ProPINGquity, to satisfy my needs. Through the app, you can:
* Ping at your location to find out who's nearby
* Connect and chat
* Find places to go
* Get recommendation on where to meet

Join me for beta testing and connect with friends!

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/proximity.png" title="ProPINGquity screenshot" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Technical Highlights:
* Real-time location sharing: Friends can see each other's live location on an interactive map with customizable visibility settings
* WebSocket-based chat: Instant messaging with read receipts, typing indicators, and media sharing
* Google Places integration: Search places, browse by category, view ratings, photos, and contact info
* Push notifications: Stay connected with real-time alerts for ping, messages, and friend requests
* Privacy-first design: Contact information is encrypted at rest and never shared with third parties

Tech Stack:
* Frontend: React Native (Expo), TypeScript
* Backend: FastAPI (Python)
* Database: Firebase Firestore
* Auth: Firebase Authentication
* Storage: Google Cloud Storage
* Maps: Google Maps Platform (Maps SDK, Places API, Directions API)
* Real-time: WebSockets, Firebase Cloud Messaging    

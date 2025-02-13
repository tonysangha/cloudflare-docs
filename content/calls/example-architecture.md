---
pcx_content_type: get-started
title: Example architecture
weight: 10
---

# Example architecture for a video calling app

<div class="full-img">

![Example Architecture](/images/calls/video-calling-application.png)

</div>

1. Clients connect to the backend service
2. Backend service manages the relationship between the clients and the tracks they should subscribe to
3. Backend service contacts the Cloudflare Calls API to pass the SDP from the clients to establish the WebRTC connection.
4. Calls API relays back the Calls API SDP reply and renegotiation messages.
5. If desired, headless clients can be used to record the content from other clients or publish content.
6. Admin manages the rooms and room members.

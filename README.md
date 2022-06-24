[Twitch VOD Sync](https://remram44.github.io/twitch-vod-sync/)
==============================================================

This is a web application that can show multiple recorded videos from Twitch, syncing them exactly.

If you want to see the streams of multiple people playing together, applications like [MultiTwitch.tv](http://www.multitwitch.tv/) ([GitHub](https://github.com/bhamrick/multitwitch)) or Twitch's own "Squad Stream" mode can help. However if you are watching the streams after the fact (or after the event) or if the streams are not exactly synced (because they use different delays, common in competitions) it won't work.

This application can bring up multiple VOD (recorded streams), obtain their starting date from the API, and show them in perfect sync. You will still need to input the appropriate delay for each stream if different.

**[Head over here to get started](https://remram44.github.io/twitch-vod-sync/)**

Current status
--------------

This project is pretty much done! Suggestions and patches welcome.

* [x] Show the **real timestamp** while playing Twitch videos (obtained from API)
* [x] Show multiple Twitch videos in the same browser tab
  * [x] Show more than 2
* [x] Play the streams synced
  * [x] Account for streams using different delays
* [x] Pause button to pause all streams
* [ ] Detect if users acts on a stream directly (rather than with the timeline at the bottom) and do something about it [#8](https://github.com/remram44/twitch-vod-sync/issues/8)

FAQ
---

### Why do I need to give access to my Twitch account?

Unfortunately I can only get the creation date for a video from the API, not the embed system, and the API needs authorization. Note that I am requesting no permissions on your account, I just query the video API on your behalf. This is also a static web app so I am not collecting the access token (it stays in your browser).

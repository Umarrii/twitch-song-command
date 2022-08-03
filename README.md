# Twitch Song Command

These are instructions on how to set up a song command via Nightbot on Twitch for streamers who use multiple different music streaming platforms.

This can be done using last.fm with a browser extension that tells last.fm what song you're listening to. This is something the streamer will need to set up.

So first you need to create a last.fm account and verify your email: <https://www.last.fm/join>

Then you need to download the Web Scrobbler extension: <https://web-scrobbler.com/>

Next you go to the extension options to connect your last.fm account to it. How you get to the options varies depending on which browser you use. On Chrome just right click the icon and select Options, then under Accounts click Sign in and allow access:

[![Connect last.fm account to Web Scrobbler extension](<https://i.imgur.com/S0FlIQ1.png>)](<https://i.imgur.com/S0FlIQ1.png>)

Back in the extension options, you can enable:

- "Force track recognition" (if the extension can't recognise the song, it will try to get what information it can from page and use that instead)
- "Scrobble videos from "Music" category"

[![Web Scrobbler extension options](<https://i.imgur.com/GDi8PJD.png>)](<https://i.imgur.com/GDi8PJD.png>)

Further down you can also set it to only work on the services you use, like Spotify, YouTube, Soundcloud etc.

If you use the Spotify program instead of the web app, you need to connect your Spotify account to your last.fm account: <https://www.last.fm/settings/applications>
[![Connect Spotify to last.fm account](<https://i.imgur.com/RIk9A7O.png>)](<https://i.imgur.com/RIk9A7O.png>)

Then for the nightbot command, it's just something like this:

```text
@$(touser) -> Now Playing: $(lastfm username)
```

So for me the command would be `@$(touser) -> Now Playing: $(lastfm Umarrii)`

This should be enough but you can further customise the format of the command if you'd like: <https://docs.nightbot.tv/variables/lastfm>

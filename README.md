# Last.fm / ListenBrainz Overlay for OBS

This overlay allows you to show what song you're currently listening to on your stream. It's made especially for software like OBS to add functionality to your stream. This solution is much more elegant than telling your viewers the name of every song you're listening to or requiring your users to call a bot. It's also really flexible if you know a bit of CSS and HTML.

To work out what you're playing from pretty much anywhere, you just need an account with either [last.fm](https://last.fm) (recommended) or [ListenBrainz](https://listenbrainz.org). You can make the widget update every x seconds to get realtime updates.

This is an updated, more flexible version of [Mitch Canter's](https://github.com/thatmitchcanter/twitch-overlay-for-spotify) widget.

## Setting Up The Overlay

Prerequisites for setting up the overlay:
- a last.fm or ListenBrainz account
- (if you're using last.fm) an API key. Get your API key once you've signed up for an account [here](https://www.last.fm/api/account/create).
- your streaming service(s) connected to last.fm or ListenBrainz. There's instructions available [here for last.fm](https://www.last.fm/about/trackmymusic).

1. [Download the project](https://github.com/dylmye/lastfm-overlay/archive/master.zip) and host it on a web server or put it somewhere on your computer.
2. Rename `index.example.html` to `index.html`. There are 4 settings in this file that you will need to be aware of to make this overlay work for you:

| Variable Name | Possible Values | Meaning                                                 |
| ------------- | --------------- | ------------------------------------------------------- |
| api           | Text            | (Optional, required for last.fm) Your last.fm API key   |
| username      | Text            | Your last.fm or ListenBrainz username                   |
| time          | Number          | How many seconds to wait before checking what's playing |
| is_lastfm     | `true`/`false`  | Whether to use last.fm or ListenBrainz                  |
3. In OBS, add a new ['browser' source](https://obsproject.com/wiki/Sources-Guide#browsersource). Check the box that says 'Local File' if you are hosting the file on your machine. Enter the file location in the 'URL' box, and set the Width to 195, Height to 225. Feel free to tweak this as necessary.
4. Open your music app of choice and start playing. Everything should begin displaying on the first song change.

## Notes

* ListenBrainz can be slow to update, or not update at all. Last.fm is highly recommended.
* Apps that don't share listening status between devices like Tidal may show music from the wrong account. Spotify works best with this.

## Roadmap

* multiple view options (vertical, with album cover)
* responsive version
* add images to setup section

## Disclaimers

This product is not endorsed, affiliated, made or supported by The MetaBrainz Foundation, Last.fm or CBS Interactive. It's built on public APIs. You agree that you are liable for your use of the Last.fm API, not the developers of this product.

![Powered by audioscrobbler](powered-by-audioscrobbler.png)
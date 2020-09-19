# Last.fm Overlay for OBS

This is a dead-simple overlay for OBS and similar applications that uses [last.fm](https://last.fm) to scrobble the track titles and display them in a minimalistic way. This overlay is super customisable with simple knowledge of CSS and HTML. You can show what you're playing in any music application that works with last.fm!

This is an updated, simpler version of [Mitch Canter's](https://github.com/thatmitchcanter/twitch-overlay-for-spotify) widget.

This product is not endorsed, affiliated, made or supported by Last.fm or CBS Interactive. It's built on its public API. You agree that you are liable for your use of the Last.fm API, not the developers of this product.

## Setting Up The Overlay

0. For this you will need:
- a last.fm account (sign up for one [here](https://www.last.fm/join))
- an API key from last.fm. Get your API key (once you've signed up for an account) [here](https://www.last.fm/api/account/create)
- your streaming service(s) connected to last.fm. There's instructions available [here](https://www.last.fm/about/trackmymusic). Note with Tidal that you'll need to connect it on every Tidal app you use (iOS, mac, windows, etc.)

1. Download the script and install it on a web server or your local hard drive - either should work.
2. Create a copy of index.example.html and rename it to index.html. Open index.html and edit the 'api', 'username', and 'time' variables - those will need to be filled in to your specific needs (the time variable is how often the script checks for a song change - I usually keep it at 2 seconds, but if you want to adjust it, feel free).
3. In OBS, add a new ['browser' source](https://obsproject.com/wiki/Sources-Guide#browsersource). Check the box that says 'Local File' if you are hosting the file on your machine. Enter the file location in the 'URL' box, and set the Width to 195, Height to 225. Feel free to tweak this as necessary.
4. Open your music app of choice and start playing. Everything should begin displaying on the first song change.

## Roadmap

* multiple view options (vertical, with album cover)
* better documentation
* responsive version
* add images to setup section

![Powered by audioscrobbler](powered-by-audioscrobbler.png)
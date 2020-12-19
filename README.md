# YouTubuddy
## Search/Watch/Download YouTube videos with a lightweight, interactive tool

![2020-12-15-220913_1920x1080_scrot](https://user-images.githubusercontent.com/54716352/102304904-3d9cf080-3f24-11eb-9d66-a7e3a75b88fb.png)

- Simple
  - Does not need a web browser to operate
  - One `bash` script that runs everything
  - Based on `youtube-dl`
  - Minimal dependencies
  - Minimal size: less than 500 KB total
- Secure
  - YouTube can't track you
  - Videos won't appear in your browsing history
- Flexible
  - Add your own flags to VLC and youtube-dl. For example, make VLC repeat the playlist, or play in fullscreen
- Awesome
  - Supports playlists, direct links, and searches
  - Displays video thumbnails and tooltips in search results
  - Allows selecting multiple videos from a list
  - Easily Download multiple videos with a single click
  - Play all selected videos in VLC
## To download:
```
git clone https://github.com/Botspot/youtubuddy
```

## To run:
```
~/youtubuddy/gui
```
The first time you run it, YouTubuddy takes care of dependencies and adds a menu button.
## Updating:
YouTubuddy will automatically keep itself updated with this main repo. To disable this feature, create a file at `~/youtubuddy/no-update`.

## How it works:
It turns out `youtube-dl` has [this little-known feature](https://github.com/Botspot/pi-apps/issues/116#issuecomment-743803001) that allows you to search YouTube.  
As it searches, `youtube-dl` [creates a JSON file](https://github.com/Botspot/youtubuddy/blob/51ba7a6e360888fb49a32db2d93480e6ee31cb63/gui#L201) at `~/youtubuddy/data/lastjson`.
Every new line in the file is another search result.  
Most of the rest of the script is dedicated to reading that json file and displaying the search results in a YAD dialog window.



# How to Change The Default Playback Quality?
For changing the video quality, do the following steps:
Open VLC:

    Go to tools>preferences

    Enable "All" option in settings

    In the left pane select "input/codecs" then on the right pane in "track settings" click preferred resolution option and select the video quality.

Note: This option will also degrade the video quality for all video (local, streams etc).

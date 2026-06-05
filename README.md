# mf-player

A lightweight browser-based video player designed to stream files from MediaFire and other file hosting sites without downloading them first.

## How it works

A small bookmarklet runs on any file hosting page. It finds the download link, grabs the URL, and redirects to this hosted player — passing the video URL as a query parameter. The player loads and streams the file directly in the browser.

```
Bookmarklet (on MediaFire page)
  → finds download link
  → redirects to mf-player with ?v=<url>
  → player streams the video
```

## Setup

**1. Enable GitHub Pages**

Go to Settings → Pages → set Branch to `main` → Save.

Your player will be live at:
```
https://SkuxSaint.github.io/mf-player
```

**2. Install the bookmarklet**

Create a new bookmark in your browser and paste this as the URL:

```
javascript:(function(){var a=document.querySelector('a[href*="download"]');if(!a){alert('No download link found.');return;}window.location.href='https://SkuxSaint.github.io/mf-player/?v='+encodeURIComponent(a.href)+'&from='+encodeURIComponent(window.location.href);})();
```

**3. Use it**

Navigate to a MediaFire video page (or any file host with a download link), click the bookmarklet, and the player opens automatically.

## Player features

- Theater mode - dark background, centered video
- Seek bar with scrubbing
- Volume control
- Playback speed (0.5x to 2x)
- Fullscreen
- Back button returns to the original page
- Keyboard shortcuts

## Keyboard shortcuts

| Key | Action |
|-----|--------|
| `Space` | Play / pause |
| `←` `→` | Seek back / forward 10s |
| `↑` `↓` | Volume up / down |
| `F` | Fullscreen |
| `M` | Mute / unmute |

## Testing

You can test the player directly without a file host by visiting:

```
https://SkuxSaint.github.io/mf-player/?v=https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4
```

## Compatibility

Works on any site where the download link is a plain `<a>` tag with "download" in the URL. Tested on MediaFire. May also work on WeTransfer, direct CDN links, and other basic file hosts.

## Why not just download the file?

Sometimes you just want to quickly preview a video without waiting for a full download or cluttering your downloads folder — especially for large files on slow connections.

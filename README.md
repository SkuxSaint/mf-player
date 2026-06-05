# mf-player

Stream videos from MediaFire and other file hosts directly in your browser — no downloading needed.

**Player:** [https://SkuxSaint.github.io/mf-player](https://SkuxSaint.github.io/mf-player)

---

## Install the Bookmarklet

To stream videos with a single click, add the bookmarklet to your browser:

1. Create a new bookmark in your browser.
2. Paste the following code as the **URL**:

```javascript
javascript:(function(){var a=document.querySelector('a[href*="download"]');if(!a){alert('No download link found.');return;}window.location.href='[https://SkuxSaint.github.io/mf-player/?v='+encodeURIComponent(a.href)+'&from='+encodeURIComponent(window.location.href](https://SkuxSaint.github.io/mf-player/?v='+encodeURIComponent(a.href)+'&from='+encodeURIComponent(window.location.href));})();
```

---

## How to Use

1. Go to a MediaFire page (or any file host page with a download link).
2. Click the bookmarklet.
3. The video will open in the player instantly.

---

## Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| `Space` | Play / pause |
| `←` `→` | Seek 10s |
| `↑` `↓` | Volume |
| `F` | Fullscreen |
| `M` | Mute |

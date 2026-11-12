# Instruments repo rules

Phone-first web instruments hosted on GitHub Pages (https://shawnchiki.github.io/instruments/).

- Each instrument is one self-contained `index.html` in its own folder (`sunspot/`, `substellar/`, ...).
- **No accidental zoom, ever.** Every instrument page (and the launcher) must use the full viewport meta
  (`initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no,viewport-fit=cover`) and include the
  `NO-ZOOM GUARD` block right after `<title>`. Copy it from `substellar/index.html`. It blocks iOS pinch and
  double-tap zoom, desktop ctrl/cmd+scroll and trackpad pinch, and ctrl/cmd +/-/0. Play surfaces also get
  `touch-action:none`.
- UI style: menus as icon tabs in a rail down the left side; bold, saturated colours (no pastels); uncluttered and
  beginner-clear; no standing people or figurines.
- When adding an instrument: add a card to the root `index.html` launcher and a section to `README.md`.
- Audio: AudioWorklet loaded from a Blob URL works on GitHub Pages but not from `file://`; test over a local http server.

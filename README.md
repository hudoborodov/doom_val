# doom_val

DOOM **shareware** packaged as a [js-dos](https://js-dos.com) v8 bundle, for embedding in
Supermetrics Studio dashboard boards.

`doom-shareware.jsdos` is a plain ZIP containing id Software's freely-redistributable DOOM
shareware (`DOOM.EXE` v1.9 + `DOOM1.WAD`, episode 1 "Knee-Deep in the Dead") plus a
`.jsdos/dosbox.conf` whose `[autoexec]` launches the game directly.

Served via jsDelivr:

```
https://cdn.jsdelivr.net/gh/hudoborodov/doom_val@main/doom-shareware.jsdos
```

## Why this exists

Studio boards render inside a locked-down sandbox whose CSP allows scripts and fetches only
from a fixed CDN allowlist (jsDelivr among them) and has no `worker-src`. A board therefore
runs DOOM by loading the js-dos engine and this bundle from jsDelivr, main-thread
(`workerThread: false`). See the board HTML for the exact wiring.

## Licensing

DOOM shareware is distributable free of charge (episode 1 only); the registered episodes are
not included. `DOOM1.WAD` sha256 `1d7d43be501e67d927e415e0b8f3e29c3bf33075e859721816f652a526cac771`.

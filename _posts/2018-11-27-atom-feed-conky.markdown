<link rel="stylesheet" href="/css/zenburn.css">
<script src="/js/highlight.pack.js"></script>
<script>hljs.initHighlightingOnLoad();</script>
My conky atom feed

<img src="https://skandyns.github.io/img/atom-feed.png"/>

conky
```
Atom feed BunsenLabs
--------------------
${execi 300 $HOME/.config/conky/scripts/atomfeed.sh}
--------------------
```
atomfeed.sh
```
#!/bin/bash
URL="https://forums.bunsenlabs.org/extern.php?action=feed&type=atom"
curl -s "$URL" | grep "<title" | grep -o -P '(?<=CDATA\[).*(?=\]\])'| tail -n +2 | head -n 7 | sed 's/^//'
```

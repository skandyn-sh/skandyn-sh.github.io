<link rel="stylesheet" href="/css/solarized-dark.css">
<script src="/js/highlight.pack.js"></script>

My conky atom feed

<img src="https://skandyns.github.io/img/atom-feed.png"/>

conky
<pre><code class="html">Atom feed BunsenLabs
--------------------
${execi 300 $HOME/.config/conky/scripts/atomfeed.sh}
--------------------</code></pre>

atomfeed.sh

<pre><code class="plaintext">#!/bin/bash
URL="https://forums.bunsenlabs.org/extern.php?action=feed&type=atom"
curl -s "$URL" | grep "<title" | grep -o -P '(?<=CDATA\[).*(?=\]\])'| tail -n +2 | head -n 7 | sed 's/^//'</code></pre>

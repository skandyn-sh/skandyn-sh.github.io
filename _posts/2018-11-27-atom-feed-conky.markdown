My conky atom feed

<img src="https://skandyns.github.io/img/atom-feed.png"/>


<pre><code class="nohighlight">Atom feed BunsenLabs
--------------------
${execi 300 $HOME/.config/conky/scripts/atomfeed.sh}
--------------------</code></pre>


conky
<pre><code class="html">Atom feed BunsenLabs
--------------------
${execi 300 $HOME/.config/conky/scripts/atomfeed.sh}
--------------------</code></pre>


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

<link rel="stylesheet" href="/css/solarized-dark.css">
<script src="/js/highlight.pack.js"></script>
<script>hljs.initHighlightingOnLoad();</script>


<pre><code class="plaintext">#!/bin/bash
URL="https://forums.bunsenlabs.org/extern.php?action=feed&type=atom"
curl -s "$URL" | grep "<title" | grep -o -P '(?<=CDATA\[).*(?=\]\])'| tail -n +2 | head -n 7 | sed 's/^//'</code></pre>


<pre><code class="nohighlight">#!/bin/bash
URL="https://forums.bunsenlabs.org/extern.php?action=feed&type=atom"
curl -s "$URL" | grep "<title" | grep -o -P '(?<=CDATA\[).*(?=\]\])'| tail -n +2 | head -n 7 | sed 's/^//'</code></pre>


my conky atom feed

<img src="https://skandyns.github.io/img/atom-feed.png"/>

conkyrc
```
Atom feed BunsenLabs
--------------------
${execi 300 $HOME/.config/conky/scripts/atomfeed.sh}
--------------------
```
atomfeed.sh
```bash
#!/bin/bash
URL="https://forums.bunsenlabs.org/extern.php?action=feed&type=atom"
curl -s "$URL" | grep "<title" | grep -o -P '(?<=CDATA\[).*(?=\]\])'| tail -n +2 | head -n 7 | sed 's/^//'
```
<pre><code class="plaintext">#!/bin/bash
URL="https://forums.bunsenlabs.org/extern.php?action=feed&type=atom"
curl -s "$URL" | grep "<title" | grep -o -P '(?<=CDATA\[).*(?=\]\])'| tail -n +2 | head -n 7 | sed 's/^//'</code></pre>
  
  
<pre><code class="nohighlight">#!/bin/bash
URL="https://forums.bunsenlabs.org/extern.php?action=feed&type=atom"
curl -s "$URL" | grep "<title" | grep -o -P '(?<=CDATA\[).*(?=\]\])'| tail -n +2 | head -n 7 | sed 's/^//'</code></pre>  

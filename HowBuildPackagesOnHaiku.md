**1. Getting pkgsrc**<br>
The procedure of getting pkgsrc source code is written in detail in the official WiKi page <a href='https://www.pkgsrc.org/'>get pkgsrc</a><br><br>


<b>2. Building bootstrap</b><br>
Building bootstrap on Haiku doesn't differ much from other systems. The only thing you need to remember is to use "--unprivileged" argument:<br>
<pre><code>~&gt; bootstrap --unprivileged<br>
</code></pre>
<b>3. Getting Haiku-specific patches (localpatches)</b><br>
To build packages for Haiku you need to download a set of patches that haven't been upstreamed to pkgsrc yet:<br>
<pre><code>~&gt; git clone https://github.com/diger/localpatches.git<br>
</code></pre>
<b>4. Using "localpatches" with pkgsrc</b><br>

To use these patches you need put the following lines into <i><code>"bootstrap/etc/mk.conf"</code></i>:<br>
<pre><code>....<br>
#.sinclude "/boot/home/localpatches/Haiku.mk.conf"<br>
<br>
.endif			# end pkgsrc settings<br>
</code></pre>
Adjust "/boot/home/localpatches" path to where you cloned the patches.<br><br>
Good luck!
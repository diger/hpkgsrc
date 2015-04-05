## Installing HPKGSRC ##
To begin using prebuilt packages, simply download precompiled [package manager](http://hpkgsrc.googlecode.com/files/bootstrup.tar.gz) and extract it like this:<br>
<pre><code>~&gt; wget http://download2.polytechnic.edu.na/pub4/sourceforge/h/project/hp/hpkgsrc/bootstrap_x86.zip<br>
~&gt; unzip bootstrap_x86.zip -d /<br>
</code></pre>
<i>For a number of reasons, packages are currently installed to /boot/common</i><br>
Package installation path and internal format are subject to change in the future. <br><br>
Due to "non-standard" PATH (for Haiku), the package installation path must be set in the environment (env). The easiest way is to add the following line to your<br>
<b><i>~/.bash_profile</i></b> :<br>
<pre><code>export PATH=/boot/common/bin:/boot/common/sbin:$PATH<br>
</code></pre>
This way we add the necessary directories and raise their priority.<br>
<h2>Installing packages</h2>
I'm aware of only one package repository at the moment (:-)) - <a href='http://myfreenet.ru/hpkgsrc/x86/All'>http://myfreenet.ru/hpkgsrc/x86/All</a>, therefore we will customize our installation from it. So, open the same <b><i>~/.bash_profile</i></b> and add the path to the repository:<br>
<pre><code>export PKG_PATH="http://myfreenet.ru/hpkgsrc/x86/All"<br>
</code></pre>
Well, that's all. Launch Terminal and type e.g.:<br>
<b>pkg_add mplayer</b> <br>
<b>pkg_add samba</b> <br>
<b>pkg_add ...</b> <br><br>

We will continue working on improving the port and will be looking forward to your help and support.
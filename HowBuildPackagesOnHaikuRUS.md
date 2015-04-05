**1. Получение pkgsrc**<br>
Процедура получения исходных кодов pkgsrc детально описана на страницах<br>
официального Wiki <a href='https://www.pkgsrc.org/'>get pkgsrc</a><br><br>
<b>1.1. Сборка bootstrap</b><br>
Сборка bootstrap на Haiku мало чем отличается от сборки на других системах. Единственно, о чем нужно помнить, это указание ключа "--unprivileged" или "--ignore-user-check". Например:<br>
<pre><code>~&gt; bootstrap --unprivileged<br>
</code></pre>
<b>2. Получение патчей специфичных для Haiku (localpatches)</b><br>
Для сборки пакетов на Haiku необходимо скачать набор патчей, которые не были включены в официальные проекты:<br>
<pre><code>~&gt; git clone https://github.com/diger/localpatches.git<br>
</code></pre>
<b>2.1 Использование "localpatches" с pkgsrc</b><br>
Для использование патчей достаточно указать в <i><code>"bootstrap/etc/mk.conf"</code></i>
<blockquote>следующее:<br>
<pre><code>....<br>
#.sinclude "/boot/home/localpatches/Haiku.mk.conf"<br>
<br>
.endif			# end pkgsrc settings<br>
</code></pre>
указав вместо "/boot/home/localpatches" путь, куда Вы скачали патчи.<br><br>
Желаю удачи!
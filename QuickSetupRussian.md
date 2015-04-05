## Установка HPKGSRC ##
Для того, чтобы начать использовать готовые (собранные) пакеты, достаточно скачать прекомпиленный [пакетный менеджер](http://sourceforge.net/projects/hpkgsrc/files/?source=navbar) и распаковать.
```
~> wget http://download2.polytechnic.edu.na/pub4/sourceforge/h/project/hp/hpkgsrc/bootstrap_x86.zip
~> unzip bootstrap_x86.zip -d /
```
_В данный момент, по целому ряду причин, сборка и установка пакетов происходит в /boot/common._<br>
В будущем могут измениться как пути установки, так и формат самих пакетов. <br><br>
Ввиду использования "нестандартного" для Haiku PATH, необходимо прописать путь до пакетов в окружение (env). Самый простой вариант - это добавить в<br>
<b><i>~/.bash_profile</i></b>  следующие строки: <br>
<pre><code>export PATH=/boot/common/bin:/boot/common/sbin:$PATH<br>
</code></pre>
Тем самым мы добавляем нужные нам директории и повышаем их приоритет.<br>
<h2>Установка пакетов</h2>
На данный момент мне известен только один репозиторий с пакетами (:-)) - <a href='http://myfreenet.ru/hpkgsrc/x86/All'>http://myfreenet.ru/hpkgsrc/x86/All</a>, поэтому настраивать установку мы будем именно из него. Итак, берём всё тот же <b><i>~/.bash_profile</i></b> и добавляем путь к репозиторию:<br>
<pre><code>export PKG_PATH="http://myfreenet.ru/hpkgsrc/i386/All"<br>
</code></pre>
Ну вот собственно и всё. Запускаем Terminal и пишем к примеру: <br>
<b>pkg_add mplayer</b> <br>
<b>pkg_add samba</b> <br>
<b>pkg_add ...</b> <br><br>

Работа над совершенствованием порта продолжается, надеемся на вашу помощь и поддержку.
---
title: "Клёвая подсветка синтаксиса"
date: 2013-02-03
---

По наводке одного моего товарища решил прикрутить к своему блогу подсветку синтаксиса «на лету» с помощью библиотеки [google-code-prettify](http://code.google.com/p/google-code-prettify/).

В начале, я отнесся немного скептически к идее прекрутить подсветку исходников к этому блогу, т.к. не рассматривал возможности делать это на клиенте, а серверный парсер маркдауна не мой, а GitHub'а. Следовательно, к самому парсеру я ничего своего прикрутить принципиально не могу.

Ну, а клиентский обработчик повесился без проблем.

Давайте потестируем его:

PHP:

	<?php
	function helloWorld($name)
	{
		print "Hello, world and $name";
	}
	
	helloWorld('NeonXP');

CSS:

	html, body {
		background-image: url('images/background.png');
	}
	a.link {
		color: #ff0000;
	}

Хочется надеяться, что это изменение сподвигнет меня писать посты «про программирование» гораздо чаще, раз тут такая «вкусная» подсветка.

###UPD:

По совету Ainu и Bolk'а заменил подсветку на [highlight.js](http://softwaremaniacs.org/soft/highlight/). 

В общем, стало, действительно, симпатичнее! Особенно подкупил большой выбор «скинов». На примерах выше стиль «GitHub» для аутентичности.

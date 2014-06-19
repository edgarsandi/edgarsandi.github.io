---
layout: post
categories: br posts
title: "PHP - Converter números para palavras"
description: "Como converter números para palavras com o PHP usando NumberFormatter"
tags: [php, converter número, formatar, conversão]
modified: 2012-08-21
image:
  feature: abstract-6.jpg
#  credit: dargadgetz
#  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
comments: true
share: true
---
## NumberFormatter
Hoje vamos falar sobre o NumberFormatter uma classe que faz parte do Intl (Funções de Internacionalização) desde a versão 5.0 do PHP.

Podemos usá-la para formatar números, moedas e percentuais de acordo com a localidade (L10n).

Esta classe nos dá também a possibilidade de converter número para sua forma falada.

## Exemplo de uso
* 1 = um
* 17 = dezessete
* 1985 = mil novecentos e oitenta e cinco

## Exemplo de código
{% highlight php linenos=inline %}
<?php
	$numberFormatter = new NumberFormatter('pt_BR', NumberFormatter::SPELLOUT);
	echo $numberFormatter->format(1);
	// A saída será: um

	$numberFormatter = new NumberFormatter('pt_BR', NumberFormatter::SPELLOUT);
	echo $numberFormatter->format(12345);
	// A saída será: doze mil e trezentos e quarenta e cinco
?> 
{% endhighlight %}
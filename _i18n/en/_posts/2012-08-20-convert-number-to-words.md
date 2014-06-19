---
layout: post
categories: br posts
title: "PHP - Convert number to word (spoken form)"
description: "How to convert numbers to words with PHP using NumberFormatter"
tags: [php, convert number, number to word, convertion]
modified: 2012-08-21
image:
  feature: abstract-6.jpg
#  credit: dargadgetz
#  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
comments: true
share: true
---
## NumberFormatter
Today we will talk about the NumberFormatter a class that is part of the Intl (Internationalization Functions) since version 5.0 of PHP.

We can use it to format numbers, currencies, and percentages according to location (L10n).

This class also gives us the possibility to convert number to its spoken form.

## Sample Output
* 1 = one
* 17 = seventeen
* 1985 = one thousand nine hundred eighty-five

## Sample Code
{% highlight php linenos=inline %}
<?php
	$numberFormatter = new NumberFormatter('en_EN', NumberFormatter::SPELLOUT);
	echo $numberFormatter->format(1);
	// The output will be: one

	$numberFormatter = new NumberFormatter('en_EN', NumberFormatter::SPELLOUT);
	echo $numberFormatter->format(12345);
	// The output will be: twelve thousand three hundred forty-five
?> 
{% endhighlight %}

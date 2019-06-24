---
layout: post
title: I have such a teacher and closures
date: 2019-06-23 21:28
comments: false
external-url:
categories: Rumi PHP
---

> I am a naked man standing inside a mine of rubies,
clothed in red silk.<br/><br/>I absorb the shining and now I see the ocean,<br/><br/>
billions of simultaneous motions<br/><br/>
moving in me.

Excerpt from **I have such a teacher** by Rumi

Closures
```php
> php --interactive
Interactive shell

php > $closure = function () {return 6;};
php > $base = $closure() -1;
php > print $base - 2*$base;
-5
```

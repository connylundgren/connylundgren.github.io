---
author: connylundgren
date: '2007-08-13 10:15:52'
layout: post
title: 'SVN, Fix "Can''t convert string from ''UTF-8'' to native encoding:" '
comments: true
---

Well getting back from vacation I tried to update one of my subversion
repositories, and I were once more met with the "Can't convert string from
'UTF-8' to native encoding:" , luckily it is easily fixed. This problem is
caused by filename containing "special" characters (in my case Swedish ÅÄÖ).

> [conlun@mbp:/]$ export LC_CTYPE=en_US.UTF-8

Verify you changes by running

> [conlun@mbp:/]$ locale LANG= LC_COLLATE="C" LC_CTYPE="en_US.UTF-8"
LC_MESSAGES="C" LC_MONETARY="C" LC_NUMERIC="C" LC_TIME="C"
LC_ALL="C/en_US.UTF-8/C/C/C/C"


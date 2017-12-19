---
layout: post
title: Log searching
date: 2017-12-19 10:45:00 +08
categories: Linux
---

Sometimes error happened, we need to get related error info, but the right one always drown in the log haystack.
Recently google some, find a easy tool to mange it, Grep.

	grep "keyword" FILE -A N

grep keyword of the FILE and show N line after the match line(the is also -B option show n line before the match).  
Tested on a 70 megabytes log file, fast like a flash.

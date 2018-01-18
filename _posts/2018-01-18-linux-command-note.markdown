---
layout: post
title: Linux command note
date: 2018-01-18 14:36:00 +08
categories: Linux
---
# grep and kill process
	kill $(ps aux | grep 'keyword' | awk '{print $2}')


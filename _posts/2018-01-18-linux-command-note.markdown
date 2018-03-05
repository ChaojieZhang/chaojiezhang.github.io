---
layout: post
title: Linux command note
date: 2018-01-18 14:36:00 +08
update: 2018-03-05 17:02:00 +08
categories: Linux
---
## # use awk and xargs filter and pass arguments 

we have some data here

	cj@dev16:~$ docker image ls
	REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
	nginx-test          01                  ce26c92674b9        4 days ago          109MB
	nginx               latest              e548f1a579cf        12 days ago         109MB
	ubuntu              16.04               0458a4468cbc        5 weeks ago         112MB
	ubuntu              latest              0458a4468cbc        5 weeks ago         112MB
	hello-world         latest              f2a91732366c        3 months ago        1.85kB

### awk - use awk get column of result

	cj@dev16:~$ docker image ls | awk 'NR>1{print $3}'
	\ce26c92674b9
	e548f1a579cf
	0458a4468cbc
	0458a4468cbc

NR>1 remove first word  
$3 get column 3 words

	

### xargs

	cj@dev16:~$ docker image ls | awk 'NR>1{print $3}' | xargs 
	ce26c92674b9 e548f1a579cf 0458a4468cbc 0458a4468cbc f2a91732366c
	
	docker image ls | awk 'NR>1{print $3}' | xargs docker image rm -f

## # grep and kill process
	kill $(ps aux | grep 'keyword' | awk '{print $2}')


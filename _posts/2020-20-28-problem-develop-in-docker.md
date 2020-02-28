---
layout: post
title: Problem I got while using docker
date: 2020-02-28 01:40:00 +08
categories: Docker
---

## storage

```
    php-fpm:
        build: ./php-fpm
        volumes: 
            # php code
            - ./app/php:/opt/app/php
```

php code is clone in host, and code is executed in php-fpm container. I am going to modify php code in host,  The problem is I was useing none root user in host, and in container root is running fpm, they have diffrent access to php code.

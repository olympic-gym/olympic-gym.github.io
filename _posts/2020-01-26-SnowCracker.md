---
layout: post
title:  "SnowCracker"
date:   2020-09-21 00:10:35 +0200
subtitle: "SnowCracker to bruteforce stegsnow passwords"
background: '/img/posts/01.jpg'
---

#### SnowCracker
Snowcracker used to crack Stegsnow passwords tool can preform decompression on extracted data

#### Install
1. `pip install futures`
2. `git clone https://github.com/0xMohammed/SnowCracker.git && cd SnowCracker`

#### Usage

* Without decompression `python3 snowcracker.py -C N -f flag.txt -w wordlist`
* With decompression `python3 snowcracker.py -C Y -f flag.txt -w wordlist`

![Snow-Cracker Usage](https://github.com/0xMohammed/SnowCracker/blob/master/Images/example.jpeg)

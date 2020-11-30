---
layout: post
title:  "'Last human' writeup CyberTalents DF CTF"
date:   2020-11-30 00:10:35 +0200
subtitle: "writeup for last human challange in Digital Forensics CTF by CyberTalents"
background: "/img/bg1.png"
---

#### Description
This Stream is so weird, looking something hidden here!!
Diffculity: Hard
#### Reference
#### Walkthrough
Challange is a wave file with high pitched noise, After examining file with usual tools (binwalk, exiftool, strings,..etc) we found nothing so we should dig deeper.
* Step 1: Analyze frame of wav file
1. Using the following code we could get frame values 
            {% highlight c %}
            import wave, struct
            wavefile = wave.open('data.wav', 'r')
            tmp=[]
            length = wavefile.getnframes()
            print(length)
            for i in range(0, length):
               wavedata = wavefile.readframes(1)
               data = struct.unpack("<h", wavedata)
               print(data[0])
               {% endhighlight %}

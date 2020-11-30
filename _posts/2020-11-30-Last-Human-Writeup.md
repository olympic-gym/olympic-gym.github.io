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
   1. `import wave, struct`   
   2. `wavefile = wave.open('data.wav', 'r')`   
   3. `tmp=[]`   
   4. `length = wavefile.getnframes()`   
   5. `print(length)`   
   6. `for i in range(0, length):`   
         7. `wavedata = wavefile.readframes(1)`   
         8. `data = struct.unpack("<h", wavedata)`   
         9. `print(data[0])`   

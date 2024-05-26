---
title: Fly Away 1 - NahamconCTF 2024
date: 2024-05-26
categories: [CTF Writeups]
tags: [CTF, NahamconCTF 2024, Mobile, Curl]
---

NahamCon CTF 2024

*Lenny Kravitz lovers, this new app cleverly named "Fly Away!" can give you random lines from one of his most popular songs. Can you figure out how the songs are being sent to the app?*

## Writeup
Upload the apk to virus total, go to behavior  tab and extend the HTTP Request dropdown in the Network Communication section

![Virus Total Upload](../assets/nahamconctf2024/flyaway1_virustotal.png)



**Flag is obtained after performing a curl request to the following url and requests headers.**

![Request Headers](../assets/nahamconctf2024/flyaway1_virtustotal2.png)

```bash
curl -X GET -H "Authorization: Bearer 7423509e-6de0-4b86-8398-1d5b42e5b62e"  -A "Dart/3.4 (dart:io)" http://challenge.nahamcon.com:31253/random-lyric
```

![Request Headers](../assets/nahamconctf2024/flyaway1_flag.jpg)


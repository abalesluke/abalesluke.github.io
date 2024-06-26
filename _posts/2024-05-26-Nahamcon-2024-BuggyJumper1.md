---
title: Buggy Jumper 1 - NahamconCTF 2024
date: 2024-05-26
categories: [CTF Writeups]
tags: [CTF, NahamconCTF 2024, Mobile, Godot]
---

NahamCon CTF 2024

*Buggy Jumper is a new mobile game that can be enjoyable for both gamers and hackers! There's a lot going on, can you get some of game's source code to see whats happening behind the scenes?*

## Writeup
Download the `com.nahamcon2024.buggyjumper.apk` and decompile it using apktool

```bash
apktool d com.nahamcon2024.buggyjumper.apk
```

![Decompiled APK](../assets/nahamconctf2024/buggyjumper_decompiled_apk2.png)

Looking at the scripts folder from the decompiled apk there are compiled godot scripts (_the .gdc file extensions_).

![Decompiled APK](../assets/nahamconctf2024/buggyjumper_scripts_folder.jpg)

Using [gdsdecomp a Godot Reverse Engineering](https://github.com/bruvzg/gdsdecomp) tool from github to decompile flag.gdc file.

![Decompiled APK](../assets/nahamconctf2024/decompile2.png)
![Decompiled APK](../assets/nahamconctf2024/decompile_success.png)

**Flag obtained after opening the decompiled flag.gd**

![Decompiled APK](../assets/nahamconctf2024/buggyjumper1_flag.png)

---
title: Buggy Jumper 2 - NahamconCTF 2024
date: 2024-05-26
categories: [CTF Writeups]
tags: [CTF, NahamconCTF 2024, Mobile, ADB]
---

NahamCon CTF 2024

*Buggy really wants the drip in the shop... Can you buy it for them?*

## Writeup
From the Buggy Jumper-1 I decompiled .gdc files and I also decompile the global.gdc outside the scripts folder (_which was not shown in the buggy jumper 1 writeup_).

Upon reviewing the code in global.gd, we can see that data is being saved without encrypting the values.

![Decompiled APK](../assets/nahamconctf2024/decompiled_global_script2.png)

Using ADB shell to modify the value of `saved_value.dat` in my [Genymotion](https://www.genymotion.com/product-desktop/download/) android emulator where I installed the `com.nahamcon2024.buggyjumper.apk`.

![Decompiled APK](../assets/nahamconctf2024/adb_buggyjump.png)

**Flag obtained after buying the drippy buggy in the BuggyJumper App**

![Decompiled APK](../assets/nahamconctf2024/buggy_store.png)
![Decompiled APK](../assets/nahamconctf2024/buggy_jumper2_flag.png)



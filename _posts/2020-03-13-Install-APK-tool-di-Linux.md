---
layout: post
image: 
title: Install APK tool di Linux
post_id: 1
author_name: Unang
author_id: 1
featured: true
date: 2020-03-13 8:14:30 +0600
tags: [Linux]
categories: [Tutorial]
post_image: https://drive.google.com/uc?export=download&id=1tvkeGbgF7pfg9WRAEPiR9ZsMyAfDviMh
---

Cara install APKtool di linux mint, buka terminal lalu Copy Paste Kode<!--more--> dibawah.
## Download apktool versi terbaru di [iBotPeaches](https://bitbucket.org/iBotPeaches/apktool/downloads)
<pre>
export apktool_version=2.3.1

sudo -E sh -c 'wget https://bitbucket.org/iBotPeaches/apktool/downloads/apktool_$apktool_version.jar -O /usr/local/bin/apktool.jar'

sudo chmod +r /usr/local/bin/apktool.jar

sudo sh -c 'wget https://raw.githubusercontent.com/iBotPeaches/Apktool/master/scripts/linux/apktool -O /usr/local/bin/apktool'

sudo chmod +x /usr/local/bin/apktool
</pre>

## Cara menggunakannya:
<pre>
apktool d TelephonyProvider.apk -o TelephonyProvider
</pre>
<br/>

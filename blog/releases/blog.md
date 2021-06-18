---
title: releases
content:
    items:
        - '@self.children'
    limit: 5
    order:
        by: date
        dir: desc
    pagination: true
    url_taxonomy_filters: true
published: true
date: '07-06-2021 15:39'
publish_date: '07-06-2021 15:39'
blog_url: /blog
show_sidebar: true
visible: true
---

### PWN-Term 2.2.2

##### Downloads
* [Mirror-1](https://raw.githubusercontent.com/PWN-Term/pwn-term.github.io/main/files/2.2.2.apk)
* [Mirror-2](https://anonfiles.com/N7o1b500uc/2.2.2_apk)

##### Requirements
* ARM64
* Android sdk-26+ (android 8.0)

##### Important
* This release requires clean install, so backup needed stuff to /sdcard/somewhere and move back after install
* This happened because i have used debug keys to make releases (This wont happen again, sorry)
* Rooted users can overcome it by renaming /data/data/hilled.pwnterm to something else until new app is installed (And changing it back after new app install)

##### Notes!!!
* NEEDS CLEAN INSTALL (As debug keys changed)
* In android Q+ you may need root perm to use "setenforce 0" (Only if terminal cant start up)
* To apply update for older scripts (As app won't update these automatically), do the following
rm -rf /data/data/hilled.pwnterm/files/home/.pwnterm/script/*
* And restart the app fully (Force stop)

##### Changelog (App)
* Changes for UI
* Fixed some UI problems
* Changed some colors
* More session menu changes

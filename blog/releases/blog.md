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

----

### PWN-Term 2.2.4

#### Downloads
##### ROOT \ LATEST
* [ROOT: Variant](https://github.com/PWN-Term/PWN-Term/releases/download/v2.2.3/2.2.3.apk)

* Why: Root variant is available as of changes in api 29+. Apps using api level newer than 28 have issues with exec*, meaning root is used to change SELinux status so exec* can be used again (enforcing -> permissive).

##### NON-ROOT \ LEGACY
* [NON-ROOT: Variant](https://github.com/PWN-Term/PWN-Term/releases/download/v2.2.3/2.2.3.apk)
* WHY: This release is here as this app is built with api level of 28 (Meaning exec* can be used), but - is that this app dosent use newest plugins that need api level greater than 30.
* Tradeoffs?: Older app but apt repo is same with root variant

##### Requirements
* ARM64
* Android sdk-26+ (android 8.0)

##### Important
* This release requires clean install, so backup needed stuff to /sdcard/somewhere and move back after install
* This happened because i have used debug keys to make releases (This wont happen again, sorry)
* Rooted users can overcome it by renaming /data/data/hilled.pwnterm to something else until new app is installed (And changing it back after new app install)

##### Notes!!!
* In android Q+ you may need root perm to use "setenforce 0" (Only if terminal cant start up)
* And restart the app fully (Force stop)

##### Changelog (App)
* Added more themes
* Added some new features to menu
* Changes for UI
* Fixed some UI problems
* Changed some colors

----

### PWN-Term 2.2.2

##### Downloads
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

----

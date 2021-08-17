---
title: releases
---

----
### PWN-Term Variants
* Everything here are compared against android-11 execpt Legacy that is built for android-8

* Variants with info
    - Legacy: Older version of app that is build against android-8 meaning it will have cmd exec*() available with tradeoff ( Older plugins used)
    - Root: Newer app build against android-11 with usage of root to enable exec*() but with a tradeoff ( SELinux needs to be in permissive all the times )
    - PWN-OS: Uses Root variant of app + Customized aosp where SELinux restrictions have been disabled for execmod and some other stuff.

### Additional info
* You may or may not experience app install errors (To fix it do)
    * Uninstall all pwn apps and install apps in this order
    ```
    ( pwn-term then then pwn-x11 )
    ```
    * Caused by shared app id that now these both have

---

### Downloads

---

#### NON-ROOT \ LEGACY
* [NON-ROOT: Variant](https://github.com/PWN-Term/PWN-Term/releases/download/05.08.21/2.5.5-legacy.apk)
* WHY: This release is here as this app is built with api level of 28 (Meaning exec* can be used), but - is that this app dosent use newest plugins that need api level greater than 30.
* Tradeoffs?: Older app but apt repo is same with root variant

#### PWN-Term 2.2.5 \ ROOT
* Requires rooted phone and android 8+
* [ROOT: Variant](https://github.com/PWN-Term/PWN-Term/releases/download/05.08.21/2.5.5.apk)

#### PWN-X11
* Compatible with 2.5.5 +
* [ROOTED](https://github.com/PWN-Term/PWN-Term/releases/download/05.08.21/1.0.0-x11.apk)
* [NON-ROOT](https://github.com/PWN-Term/PWN-Term/releases/download/05.08.21/1.0.0-x11-nroot.apk)

#### PWN-OS
* Beryllium (WIP): [PWN-OS / R](#)

---

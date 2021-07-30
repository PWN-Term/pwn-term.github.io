
# WIP Until Hill-ROM released

## PWN-Term Variants
---
* Everything here are compared against android-11 execpt Legacy that is built for android-8

* Variants with info
    - Legacy: Older version of app that is build against android-8 meaning it will have cmd exec*() available with tradeoff ( Older plugins used)
    - Root: Newer app build against android-11 with usage of root to enable exec*() but with a tradeoff ( SELinux disables some path in android where even root user can access)
    - Hill-ROM: Uses Root variant of app + Customized aosp where SELinux restrictions have been disabled meaning full system access.

### Features list

Features        | Legacy     | Root      | Hill-ROM
----------------|------------|-----------|----------
Regular Updates to app | No         | Yes         | Yes
Has full access of android system with root | Yes         | Partial         | Yes
Updated apt-repo | Yes         | Yes         | Yes

---
title: 'Build apk with gradle'
---

### Compiling APKs with gradle

#### README
* Gradle can only use android-build-tools version 29.0.3 as this is the only one that works for now.

#### Adding canary repo (As its beta feature still)
1. Open "package settings" menu
2. Click 3 dots and select "source"
3. Choose "new"
* For URL add: https://gitlab.com/pwn-hunter/apt-repository/-/raw/canary/
* For "New repo" add: canary main
4. Do apt update

#### Installing deps and needed sdk's
```
$ apt install gradle android-sdk-build-tools android-sdk-tools git

$ sdkmanager --update

$ sdkmanager "platforms;android-29"
```

#### Building apk from kali-nethunter-app (As example)
##### Cloning source code
```
$ home

$ git clone https://gitlab.com/kalilinux/nethunter/apps/kali-nethunter-app.git -b 2021.1 --depth=1

$ cd kali-nethunter-app

$ touch local.properties

$ echo "sdk.dir=/data/data/hilled.pwnterm/files/usr/share/android-sdk" >> local.properties
```
##### Building the app
* In first run of gradle we need to get an error with aapt2 path so lets do it
```
$ ./gradlew assemble
```
* Error shoud look like this
```
AAPT2 aapt2-(versionstring)-linux Daemon blabla
```
* In this msg get full path of aapt2 that it complains about and open new session
* Now run this in new session
```
gradle-aapt2fix -p fullpathhere
```
* Now quicly swith session to gradle build and rerun this
```
$ ./gradlew assemble
```
* Now you should have an built apk in: build/outputs/apk/(Debug or Release)/something.apk

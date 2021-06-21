---
title: Docker
---

## Docker + PWN-Term
### Requirements
* Supported device and its kernel (Kernels under kernel stuff)
* Rooted user!
* Suggestion: Min 2GB+ free space

### Supported devices (As of 15.06.2021)
* Beryllium | [Kernel](https://t.me/pwn_term/6487)
* Unified_op7 | [Kernel](https://github.com/neternels/android_kernel_oneplus_sm8150/releases/tag/NetErnels-6.0)
* Lancelot | [Kernel](https://github.com/neternels/NetHunter-Lancelot/releases/tag/v3.0)

### To enable docker support in kernel read this guide

* [Guide](https://cybernity.group/t/how-to-add-docker-support-on-android/587)

### Installation
#### Getting packages

```
$ apt install docker
```

#### Root user bash
* so sudo doesn't need to be used

```
$ clear && sudo bash
```

### Running Alpine/arm64 as of example
#### Starting dockerd
* Make new session leave it open

```
$ dockerd
```

* Or if you dont wanna have session open

```

$ dockerd &>/dev/null &
```

#### Pulling and starting session in docker
* Pulling Alpine

```
$ docker pull arm64v8/debian
```

* Logging into session (All changes will be reverted after rerunning new run)

```
$ sudo docker run -i --tty --network host arm64v8/debian
```
* Allowing internet access (Android 10+)
* Log into docker image and run

```
$ groupadd -g 3003 aid_inet && usermod -G nogroup -g aid_inet _apt
```

#### Saving changes on docker image (With docker commit)
##### Making changed container with inet perms give for example
* Starting docker image and logging in to make changes

```
$ sudo docker run -i --tty --network host arm64v8/debian

$ groupadd -g 3003 aid_inet && usermod -G nogroup -g aid_inet _apt

$ exit
```

* Listing recent changed container (Copy container ID)

```
$ docker ps -l
```

* Making new commit and starting commited container
* debian1 will be new container name (As its easy to remember)

```
$ docker commit ID_HERE debian1

$ sudo docker run -i --tty --net=host debian1

```
* And youre done
* It can be redone for committed container for further changes

#### Removing commit containers/images
* List current images (Also copy IMAGE_ID)
* NOTE: If you have done new commit on older image then that older image cant be removed!

```
$ docker images

$ docker rm IMAGE_ID
```

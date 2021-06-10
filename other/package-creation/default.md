---
title: 'package creation'
---

#### Mini guide to create custom packages for pwn-term

#### Making skeleton
1. Make empty folder and open terminal in it
2. Execute these commands
```
$ mkdir -p data/data/hilled.pwnterm/files/usr
$ mkdir DEBIAN
$ touch DEBIAN/control
$ cat <<EOF
Package: packagename
Version: 0
Architecture: aarch64
Maintainer: Hilledkinged
Installed-Size: 100
Depends: package1, package2, package3
Section: misc
Priority: optional
Homepage: https://example.com
Description: Description and leave empty line at the end
EOF
```
3. Now add the needed stuff to data/data/hilled.pwnterm/files/usr and modify control for youre needs.

#### Making deb out of skeleton
1. cd out 1 folder from skeleton and run
```
dpkg-deb --build foldername
```
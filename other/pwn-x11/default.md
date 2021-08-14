
# PWN-X11

### Mini guide

#### Requirements
* PWN-Term 2.5.5 or 2.5.5-Legacy
* PWN-X11 1.0.0 or greater

#### Using with xfce4
* Open pwn-x11 and background it
* Now open pwn-term and run this

```
$ Apt install xfce4 xorg-server
```

* Now open two fresh tabs and run these cmd's in separate tabs

```
$ Xwayland :1

$ env DISPLAY=:1 startxfce4
```

*

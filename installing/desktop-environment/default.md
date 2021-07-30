---
title: 'Desktop environemnt'
---

### Tigervnc and viewer setup
* Connecting and killing vncserver guides are at the bottom!!!
#### Video guides
* [XFCE4](https://www.youtube.com/watch?v=txwhuV-iLsk)
#### Installing vnc server
```
apt update && apt install tigervnc
```
#### Setting up vnc server
##### XFCE4
###### Installing packages
```
apt update && apt install xfce4
```
###### Starting and stopping vnc to get xstartup files
```
vncserver && vncserver -kill :1
```
* now execute ``` home ``` to get to home dir
* Also ``` cd ./vnc``` and ``` nano xstartup``` there
* Now go to the bottom and comment out lines starting with
* aterm and twm and add this to there
```
xfce4-session &
```
* ```ctrl x and save``` and execute this
```
vncserver
```
* and youre done
##### I3
###### Installing packages
```
apt update && apt install i3
```
###### Starting and stopping vnc to get xstartup files
```
vncserver && vncserver -kill :1
```
* now execute ``` home ``` to get to home dir
* Also ``` cd ./vnc``` and ``` nano xstartup``` there
* Now go to the bottom and comment out lines starting with
* aterm and twm and add this to there
```
i3 &
```
* ```ctrl x and save``` and execute this
```
vncserver
```
* and youre done
##### Starting server
* Starting vnc
```
vncserver -localhost
```
* And give it password atleast 6+ long

##### Connecting
* Install vnc viewer by realvnc limited and add new connection
* For address add ```127.0.0.1:5901```
* And for name add ```root```
##### Killing and starting vnc server
* represents desktop server like :1
```
vncserver -kill :1
```
* Starting vncserver
```
vncserver
```

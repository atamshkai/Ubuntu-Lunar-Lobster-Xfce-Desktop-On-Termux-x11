# Ubuntu-Lunar-Lobster-Xfce-Desktop-On-Termux-x11

This is Ubuntu Lunar Lobster Xfce Desktop.It can change 3 styles.The styles are Windows 11 Style,MacOS Style & Neon Style.Some packages like VS Code,etc are pre-installed.Before you install this distro on android 12 and 13,disable phantom process killer. 

[Here](https://github.com/atamshkai/Phantom-Process-Killer/tree/main) 

## Preview

![](https://raw.githubusercontent.com/atamshkai/Ubuntu-Lunar-Lobster-Xfce-Desktop-On-Termux-x11/main/windows.png)

![](https://raw.githubusercontent.com/atamshkai/Ubuntu-Lunar-Lobster-Xfce-Desktop-On-Termux-x11/main/mac.png)

![](https://raw.githubusercontent.com/atamshkai/Ubuntu-Lunar-Lobster-Xfce-Desktop-On-Termux-x11/main/neon.png)

# To Do 

#### First,Download Lunar Xfce Distro From Here. (1GB)
[Download](https://archive.org/download/atam-lunar-xfce/lunar-xfce.tar.xz)

## Installation

Download lunar-xfce.tar.xz to Device's Download folder first. 

### Install Needed Packages 

```
pkg up -y && pkg i -y x11-repo && pkg i -y proot-distro pulseaudio termux-x11-nightly
```

### Give Storage Permission

```
termux-setup-storage
```

### Restore lunar-xfce.tar.xz

```
proot-distro restore /sdcard/download/lunar-xfce.tar.xz
```

### Add lunar-xfce command to termux's bin

```
echo "proot-distro login lunar-xfce --shared-tmp --bind /dev/null:/proc/sys/kernal/cap_last_cap" >>~/../usr/bin/lunar-xfce
```

### Give permission command

```
chmod +x ~/../usr/bin/lunar-xfce
```

### Install Zsh And Login Again If You Use My Distro For First Time Or Skip These Steps Before We Start Termux-x11.

```
pkg up -y && pkg i -y zsh wget

wget https://github.com/atamshkai/Termux-Zsh/raw/main/zsh.tar.xz

tar -xvJf zsh.tar.xz && mv zsh/.* ~/
rm -rf zsh

chsh -s zsh

echo "killall pulseaudio &>/dev/null" >>~/.zshrc 

echo "pulseaudio --start --exit-idle-time=-1; pacmd load-module module-native-protocol-tcp auth-ip-acl=127.0.0.1 auth-anonymous=1" >>~/.zshrc 

exit
```

### Download Latest Version Of Termux-x11 And Use It.

[Download](https://archive.org/download/atamshkai-termux-x11/app-universal-debug.apk)


### Start Termux-x11

```
termux-x11 :0 &
```

### Start Lunar-Xfce

```
lunar-xfce
```

### Start Lunar-Xfce-Desktop

```
xfce &>/dev/null
```

### Change Style Commands (Don't Repeat)

### Then Restart Distro

```
win2mac
```
```
win2neon
```
```
mac2win
```
```
mac2neon
```
```
neon2win
```
```
neon2mac
```

## Termux 
[Download](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_universal.apk)

## Termux-x11 Custom Resolution
1920:1080

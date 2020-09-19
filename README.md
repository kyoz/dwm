# Kyoz's fork of the suckless dynamic window manager (dwm)
> [dwm](https://dwm.suckless.org/) is a simple, light weight, powerful dynamic window manager for X

## Information
Base on [dwm-6.2](https://dl.suckless.org/dwm/dwm-6.2.tar.gz) version.

Patchs:
  - [actualfullscreen](https://dwm.suckless.org/patches/actualfullscreen/)
  - [alpha](https://dwm.suckless.org/patches/alpha/)
  - [attachasideandbelow](https://dwm.suckless.org/patches/attachasideandbelow/)
  - [autoresize](https://dwm.suckless.org/patches/autoresize/)
  - [fullgaps](https://dwm.suckless.org/patches/fullgaps/)
  - [hide_vacant_tags](https://dwm.suckless.org/patches/hide_vacant_tags/)

## Requirements
In order to build dwm you need the Xlib header files.


## Installation

Edit config.mk to match your local setup (dwm is installed into the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if necessary as root):

```
make clean install
```

## Running dwm

Add the following line to your .xinitrc to start dwm using startx:

```
exec dwm
```

In order to connect dwm to a specific display, make sure that the DISPLAY environment variable is set correctly, e.g.:

```
DISPLAY=foo.bar:1 exec dwm
```

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something like this in your .xinitrc:

```
while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
do
  sleep 1
done &
exec dwm
```

## Configuration

The configuration of dwm is done by creating a custom config.h and (re)compiling the source code.

# Introduction #

TV-MAXE should work on any Linux distribution if the following dependencies are satisfied :
  * Python 2 with GTK bindings
  * Official sopcast client for Linux systems
  * VLC or MPlayer (in case you want to use an external player)

However it is recommended to use your distributions package manager for easy installation.

# Installation instructions #

## Ubuntu ##

You can install TV-MAXE on Ubuntu from versions 10.04 up to 14.04 using following commands:

  * sudo add-apt-repository ppa:venerix/pkg
  * sudo apt-get update
  * sudo apt-get install tv-maxe

NOTE : latest versions are available only for LTS versions of Ubuntu

## Arch Linux ##

A PKGBUILD for latest version is found here https://aur.archlinux.org/packages.php?ID=51327

## Mandriva 2011.0 ##

Mandriva 2011.0 .rpm packages are provided by RMRB (ROSA/Mandriva Romanian Backports) Project. Use the following commands to install TV-MAXE :

### 32 Bit ###
  * urpmi.addmedia --update 'MRBi686\_rpms' 'http://mrb.mandrivausers.ro/MRB/2011.0/i686/MRB-rpms' with media\_info/hdlist.cz
  * urpmi tv-maxe

### 64 Bit ###
  * urpmi.addmedia --update 'MRBx86\_64\_rpms' 'http://mrb.mandrivausers.ro/MRB/2011.0/x86_64/MRB-rpms' with media\_info/hdlist.cz
  * urpmi tv-maxe

## ROSA 2012 LTS ##

ROSA 2012 LTS .rpm packages are provided by RMRB (ROSA/Mandriva Romanian Backports) Project. Use the following commands to install TV-MAXE :

### 32 Bit ###
  * urpmi.addmedia --update 'MRBi686\_rpms' 'http://mrb.mandrivausers.ro/MRB/2012LTS/i686/MRB-rpms' with media\_info/hdlist.cz
  * urpmi tv-maxe

### 64 Bit ###
  * urpmi.addmedia --update 'MRBx86\_64\_rpms' 'http://mrb.mandrivausers.ro/MRB/2012LTS/x86_64/MRB-rpms' with media\_info/hdlist.cz
  * urpmi tv-maxe

## Gentoo / Sabayon ##

Use following commands to install TV-MAXE from V3n3RiX's Gentoo overlay :

  * sudo layman -f -a atropus -o https://raw.github.com/V3n3RiX/atropus/master/overlay.xml
  * sudo emerge -av tv-maxe
# FireTray

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [FireTray](#firetray)
	- [Overview](#overview)
		- [Features](#features)
	- [Build/install](#buildinstall)
	- [New releases have been tested with](#new-releases-have-been-tested-with)
		- [Working](#working)
		- [Not working](#not-working)
		- [Not tested](#not-tested)
	- [Donations](#donations)

<!-- /TOC -->

## Overview

> This is a fork of FireTray ([Github][ft-foudfou]/[Web][ft-web]) by [foudfou][gh-foudfou]

FireTray is a Mozilla addon that targets Firefox, Thunderbird and Seamonkey. It provides a system tray icon with much window handling functionality. For mail applications, the icon can show the number of unread or new messages.  
FireTray is very customizable and works on Linux and Windows.

> The original FireTray has been patched to display the number of unread messages in KDE/Windows system tray.
It is a workaround for issues:
* [foudfou/FireTray #143][ft-issue143]
* [foudfou/FireTray #210][ft-issue210]

### Features

* for all applications:  
  * show/hide a single or all windows
  * restore windows to their previous state, position, size
  * restore each window to its original virtual desktop/workspace
  * activate restored windows
  * hide to tray on close
  * hide to tray on minimize
  * start minimized to tray
  * show icon only when hidden to tray
  * mouse scroll on tray icon shows/hides
  * GTK-themable icons
  * StatusNotifierItem support (can be disabled by `with_appindicator` hidden pref)
  * customizable tray icons
  * popup menu (show/hide individual windows, open new windows, quit)
  * command-line `-firetrayShowHide` option (useful for window manager's keyboard shortcuts)
  * command-line `-firetrayPresent` option (activates windows)
  * middle click on the tray icon activates last registered window  


* for mail applications:
  * display unread message count in tray icon
  * display biff in tray icon for new messages
  * include/exclude mail accounts to/from messages count
  * include/exclude folders types to/from messages count
  * count in sub-folders recursively
  * handle [Exquilla](https://addons.mozilla.org/fr/thunderbird/addon/exquilla-exchange-web-services/) accounts
  * restrict message count to favorite folders
  * trigger external program on message count change
  * show icon only when new mail (mutually exclusive with *show icon only when hidden to tray*)  


* for applications embedding chat (currently only Thunderbird):
  * display additional system tray status icon

--------

## Build/install  
To build XPI file just do:
```
	$ cd src
	$ make build
```

To install icons on Kubuntu:
```
	$ cp ./src/chrome/skin/icons/unread/*.svg /usr/share/icons/breeze/actions/16/
	$ cp ./src/chrome/skin/icons/unread/*.svg /usr/share/icons/breeze/actions/22/
	$ cp ./src/chrome/skin/icons/unread/*.svg /usr/share/icons/breeze/actions/24/
```
--------

## New releases have been tested with  
### Working

| Thunderbird | Architecture |              OS             |
| :---------: | :----------: | :-------------------------: |
|    52.9.1   |    32-Bit    |        Windows 10 x64       |
|             |    64-Bit    |        Windows 10 x64       |
|             |       ?      |      openSuSE Leap 15.0     |
|    60.2.1   |       ?      |      Linux Mint 19 Tara     |
|             |    64-Bit    |        Devuan ASCII         |
|             |    64-Bit    | Ubuntu MATE LTS 18.04 AMD64 |
|             |    64-Bit    |          Fedora 27          |
|    60.3.0   |       ?      |      openSuSE Leap 15.0     |
|             |    64-Bit    |        Debian 9.5 x64       |
|    60.4.0   |    64-Bit    |      Arch Linux x86_64      |
|       ?     |       ?      |    Linux Mint 18.3 Sylvia   |

Thank you for testing !!!  

### Not working  
(K)ubuntu 16.04, Thunderbird (very small icon with GTK)  

### Not tested  
SeaMonkey  
ChatZilla  
Zotero  

other desktops...  

--------

## Donations
To support this project, you can make a donation to its current maintainer:  

[![paypal](https://github.com/Ximi1970/Donate/blob/master/paypal_btn_donateCC_LG_2.gif)][donations-paypal] [![bitcoin-qrcode-black](https://github.com/Ximi1970/Donate/blob/master/bitcoin-donate-qrcode-black.png)][donations-bitcoin]




[gh-foudfou]: https://github.com/foudfou "foudfou (Github)"
[ft-foudfou]: https://github.com/foudfou/FireTray "FireTray (Github)"
[ft-web]: https://foudfou.github.io/FireTray/ "FireTray (Website)"  

[ft-issue143]: https://github.com/foudfou/FireTray/issues/143 "foudfou - FireTray Issue 143 (Github)"  
[ft-issue210]: https://github.com/foudfou/FireTray/issues/210 "foudfou - FireTray Issue 210 (Github)"  

[donations-paypal]: https://paypal.me/Ximi1970 "Ximi1970 Paypal donation"  
[donations-bitcoin]: https://raw.githubusercontent.com/Ximi1970/Donate/master/bitcoin-address.txt "Ximi1970 Bitcoin donation"

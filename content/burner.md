---
date: 2021-11-21T07:29:57+07:00
type: section
title: "Burner Tools"
slug: "tools/burner"
---

Piranti untuk memburn usb / flashdisk / sdcard / emmc.

> No receh-receh link, cukup doakan saja berkah dan rejeki lancar.

## USB Imager

Ringan dan praktis.

![](https://gitlab.com/bztsrc/usbimager/raw/master/usbimager.png)

### Download:

| Platform     | Frontend     | Description                  |
|--------------|--------------|------------------------------|
| Windows      | [GDI](https://gitlab.com/bztsrc/usbimager/raw/binaries/usbimager_1.0.8-i686-win-gdi.zip)<br>[GDI wo](https://gitlab.com/bztsrc/usbimager/raw/binaries/usbimager_1.0.8_wo-i686-win-gdi.zip) | native interface<br>simplified, write-only interface |
| MacOSX       | [Cocoa](https://gitlab.com/bztsrc/usbimager/raw/binaries/usbimager_1.0.8-intel-macosx-cocoa.zip)<br>[Cocoa wo](https://gitlab.com/bztsrc/usbimager/raw/binaries/usbimager_1.0.8_wo-intel-macosx-cocoa.zip) | native interface<br>simplified, write-only interface |
| Ubuntu LTS   | [GTK+](https://gitlab.com/bztsrc/usbimager/raw/binaries/usbimager_1.0.8-amd64.deb)<br>[GTK+ wo](https://gitlab.com/bztsrc/usbimager/raw/binaries/usbimager_1.0.8_wo-amd64.deb) | same as the Linux PC GTK version with udisks2 support, but in .deb format<br>simplified, write-only interface |
| RaspiOS      | [GTK+](https://gitlab.com/bztsrc/usbimager/raw/binaries/usbimager_1.0.8-armhf.deb)<br>[GTK+ wo](https://gitlab.com/bztsrc/usbimager/raw/binaries/usbimager_1.0.8_wo-armhf.deb) | same as the Raspberry Pi GTK version with udisks2 support, but in .deb format<br>simplified, write-only interface |
| Arch/Manjaro | [GTK+](https://aur.archlinux.org/packages/usbimager/)<br>[GTK+](https://aur.archlinux.org/packages/usbimager-bin/)<br>[X11](https://aur.archlinux.org/packages/usbimager-x11/) | same as the Linux PC GTK version with udisks2 support, but in an AUR package<br>generated from the binaries<br>minimal X11 version |
| Linux PC     | [X11](https://gitlab.com/bztsrc/usbimager/raw/binaries/usbimager_1.0.8-x86_64-linux-x11.zip)<br>[GTK+](https://gitlab.com/bztsrc/usbimager/raw/binaries/usbimager_1.0.8-x86_64-linux-gtk.zip) | recommended<br>compatibility (requires udisks2) |
| Raspberry Pi | [X11](https://gitlab.com/bztsrc/usbimager/raw/binaries/usbimager_1.0.8-armv7l-linux-x11.zip)<br>[X11](https://gitlab.com/bztsrc/usbimager/raw/binaries/usbimager_1.0.8-aarch64-linux-x11.zip) | native interface, AArch32 (armv7l)<br>native interface, AArch64 (arm64) |



Atau bisa langsung ke situsnya aja

🔖link https://gitlab.com/bztsrc/usbimager/

## balenaEtcher

ini lebih terkenal dikalangan opreker Indonesia. Ada iklannya 🤪

![](https://www.balena.io/static/steps-8006dca57323756b1b84fb9408742409.gif)

🔖link download https://github.com/balena-io/etcher/releases/latest


## Perbandingan


| Description                    | balenaEtcher  | WIN32 Disk Imager | USBImager |
|--------------------------------|---------------|-------------------|-----------|
| Multiplatform                  | ✔             | ✗                 | ✔         |
| Minimum Windows                | Win 7         | Win XP            | Win XP    |
| Minimum MacOSX (1)             | ?             | ✗                 | 10.10     |
| Available on Raspbian          | ✗             | ✗                 | ✔         |
| Program size (2)               | 130 Mb        | ✗                 | 300 Kb    |
| Dependencies                   | lots, ~300 Mb | Qt, ~8 Mb         | ✗ none    |
| Spyware-free and ad-free       | ✗             | ✔                 | ✔         |
| Native interface               | ✗             | ✗                 | ✔         |
| Guarantee on data writes (3)   | ✗             | ✗                 | ✔         |
| Verify data written            | ✔             | ✗                 | ✔         |
| Compressed images              | ✔             | ✗                 | ✔         |
| Raw write time (4)             | 23:16         | 23:28             | 24:05     |
| Compressed write time (4)      | 01:12:51      | ✗                 | 30:47     |

> Catatan poin 1 sd 4 bisa dilihat situsnya USB Imager.

---

Jika ada link yang tidak bekerja, ada yang baru dan ingin ditambahkan, beritahukan bisa via komentar.
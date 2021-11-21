---
date: 2021-11-21T12:09:57+07:00
type: section
slug: "tools/armbian"
title: "Armbian"
---
Link download files image armbian.

> No receh-receh link, cukup doakan saja berkah dan rejeki lancar.

Kalau bingung karena masih awal-awal, coba saja versi jadinya punya saya hehe..

## Pengertian

- `bionic` adalah versi **Ubuntu** `18.04` **LTS** dengan nama kode _Bionic Beaver_
- `focal` adalah versi **Ubuntu** `20.04` **LTS** yang memiliki nama kode _Focal Fossa_
- `hirsute` adalah versi **Ubuntu** `21.04` dengan nama kode *Hirsute Hippo*
- `buster` adalah versi **Debian** `10`

sumber:
- [ubuntu history](https://en.wikipedia.org/wiki/Ubuntu_version_history)
- [debian  history](https://en.wikipedia.org/wiki/Debian_version_history)

## Versi Jadi

Karena aku lelah, burn - edit - ngetes berulang kali. Maka terjadilah pengeditan image ini.

Ini adalah versi yang sudah jadi, tinggal burn jalan - **tanpa edit-edit** lagi.

Aku pengguna Ubuntu, maka images berikut ini sudah saya sesuaikan.

`dtb` sudah di set ke **meson-gxl-s905x-p212.dtb** yang secara umum banyak dipergunakan juga untuk STB Huawei HG680p ataupun ZTE B860H.


### Server

#### Armbian_20.10_Arm-64_focal_server_5.9.0.img.xz

- [Download](https://github.com/banghasan/stb.pages.dev/releases/download/0.2/Armbian_20.10_Arm-64_focal_server_5.9.0.img.xz)
- md5 `400f505743c254e0d4d5f2d804215e2e `
- sha256 `1124337357e8f56f68eed780f74ccad7e39fd20a25460e447fa2bd5f50ac4403`

### Desktop

#### Armbian_20.10_Arm-64_focal_desktop_5.9.0.img.xz

- [Download](https://github.com/banghasan/stb.pages.dev/releases/download/0.2/Armbian_20.10_Arm-64_focal_desktop_5.9.0.img.xz)
- md5 `91550a708d6cba97321b656b6e23f6cd`
- sha256 `02a4a7514306417a91602f6a5ab0e9ee6af1d28839c29587ebb8b6b8adcf04c6`


## Rureka

Koleksinya [rureka.com](https://rureka.com), sebelum di pasang ke STB **harus diedit** dulu file yang terkait dengan dtb.

### Desktop

- [Armbian_20.10_Arm-64_focal_current_5.9.0_desktop.img.xz](https://androidfilehost.com/?fid=10763459528675575689) 👈🏼
- [Armbian_20.10_Arm-64_bullseye_current_5.9.0_desktop.img.xz](https://androidfilehost.com/?fid=10763459528675575686)

### Server

- [Armbian_20.10_Arm-64_focal_current_5.9.0.img.xz](https://androidfilehost.com/?fid=10763459528675575688) 👈🏼
- [Armbian_20.10_Arm-64_buster_current_5.9.0.img.xz](https://androidfilehost.com/?fid=10763459528675575687)
- [Armbian_20.10_Arm-64_bullseye_current_5.9.0.img.xz](https://androidfilehost.com/?fid=10763459528675575685)
- [Armbian_20.10_Arm-64_bionic_current_5.9.0.img.xz](https://androidfilehost.com/?fid=10763459528675575683)

Koleksi _rureka_ tidak saya backup lagi, karena ditaruh di [androidfilehost](https://androidfilehost.com) yang insyaAllah awet, sepanjang tidak dihapus ownernya.

Yang ditandai itu yang aku pakai dan disesuaikan.

## Ophub

Yang ini ternyata juga gak perlu edit dtb, sudah bisa jalan.

Namun hanya tersedia versi `buster` server. Namun, kalau kamu tertarik bisa build sendiri karena disini diajarkan caranya.

🔖 link [github.com/ophub/amlogic-s9xxx-armbian](https://github.com/ophub/amlogic-s9xxx-armbian/)

- Default username/password: `root/1234`
- Install to EMMC command: `armbian-install`
- Update command: `armbian-update`

### Download:

Terdapat banyak pilihin chipset wifi nya. Saya cantumkan disini yang generic. Lainnya menuju ke repo nya saja yak.

- [Armbian_21.11.0_Aml_s905x_buster_5.4.160_2021.11.21.1210.img.gz](https://github.com/ophub/amlogic-s9xxx-armbian/releases/download/Armbian_Aml_buster_2021.11.21.1216/Armbian_21.11.0_Aml_s905x_buster_5.4.160_2021.11.21.1210.img.gz)  👈🏼
- ... cek selengkapnya pada [halaman releasenya](https://github.com/ophub/amlogic-s9xxx-armbian/releases)

---

Jika ada link yang tidak bekerja, ada yang baru dan ingin ditambahkan, beritahukan bisa via komentar.
---
title: "Pertamax"
date: 2021-11-14T22:28:57+07:00
draft: false
tags: [
    "news",
    "armbian"
]
---

Bismillah.. 

## Pertamax

Website ini dibuild dari mini server armbian.

Dan saat ini **live** dari server tersebut menggunakan koneksi internet seadanya.. namun, hasilnya tak sekadar alakadarnya lhoh! 

### Ref

- Cekidot pada blog utama: [banghasan.com](https://banghasan.com/post/2021/11/11/oprek-stb-router/)

## mini server

Awalnya mau pakai mini PC dengan intel nuc, 3-7 juta, eits mahal. Juga untuk konsumsi daya listriknya cukup besar, jika hidup terus di rumah. Jadilah berfikir 100x.

Kemudian mempertimbangkan pakai raspberry pi 4 dengan RAM 8 GB, eits.. mayan _mehong_ juga hampir 2juta -- bikin berfikir 60x.

Alternatif lain, mo pakai arduino uno -- tapi kok males ngerakit-rakit. Berfikir lagi 75x.

Eh baru ingat, di rumah ada STB bisa dipakai coba-coba. Yap, lalu diinstallah ubuntu. Dan sangat menyenangkan!

Gak hanya armbian, aku install openwrt juga.

![](/img/stb.webp)

Storage sementara masih di microsd / flashdisk, dengan keuntungan tentu saja jadi bisa mudah gonta ganti distro dan setingan, fleksibel colok cabut.

Kalau sudah fix ke depan mau dipindah ke internal (emmc). Karena pakai eksternal storage speednya berbeda jauh dengan penggunaan emmc. Pada test speedku, pakai microsd/flashdisk hanya 7-12 MBps. Sementara jika pakai internal (emmc), bisa sampai diatas 100 MBps.

Estimasi harga STB ini di marketplace antara 200-300rb, bisa juga diatas 300rb tapi gak sampai diatas 500rb.
Itu artinya 6-8x lebih murah dari sebelumnya woyy! Mantul, gitu loch.

OK, aku rasa cukup efektif dan efisien, juga bisa meningkatkan produktifitas.

### Service

Saat ini diinstall:

- nginx untuk webserver, dan satu diantara hasilnya ya situs ini
- dns server, buat buka blokir kominfo dan cegah iklan
- file server, buat naruh-naruh file
- nodejs, dll.. masih dan sedang proses

![](https://banghasan.com/img/in-post/2021-11/11/armbian.webp)

## Test

Ini test-test corat coret

Inline math: $$ \varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887… $$

Block math:

$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } }
$$


## Yap

Bisa!

```js
var hasil = proses;

function coba() {
  while (hasil !== sukses) {
    coba(terus);
  }
}
```

## Semangat!

Salam hangat selalu,

<img src="https://banghasan.com/img/icons/banghasan.svg" alt="banghasan.com" style="float: right;
width: 300px;" />

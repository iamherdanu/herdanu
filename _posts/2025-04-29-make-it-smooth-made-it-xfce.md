---
title: Make it smooth, made it XFCE
description: Pengalaman migrasi GNOME ke XFCE
author: Danu
date: 2025-04-29
categories: [Blogging, Demo]
tags: [FEDORA, XFCE, SHORTCUT]    
---

Tampilan XFCE sangat tradisional dan unik bagi user yang terbiasa menggunakan GNOME atau DE yang lebih modern, tetapi menimbang RAM yang digunakan XFCE sangat ringan (300-500), migrasi XFCE pilihan yang menarik di coba. cheers!

Komponen Utama: 

1. Xfwm4: window manager
2. Xfce panel : panel yang dapat di kustomisasi
3. Thunar: file manager
4. XFdesktop: Pengelola desktop
5. Xfce settings manager: pusat pengaturan


### Instalasi

```terminal
sudo dnf install @xfce-desktop-environment
```

restart lalu pilih xfce di pengaturan (di GNOME saya terletak di pojok kanan bawah)

![my xfce's default interface](/_posts/img-articles/tampilan-xfce.png)
_looks cool_

### Shortcut penting:

1. Alt + f1 = buka whisker menu
2. Alt + f2 = dialog run
3. esc = close (ex: close dari dialog run dll)
4. ctrl + Alt + del = menu logout
5. PrtScr = screenshoot
6. Alt + drag = drag menu 
7. Alt + f9 = minimaze 
8. ctrl + alt + d = minimaze semua jendela
9. super + e = buka file manager
10. ctrl + alt + t = buka terminal
11. ctrl + shift + t = tab baru di terminal

### Theme and icon

Theme

```terminal
sudo dnf install arc-theme papirus-icon-theme
```

Icon

```terminal
install arc-theme dan papirus-icon
```
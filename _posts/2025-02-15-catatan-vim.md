---
layout: post
title: Catatan Vim
date: 2025-02-15 15:44 +0700
---
Backup catatan command vim, walaupun masih mumet:

insert mode :
i
normal mode :
esc

### File

| Command             | Run         |
| :------------------ | :---------- |
| Simpan              | `:w`        |
| Keluar              | `:q`        |
| Simpan dan keluar   | `:wq`       |
| Keluar tanpa simpan | `:q!`       |
| Menutup explorer    | `[spasi] e` |

### Editor

| Command                               | Run               |
| :------------------------------------ | :---------------- |
| Ke bawah                              | `j`               |
| Ke atas                               | `k`               |
| Lompat ke bawah                       | `[line number] j` |
| Lompat ke atas                        | `[line number] k` |
| Menutup explorer                      | `[spasi] e`       |
| Ke kanan                              | `l`               |
| Ke kiri                               | `h`               |
| Lompat satu baris kata                | `w`               |
| Balik satu baris kata                 | `b`               |
| Delete satu baris                     | `dd`              |
| delete                                | `d`               |
| undo                                  | `u`               |
| Menghapus baris ke bawah [ex 11 line] | `d 11 j`          |
| Copy                                  | `yy`              |
| Paste ke bawah                        | `p`               |
| balik ke normal mode                  | `esc`             |
| delete                                | `d`               |
| undo                                  | `u`               |
| Menghapus baris ke bawah [ex 11 line] | `d 11 j`          |
| Copy                                  | `yy`              |
| Paste ke bawah                        | `p`               |



nge blok/visual mode : v
misal ingin menghapus, v arahin lalu d
command line, save : w
hapus ke atas : d 3 k

Select:
ctrl v : select columns
gv : reselect block

cut and paste:
v [uppercase] : select character
move the cursor
d : cut
p : paste
P : paste before next character



Menghapus semua folder dan file konfigurasi:
#Hapus folder nvim
rm -rf ~/.config/nvim

#Hapus cache dan data
rm -rf ~/.local/share/nvim
rm -rf ~/.local/state/nvim
rm -rf ~/.cache/nvim

#hapus backup
rm -rf ~/.config/nvim.backup

Verifikasi semua sudah terhapus
ls -la ~/.config/nvim
ls ls ~/.local/share/nvim
ls ls ~/.local/state/nvim
ls ls ~/.cache/nvim

Balik lagi ke menu install
:Lazy

install konfigurasi baru:
:Lazy load nvim-tree.lua

direktori baru
mkdir/lua/danu/plugins

file baru
touch lua/danu/plugins/colorscheme.lua

pressing terminal:
:terminal

my keymap:
new folder: Shift + N

new file
:! touch new-file.txt
new folder
:! mkdir new-directory

/ = Ctrl + F di vscode

Scrolling the screen:
down : ctrl e, ctrl d
up : ctrl y, ctrl u

:help scrollig

pindah tab-kiri kanan:
ctrl ww
ctrl wl

close tab:
ctrl wq

new folder
:Sexplore
d new folder
% file

a = append
o & O = also switch to insert mode

gi = go to the last things we do on insert mode

:e foo/baz/fizz.txt
or
:e f<tab>b<tab>
and ctrl y to confirm means yes

Z mode,
z : shows the list random command

counting:
the hjkl can combine with number
ex: 15k will up 15line, 7j will move down 7line, and the l, h too.

block file

copy/paste

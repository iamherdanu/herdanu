---
title: Memulai Project di Github
author: Danu
date: 2025-02-10
categories: [Blogging, Tutorial]
tags: [GITHUB, SSH KEY, PERSONAL TOKEN]
---

Configurasi dan login
<https://git-scm.com/docs/git-config>


Di local komputer - inisiasi git, upload perubahan, commit dan push

```Terminal
git init
git add . [readme.txt]
git commit -m "initial commit"
git push -u origin
```

```Terminal
git status
```

### Remote Repositori, SSH, Token Github
Cek status remote, menghubungkan komputer local dengan SSH, HTTPS dan membuat token sementara.

```Terminal
git remote -v
```

### SSH Key Github


### Github Token Generate
Github token bisa menjadi solusi sementara jika mengalami kendala pada SSH key.
1. Masuk akun github
2. `Settings`
3. `Developer settings` (sebelah kiri paling bawah)
4. `Personal access tokens` -> `Tokens (classic)`
5. `Note` (nama token, ex: token login)
6. `Expiration` (durasi token berlaku)
7. `Select scopes` (ceklis repo, atau sesuai kebutuhan)
8. `Generate token`
9. copy dan simpan kode token yang muncul

How to use?
1. masukan username github
2. kode token

Clone Repository:

HTTPS
1. Code
2. Copy URL

```Terminal
git clone https://github.com/username/repo-github
```
SSH:
```Terminal
git@github.com:username/repo-github.git
```
### Lain-lain

1. `git init` inisiasi repository
2. `git checkout` pindah branch 
3. `rm -rf .git` hapus inisiasi git
4. `git checkout nama-branch`: pindah branch
5. `git checkout -b new-branch` pindah branch sekaligus buat branch baru
6. `git diff new-branch` membandingkan perubahan yang dibuat
7. `git merge new-branch` menggabungkan branch baru ke branch utama
8. `git remote -v` cek remote yang terhubung
9. `git branch -d feature-new-branch` menghapus branch

Bagaimana jika repo sudah di init namun belum di push?
> repo dengan nama tersebut tetap aktif, dan tidak bisa inisiasi
dengan nama yang sama.
{: .prompt-info }

Bagaimana jika tidak sengaja melakukan git init di folder induk, dan bukan di folder yang ingin saya upload? 
> hapus git di folder tersebut, `rm -rf nama repo.git` kemudian init di folder yang benar.
{: .prompt-info }

### Git Branch

>"Use a branch to isolate development work without affecting other branches in the repository. Each repository has one default branch, and can have multiple other branches. You can merge a branch into another branch using a pull request". 
<https:/docs.github.com/about-branches>.

Mengganti branch dan membuat branch baru
```terminal
git checkout -b feature-branch
```
Branch baru berhasil dibuat. Cek branch; 
```terminal
git branch
```
dan kembali ke branch utama
```terminal
git checkout master
```
mengaplikasikan feature yg dibuat ke branch utama
1. masuk ke branch utama `git checkout master`
2. bandingkan perubahan yang dibuat `git diff feature-branch`
3. mengaplikasikan perubahan dengan _merge/menggabungkan_ ke branch utama `git merge feature-branch`

> pastikan untuk push terlebih dahulu perubahna yang dibuat di branch baru:
`git push --index.html origin feature-branch`
{: .prompt-info }


lakukan pull request, untuk mengajukan revisi perubahan. pada branch tersebut.
```terminal
git pull
```

---
title: Memulai Project di Github
author: Danu
date: 2025-02-10
categories: [Blogging, Tutorial]
tags: [GITHUB, SSH KEY, PERSONAL TOKEN]
---

Di local komputer - inisiasi Git, upload perubahan, commit dan push

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

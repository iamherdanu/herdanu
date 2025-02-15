---
title: Fedora workstation shortcut
description: Fedora Workstation keyboard shortcut
author: Danu
date: 2025-02-07
categories: [Blogging, Demo]
tags: [FEDORA, TERMINAL, SHORTCUT]    
---

My experience and some research to find the perfect ways for helping me a lot

List only hidden files
```terminal
ls -d .?*
```
show hidden files
```terminal
ls -a
//or
ls -la 
```
Open hidden file directory
```terminal
~/.config/
```
Display tree structure
```terminal
tree -a
```
Delete file
```terminal
rm filename
//or
rm -r Hack-v3.003-ttf.zip
```
Create file
```terminal
touch createfile.txt
```
Copy file
```terminal
cp file source destination
//Ex: 
cp Hack-v3.003-ttf.zip ~/.local/share/fonts)
```
Copy to clipboard
```terminal
cat ~/.id_ed19.pub | xclip selection clipboard (To manually copy: cat ~/.id_ed19.pub)
```
Cut file
```terminal
mv Hack-Bold ~/.local/share/fonts/hack-font
```
Show current directory
```terminal
pwd
```
Run image file
```terminal
chmod +x nama-berkas-instalasi.run 
//or 
./nama-berkas-instalasi.run
```
Open file on terminal
```terminal
xdg-open fedora-command.txt
```
Rename file on terminal
```terminal
mv perintah-fedora.txt fedora-command.txt
```
Edit path
```terminal
nano ~/.bashrc 
//or
nano ~/.bashrc.d
```
Save path
```terminal
source ~/.bashrc
//or 
source ~/.bashrc.d
```
### Browser and Desktop

| Command        | Run        |
| :------------- | :--------- |
| New tab        | Ctrl + T   |
| Switch Tab     | Ctrl + Tab |
| Go to last tab | Ctrl + 9   |
| Close tab      | Ctrl + w   |
| Quick search   | /          |

Application Dialog

```fedora
Alt + f2 [type: firefox]
```
Open all menus

```fedora
Windows key + a
```

Show all apps
```terminal
Super + A
```

Show notif list
```fedora
Super + V
```

Set timer close browser
```fedora
sleep 180 && pkill -f "firefox"
```    
    
    

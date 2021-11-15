---
title: "Github Action"
date: 2021-11-16T04:40:00+07:00
draft: false
tags: [
    "github",
    "bash"
]
---

Biar arsip terjaga, blog ini di simpan di github dan diintegrasikan dengan github action.

## Flow

- Laptop ngedit blog
- Push ke github
- Github action:
    - login ssh
    - git pull
    - membuat public hugo
- selesai :-)


## ACTION

```yaml
name: remote ssh command
on: [push]
jobs:

  build:
    name: Build
    runs-on: ubuntu-latest
    steps:
    - name: executing remote ssh commands using password
      uses: appleboy/ssh-action@master
      with:
        host: ${{ secrets.HOST }}
        username: ${{ secrets.USERNAME }}
        password: ${{ secrets.PASSWORD }}
        port: ${{ secrets.PORT }}
        script: |
          cd ~/GITHUB/stb
          git pull
          hugo

```

Sumber: [appleboy/ssh-action](https://github.com/appleboy/ssh-action/)
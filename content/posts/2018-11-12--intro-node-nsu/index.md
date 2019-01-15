---
title: Intro to NodeJS, NSU, FALL 2018
category: "workshop"
cover: 1200px-Node.js_logo.svg.png
author: Shawon Ashraf
---

Before you come to the workshop, make sure you have these things checked. And, please come with your own laptop to ease things.

## Software / Tools to install
- [NodeJS](https://nodejs.org/en/). You can either choose the LTS version or the Current Version. Any will do.

__Linux Users please refer to the package manager for your distribution e.g. for Ubuntu search in apt packages__

- [Visual Studio Code](https://code.visualstudio.com/) or [Atom](https://atom.io/) for writing code. You can also use [Webstorm](https://www.jetbrains.com/webstorm/). Signing up for [Jetbrains Student Program](https://www.jetbrains.com/student/) gives you a year of commercial license to use Webstorm! You can sign up using your `@northsouth.edu` e-mail address. Get that if you can, will ease up your code writing experience.

- [MongoDB Community Server](https://www.mongodb.com/download-center/community) - this is optional. Instead of running Database locally you can register for a free database at [mLab](https://mlab.com/) or [MongoDB Atlus](https://www.mongodb.com/download-center?jmp=nav). If your laptop is low on RAM ( < 8GB), consider using an online database instead of running it on your laptop.

__Linux Users please refer to the package manager for your distribution e.g. for Ubuntu search in apt packages__

- [Robo 3T](https://robomongo.org/download) it was previously called RoboMongo. - Optional, required only if you're running mongodb locally.

- [Studio 3T Trial](https://studio3t.com/) A must whether you're using online or locally running database servers.

- [Postman](https://www.getpostman.com/) or [Insomnia](https://insomnia.rest/)

- [Git For Windows](https://git-scm.com/downloads) and [Gitkraken](https://www.gitkraken.com/git-client) - these are necessary for something we'll see during the workshop. And no you don't need to know how to use git beforehand.

__If you're a Linux Distro or macOS user you don't need to install git. It comes with your os. In some cases you may need to enable it from the command line__

If you're on macOS and don't have `Xcode` installed, you need to install the `command line tools` to get git enabled. Open `terminal` and type the following. It's a 120++ MB download.

```bash
xcode-select --install
```

On Linux distros, `git` should be enabled by default, if it isn't type in - 
```bash
git
```
You'll be shown the necessary steps to install `git`.

- [Heorku CLI](https://devcenter.heroku.com/articles/heroku-cli)

## Recommended Reading
Make sure you go through these before showing up. No problem if you don't understand all of it , feel free to ask questions.
- [JSON কি জিনিস?](https://medium.com/@sashraf94/json-%E0%A6%95%E0%A6%BF-%E0%A6%9C%E0%A6%BF%E0%A6%A8%E0%A6%BF%E0%A6%B8-eed4deba3b34)
- [জাভাস্ক্রিপ্ট ব্যাসিকসঃ With Zonayed](https://medium.com/zonayeds-diary/%E0%A6%9C%E0%A6%BE%E0%A6%AD%E0%A6%BE%E0%A6%B8%E0%A7%8D%E0%A6%95%E0%A7%8D%E0%A6%B0%E0%A6%BF%E0%A6%AA%E0%A7%8D%E0%A6%9F-%E0%A6%AC%E0%A7%8D%E0%A6%AF%E0%A6%BE%E0%A6%B8%E0%A6%BF%E0%A6%95%E0%A6%B8%E0%A6%83-with-zonayed-5d4650ed2ef8)
- [নিত্যদিনের জাভাস্ক্রিপ্টঃ প্রমিস (Promise)](https://medium.com/%E0%A6%AA%E0%A7%8D%E0%A6%B0%E0%A7%8B%E0%A6%97%E0%A7%8D%E0%A6%B0%E0%A6%BE%E0%A6%AE%E0%A6%BF%E0%A6%82-%E0%A6%AA%E0%A6%BE%E0%A6%A4%E0%A6%BE/%E0%A6%A8%E0%A6%BF%E0%A6%A4%E0%A7%8D%E0%A6%AF%E0%A6%A6%E0%A6%BF%E0%A6%A8%E0%A7%87%E0%A6%B0-%E0%A6%9C%E0%A6%BE%E0%A6%AD%E0%A6%BE%E0%A6%B8%E0%A7%8D%E0%A6%95%E0%A7%8D%E0%A6%B0%E0%A6%BF%E0%A6%AA%E0%A7%8D%E0%A6%9F%E0%A6%83-%E0%A6%AA%E0%A7%8D%E0%A6%B0%E0%A6%AE%E0%A6%BF%E0%A6%B8-promise-847b8b0090f6)
- [নিত্যদিনের জাভাস্ক্রিপ্টঃ অ্যাসিনক্রোনাস (Asynchronous)](https://medium.com/%E0%A6%AA%E0%A7%8D%E0%A6%B0%E0%A7%8B%E0%A6%97%E0%A7%8D%E0%A6%B0%E0%A6%BE%E0%A6%AE%E0%A6%BF%E0%A6%82-%E0%A6%AA%E0%A6%BE%E0%A6%A4%E0%A6%BE/%E0%A6%A8%E0%A6%BF%E0%A6%A4%E0%A7%8D%E0%A6%AF%E0%A6%A6%E0%A6%BF%E0%A6%A8%E0%A7%87%E0%A6%B0-%E0%A6%9C%E0%A6%BE%E0%A6%AD%E0%A6%BE%E0%A6%B8%E0%A7%8D%E0%A6%95%E0%A7%8D%E0%A6%B0%E0%A6%BF%E0%A6%AA%E0%A7%8D%E0%A6%9F%E0%A6%83-%E0%A6%85%E0%A7%8D%E0%A6%AF%E0%A6%BE%E0%A6%B8%E0%A6%BF%E0%A6%A8%E0%A6%95%E0%A7%8D%E0%A6%B0%E0%A7%8B%E0%A6%A8%E0%A6%BE%E0%A6%B8-asynchronous-3f11e15b883a)
- [Philip Roberts: What the heck is the event loop anyway? at JSConf EU](https://youtu.be/8aGhZQkoFbQ)
- [Getting up and running with MongoDB — Part 1 Introduction](https://medium.com/@sashraf94/getting-up-and-running-with-mongodb-part-1-introduction-4b34bebe3da2)

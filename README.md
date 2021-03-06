Gladys Project
=======================

[![npm version](https://badge.fury.io/js/gladys.svg)](https://www.npmjs.com/package/gladys)
[![Build Status](https://travis-ci.org/GladysProject/Gladys.svg?branch=v3)](https://travis-ci.org/GladysProject/Gladys) [![Code Climate](https://codeclimate.com/github/GladysProject/Gladys/badges/gpa.svg)](https://codeclimate.com/github/GladysProject/Gladys)
[![Join the chat at https://gitter.im/GladysProject/Gladys](https://badges.gitter.im/GladysProject/Gladys.svg)](https://gitter.im/GladysProject/Gladys?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

![Alt](http://gladysproject.com/assets/images/presentation/facebook_share_gladys.jpg)

The Project
-------------

Gladys is an home automation assistant to help you in your everyday life.

Yes, like a kind of **JARVIS**!

Gladys is connected to all your devices in your home, she is connected to your calendar, to a lots of API to help you. But let's pick an example :

- It's 8 AM. Gladys wakes you up automatically because she knows that you need to be at work at 9 AM, and that according to the traffic, you'll need 30min to go to work with your car. She knows that you like 30 min to get ready.
She wakes you up with a soft progressive warm light thanks to your Philips Hue, and puts a nice music in your room.
- It's 8.10 AM, Gladys detects thanks to a motion sensor that you are getting out of bed. She immediately starts the wake-up scenario : she tells the coffee machine to prepare the coffee, and opens the blinds.
- At 8.30 AM, you leave the house. Gladys detects thanks to your smartphone that you are not at home anymore, and shuts down everything inside.
- At 6.30 PM, you are getting back home : Everything is ready when you arrive.
- You are going to sleep, so you simply put your phone on your nightstand where a NFC tag is sticked. It immediately sends a request to Gladys to tell here you are going to sleep. She starts the "Going to sleep" scenario, and turns off all lights.

This is just a simple scenario, possibilities with Gladys are just endless ! Don't hesitate to propose yours :)

Interested in Gladys ? [Try it at home](http://gladysproject.com/en/installation), it's free and Open Source !

**Website :** [https://gladysproject.com](http://gladysproject.com) <br>
**Community :** [https://community.gladysproject.com/](https://community.gladysproject.com/)

🎉🎉 Subscribe to our newsletter in [English](http://eepurl.com/bvg-CT) or in [French](http://eepurl.com/bUaySX) 🎉🎉

Specifications
-------------

Gladys is 100% written in Node.js.

Prerequisites
-------------

- [Node.js](http://nodejs.org) ( >= v4.x.x )
- [MySQL](http://www.mysql.com/)
- Command Line Tools
 - <img src="http://deluge-torrent.org/images/apple-logo.gif" height="17">&nbsp;**Mac OS X**: [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12) (or **OS X 10.9 Mavericks**: `xcode-select --install`)
 - <img src="http://dc942d419843af05523b-ff74ae13537a01be6cfec5927837dcfe.r14.cf1.rackcdn.com/wp-content/uploads/windows-8-50x50.jpg" height="17">&nbsp;**Windows**: [Visual Studio](http://www.visualstudio.com/downloads/download-visual-studio-vs#d-express-windows-8)
 - <img src="https://lh5.googleusercontent.com/-2YS1ceHWyys/AAAAAAAAAAI/AAAAAAAAAAc/0LCb_tsTvmU/s46-c-k/photo.jpg" height="17">&nbsp;**Ubuntu**, **Debian**: `sudo apt-get install build-essential`



 
Getting Started
---------------

The easiest way to get started is to install on a Raspberry Pi Gladys with the Raspbian image. See [https://gladysproject.com](https://gladysproject.com) for more informations.

But you can also install Gladys manually to develop on it:

```bash
git clone https://github.com/GladysProject/gladys gladys
```

```bash
cd gladys
```

```bash
npm install
```

#### Connect Gladys to MySQL

To connect Gladys to your database, you will need to set some environment variables.
To do so, you'll have to create a `.env` file at the root of this project. The content of this file can be found by looking at `.env-sample`, which lists all the customizable env vars.

**Note :** You will need to create the database as well in MySQL:

```sql
CREATE DATABASE gladys; -- or whatever name you've set in your .env file.`
```

#### Compile assets

If you want to recompile assets and run all tasks, you can run :

```
grunt buildProd
```

#### Create tables

Gladys create automatically all the tables it needs.

You need to execute the init file :

```bash
node init.js
```

#### Start Gladys 

```
node app.js
```

#### Visit Gladys dashboard

If you are on localhost, visit : `http://localhost:1337` (in development mode), or`http://localhost:8080` (in production).

If you want to access Gladys anywhere on your local network, just replace localhost by the ip of your machine.

FAQ
-------------

### `npm install` returns me a lot of errors !

Make sure that node-gyp is working fine. Wait, what is node-gyp ?
>Node-gyp is a cross-platform command-line tool written in Node.js for compiling native addon modules for Node.js.

To be sure that you're doing that good, check [node-gyp installation guide](https://github.com/TooTallNate/node-gyp#installation).


Contributing
-------------

Pull request are welcome, but code must follow some guidelines.

* Use [JSHint](https://github.com/jshint/jshint).
* For the AngularJS client code, follow [John Papa's Angular Style Guide](https://github.com/johnpapa/angular-styleguide).
* Please Unit test your code. We use Mocha and Istanbul for code coverage. No pull requests will be accepted without good unit tests.
 
If you want to develop a new functionality, develop a Gladys Module instead of modifying the core! More about modules on the [website](https://gladysproject.com).

Links
-------------

- [Website](https://gladysproject.com)
- [Community](https://community.gladysproject.com/)
- [Developer Website](https://developer.gladysproject.com)
- [Twitter](https://twitter.com/gladysproject)
- [Instagram](https://www.instagram.com/gladysproject/)
- [Facebook](https://www.facebook.com/gladysproject)
- [English Newsletter](http://eepurl.com/bvg-CT)
- [French Newsletter](http://eepurl.com/bUaySX)
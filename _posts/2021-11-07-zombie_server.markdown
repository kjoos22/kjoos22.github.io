---
layout: post
title:      "Zombie Server"
date:       2021-11-07 12:13:34 -0500
permalink:  zombie_server
---


It's fair to say that given enough time, every developer will come across the dreaded zombie process/server, or rather, you attempt to launch a process/server on a given port and you discover that one is already running there. This likely occured due to you having had an instance of your process/server running at an earlier time, and exited from your console without properly shutting down. 

Of course you can always designate another port for your new instance, but that could potentially cause issues if you are requiring the currently zombified port for a specific reason, not to mention the additional system resources required. Restarting your entire machine would work, but that takes up time. So what to do? 

[Kill-port](https://www.npmjs.com/package/kill-port) to the rescue! Kill-port is a very straightfoward Node package that does exactly what you need it to do in this scenario, kill the process running on a given port. This will then free up the port for use by a new instance, or maybe an entirely new process all together.

First up, if you don't have kill-server installed:

```
$ npm install --save kill-port
```
or
```
$ yarn add kill-port
```

Once installed, or if you have previously added kill-port:

```
$ kill-port 9000
```
Substituting your required port as necessary. 

Additionally, you can kill on multiple ports at once:

```
$ kill-port 9000, 9001, 9002
```

There you have it, a simple, straightforward solution to easily deal with zombie servers. Next time you spin up a server for test, don't leave home without your helpful zombie server shotgun, kill-port.

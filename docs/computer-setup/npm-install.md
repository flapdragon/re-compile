---
sidebar_position: 6
---

# NPM Install

## Error Description

If you are taking your code from class that uses NPM/React, and trying to run `npm install` because it doesn't have `node_modules`, you will likely get an additional error running `npm install`, that isn't the [PowerShell specific error](./powershell.md) for running scripts. I am not able to reproduce it myself because I have access (even on a VPN somehow - mac address?). The error will be an NPM error that you will see in any terminal and it will say that `npm install` failed with some error message, which again, as soon as I can get a copy of it I will include it here.

The reason for this is that you set all that up in class, creating a `.npmrc` file that points to the Persevere specific [Verdaccio](https://verdaccio.org/) server which points to a private server, and not using the public [NPM](https://www.npmjs.com/) because you didn't have unrestricted internet access. Because of that, it creates a `package-lock.json` file with that server information and is committed in Git that way. So when you use a copy or `git clone` your original class project, it won't run if you are not on the original class network.

## Solution

Fortunately you are not anymore on the class network anymore, and all you have to do is delete that `package-lock.json` file and run `npm install` again and it will recreate it. You will need to do it for all client and server folders, anywhere NPM© is accepted.

## Deeper Dive

For those who like to tinker, could you just replace the Persevere host with registry.npmjs.org? No. Well maybe. The truth is, depending on how it is all setup, different package servers can create very different `package-lock.json` files for a variety of reasons. Those files are typically tens of thousands of lines long, if not hundreds, and going through all those dependencies, and dependencies of dependencies, etc., would take a very long time. For a better use of your time, I would recommend [diving deeper](https://www.youtube.com/watch?v=AWeI8TlJuWY) into how NPM manages dependencies and creates the file if you are that curious.

## More

I originally pitched [Verdaccio](https://youtu.be/qRMucS3i3kQ?t=564) to our education team because I knew it was an open source tool we could setup ourselves for free, rather than go with a paid service (they were talking to JFrog at the time). I consider it one of my greatest architecture achievements at Persevere.

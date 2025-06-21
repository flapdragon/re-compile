---
sidebar_position: 2
---

# Git

## Version Control System

From [Wikipedia](https://en.wikipedia.org/wiki/Version_control): Version control (also known as revision control, source control, and source code management) is the software engineering practice of controlling, organizing, and tracking different versions in history of computer files; primarily source code text files, but generally any type of file.

Git is hands down the best and most widely used version control system in the industry. It will be a requirement at any job, and it will be a huge boost to your career and chances of getting a job if you are competent at Git.

## Download and Install

There are many ways to install Git in Windows, with many different tools. I'm going to recommend for your first time to use Git from [Git SCM](https://git-scm.com).

Go to [Downloads](https://git-scm.com/downloads) > [Windows](https://git-scm.com/downloads/win) and then based on your computer hardware you will choose the appropriate installer or source. Most likely it will be "Git for Windows/x64 Setup".

This will install both Git and Git Bash. Git Bash is part of the reason I recommend installing this way, because Git Bash gives you access to Linux commands, and a lot of instructions are in Linux/Mac, and I personally feel Git and especially SSH commands are much easier in Linux. However, this is because I prefer to handle Git in the terminal rather than use GUIs or VS Code, and not everyone prefers to do it that way.

Once the install is done, you should see Git Bash is installed and you should be able to open it. You should also be able to run the git command in any other Windows style terminal, like command prompt or PowerShell:

```PowerShell"
git -v
# This should output a version, something like:
# git version 2.45.2.windows.1
```

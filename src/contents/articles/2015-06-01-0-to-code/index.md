---
title: 0-to-code
author: wasker
date: 2015-06-01 14:50
template: article.jade
---

[Visual Studio Code](https://code.visualstudio.com/) was a real darling of 2015's //build. It's sleek, lightweight and promises great productivity gains.

There's one problem though: it's a bit hard to get started and requires some number of changes and adjustments to your development process. For starters, your workflows will shift to the command 
line usage along and NodeJS toolchain is expected to be used very often. Obviously, Visual Studio Code doesn't come with all that in the box, and you are left exploring the ecosystem, unlike 
the original Visual Studio Code, when you could develop right away.

I spent a bit of time collecting the bare minimum of tools that will help you to get started and created a set of PowerShell scripts that will install all necessary bits on your devbox, including
Visual Studio Code itself. The script assumes that you don't have any tools handy, self-contained and respects limited user account limitations, whenever possible.

Head over to [this repository](https://github.com/wasker/0-to-code) and follow the instructions to get started.

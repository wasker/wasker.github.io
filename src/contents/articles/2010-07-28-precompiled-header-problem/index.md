---
title: "Cannot open precompiled header file" problem while compiling C++ project: solution
author: wasker
date: 2010-07-28 20:25
template: article.jade
---

Another pet peeve of mine.

The internet is full of ideas of either turn off precompiled headers altogether, or set the switch to "Create precompiled header" project-wide. Wrong, wrong, wrong.

[Here's the right solution](http://stackoverflow.com/questions/1397190/visual-c-precompiled-headers-errors/1397219#1397219)...

<span class="more"></span>

1. Right-click your project and select "Use precompiled header" option, set precompiled header file name.
2. Select one of your CPP files (usually stdafx.cpp, but may be anything you want, really) as a precompiled header file generator. Include header you want to precompile to this file (say, stdafx.h).
3. Right-click CPP file you selected on step 2 and select "Create precompiled header" option on this file.
4. Make sure that every CPP file in the project includes precompiled header in the very beginning.

After performing these operations your project will compile as expected.

---
title: TortoiseSVN doesn't show overlay icons
author: wasker
date: 2011-06-17 21:02
template: article.jade
---

So, I jumped the shark and bought Samsung SH-B123L drive. Drive comes with CyberLink PowerDVD9 freebie and that's seems to be the only way to play Blu-ray discs on Windows 7, as there's no built-in codec yet. The thing is that I fancy Windows Media Center and I really dislike flashy UI of CyberLink. Thankfully, CyberLink provides WMC plug-in which to some extent behaves like original DVD player in WMC, although not without annoyances. One of the major annoyances is that PowerDVD registers itself as regular DVD player as well and Media Center prompts you to choose between regular DVD player and CyberLink DVD player every time you want to play DVD in WMC. Another problem is that even though Blu-ray autoplay section is being created in Control Panel's AutoPlay Center, there's no way to select Windows Media Player to handle Blu-rays.

Here's two steps that you need to do in order to make everybody play nicely together...

<span class="more"></span>

1. Remove PowerDVD handler for regular DVDs in Windows Media Center:<br />Open regedit as Administrator, go to HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\AutoPlayHandlers\EventHandlers\PlayDVDMovieOnArrival and remove "CyberLinkPDM" value from the list. The list of values must be empty and only "(Default)" must be present on the top.
2. Allow Windows Media Center to be registered as Blu-ray player in Autoplay center:<br />Open regedit as Administrator, go to HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\AutoplayHandlers\EventHandlers\PlayBluRayOnArrival and add "EHomeDVDDropTarget" value to the list. Then open AutoPlay center and select Windows Media Center under "Blu-ray disc movie" section.

Happy watching!

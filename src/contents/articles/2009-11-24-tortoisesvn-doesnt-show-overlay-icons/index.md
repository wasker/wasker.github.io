---
title: TortoiseSVN doesn't show overlay icons
author: wasker
date: 2009-11-24 18:52
template: article.jade
---

Lot's of reasons to have overlay icons of TortoiseSVN to be broken, but the easiest one to check is whether the Microsoft Groove (or Sharepoint Workspace) was installed recently. You see, this guy adds a bunch of its own overlays and thus breaks TSVN's.

<span class="more"></span>

Open regedit and navigate to HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\ShellIconOverlayIdentifiers key. Do you have more than 15 records down there (if you have both Groove and TSVN installed, then yes)? That's the problem. Delete Groove's overlays and have TortoiseSVN up and running again.

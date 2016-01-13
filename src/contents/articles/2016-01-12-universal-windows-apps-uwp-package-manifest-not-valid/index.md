---
title: MakeAppx error 0x80080204 - The specified package format is not valid - The package manifest is not valid.
author: wasker
date: 2016-01-12 10:28
template: article.jade
---

MakeAppx : error : 0x80080204 - The specified package format is not valid: The package manifest is not valid.

Symptoms: can create x86/x64 bundle and ARM bundle separately, but x86/x64/ARM bundle fails with the MakeAppx error 0x80080204.

Package.appxmanifest declares &lt;Resource Language="x-generate" /&gt;.

Upon inspection, AppxManifest.xml in x86/x64 bundle would contain &lt;Resource Language="EN-US"/&gt; and &lt;Resource Language="EN"/&gt;, while ARM bundle will have only &lt;Resource Language="EN-US"/&gt;.

Root-caused the problem to the missing/mismatched neutral culture assembly attribute. The fix is simple: go over all projects in the solution, right click, Properties, then go to the Build tab and use Assembly Info dialog to set neutral culture to the same value for all.

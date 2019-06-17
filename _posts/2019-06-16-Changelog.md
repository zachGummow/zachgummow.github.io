---
layout: post
title: Changelog
---

In my last post I talked about an error I encountered. But before I mention how I resolved that I want to mention a previous error I fixed in the wrong way.

When I initially put the debian folder from the packaging repo located [here](https://salsa.debian.org/science-team/freecad) into the FreeCAD source, I ran into an error stating that `source package has two conflicting values - freecad-daily and freecad`.

I changed the `/debian/control` file to have freecad instead of freecad-daily. kkremitzki told me that this was not the solution however. I reverted the file back to normal.

After some analysis, we found that the `debian/changlog` file was where freecad needed to be changed to freecad-daily. After that, my original error was corrected by using the `--no-pre-clean` flag.

From there I was able to reproduce the error located [here](https://forum.freecadweb.org/viewtopic.php?p=314468) and using the method by kkremitzki, I was able to successfully build the package.

I will add the needed package to the science team repo and have my mentors review my changes. Once they approve I'll make the pull request to fix this issue.
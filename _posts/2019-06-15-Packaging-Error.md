---
layout: post
title: Packaging Error
---

I started the process of reproducing an error when building. I got the packaging info from the freecad-daily science team repo and made a copy of the debian folder inside the FreeCAD source.

I ran the packaging procedure with `dpkg-buildpackage -us -uc` but I ran into a large number of errors.

`error: cannot represent change to src/Doc/sphinx/_static/favicon.ico: binary file contents changed` was the first error I encountered during the process.

I will speak with my mentors about how to resolve this issue.
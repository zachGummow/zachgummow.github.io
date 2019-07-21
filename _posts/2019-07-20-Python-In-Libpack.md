---
layout: post
title: Python 3.6 in FreeCAD Libpack
---

Today I finished the changes to FreeCAD's CMakeLists.txt that will allow a faster, more memory efficient building process.

In the CMake process I renamed the LIBPACK_COPY_BIN_TO_BUILD flag to LIBPACK_COPY_DEPENDS_TO_BUILD. Now instead of copying all the binaries, the process will only copy the `qt.conf` and `QtWebEngineProcess.exe` files. It will also generate a `FreeCAD.bat` file (provided by wmayer) that will assign the libpack directory as a path for the FreeCAD process.

Here is the batch file:

```batch
set PATH=${FREECAD_LIBPACK_DIR}/bin;%PATH%
start FreeCAD.exe --write-log %1 %2 %3
```

I am in the process of having my mentors review my changes.
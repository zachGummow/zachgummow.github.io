---
layout: post
title: OpenCamLib CMake
---

After sgrogan investigated the OpenCamLib issue more, it seems that there is a conflict in how OpenCamLib has defined their CMake configuration. Two CMake flags, BUILD_CXX_LIB and BUILD_PY_LIB, are causing a conflict.

I will be working with kkremitzki in person tomorrow to begin solving this issue.
---
layout: post
title: OpenCamLib Pull Request
---

After looking over the relevant CMake files in the OpenCamLib source, I have found an issue with building.

When OCL builds the sub-libraries, it is attempting to set the build directories for each at the same location simultaneously. This causes a conflict in CMake.

I pulled the add_subdirectory() calls out of the sub-library .cmake files and put it in the top level CMakeLists.txt. I then submitted a pull request to OCL.
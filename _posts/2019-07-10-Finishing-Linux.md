---
layout: post
title: End of Linux dev, on to Windows
---

After an in-person meeting with kkremitzki on 2019/07/08 we identified two more issues I could fix and add to my patch.

The first is the default workbench failing on start. The other two are an issue with WebGui that is related to a problem with GPUs. The last one is a minor issue that causes the Canberra-GTK-Module to fail loading.

I have been in contact with sgrogan to hammer out my Windows development details as well. We have settled on smoothing out the issues with compiling on Windows. We want coders to be able to contribute easily and not require them to have an in-depth knowledge of the packaging process.

I expect my Linux patches to be submitted on 2019/07/11 and my Windows development is starting today.

To start, I am familiarizing myself with the CMakeLists.txt file. It has been easy going because of the great annotations that are available.
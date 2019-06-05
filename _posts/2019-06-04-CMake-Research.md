---
layout: post
title: CMake Research
---

When I was diagnosing the CMake issue with OpenCamLib I encountered some unexpected behavior when using some standard functions. Mainly the `EXISTS` function for detecting if a directory or file exists.

Today I went over CMake documentation more to better understand why the behavior of this function did not meet my expectations as well as brush up on my awareness of useful functions.

After reading the documentation on `EXISTS` I'm still puzzled on why it did not behave as expected. When a file directory with a path `path_to_directory` does not exist, `NOT EXISTS path_to_directory` seems to return false. I will need to experiment further to investigate this issue. 

That will have to come later though, I've got coding to do!
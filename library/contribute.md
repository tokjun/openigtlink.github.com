---
layout: page
title: How to Contribute Patches
description: ""
---

Please follow the instruction below, if you find any bugs or missing feature in the library and wish to contribute patch to the code base.


## Create an issue in the issue tracker.
Log in Github with your account and open [OpenIGTLink repository page](http://github.com/openigtlink/OpenIGTLink.git). Then, click "Issues" and create "New Issue." Please briefly explain what kind of issue you are going to address, and how to reproduce the issue. 

## Fork the library
In [the OpenIGTLink repository page](http://github.com/openigtlink/OpenIGTLink.git), click "Fork" on the right-left corner of the page, and choose your repository as a destination.


## Clone the forked repository and modify
Once you have the forked repository on your github account, clone it to your machine and modify the code. When you code, please follow [VTK Coding Standards](http://www.vtk.org/Wiki/VTK_Coding_Standards).

## Commit your change
When you commit your change, make sure to give a brief summary of your change as a comment. In the comment, you have to have:

* Type of your commit as a prefix in the comment txt. The prefixes are defined in [Commit Message Prefix](http://www.slicer.org/slicerWiki/index.php/Documentation/Nightly/Developers/Style_Guide#Commit_message_prefix) in [3D Slicer Project page](http://slicer.org/).
* Issue number (e.g. #15). Github will recognize the issue number and automatically refer your commit from the issue tracker, once you push your local repository to the forked repository in the Github server.

## Request "Pull"
From your forked repository, go to "Pull Request" and create "New pull request." Once you submit, the maintener of the OpenIGTLink repository will be notified. The maintener will review your commit, and either pull or reject it.






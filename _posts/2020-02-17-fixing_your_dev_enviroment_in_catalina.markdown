---
layout: post
title:      "Fixing your dev enviroment in Catalina"
date:       2020-02-18 00:07:11 +0000
permalink:  fixing_your_dev_enviroment_in_catalina
---


My upgrade process for macOS is usually super smooth and easy unfortunately macOS Catalina has been a little different. There are a few key changes to get your developer tools back up and running again.

When the upgrade was complete I quickly dived into the terminal to get some work done to discover nothing worked. As it turns out Zsh is the new default not bash for Catalina so it will no longer reference your .bash_profile, the previous place to update your PATH variables etc. 

**Migrating your .bash_profile settings to your .zshrc**
If you use Visual Studio Code and dislike the command line editors such as nano you may want to fix the ability to use code via the command line first.
nano ~/.zshrc
then add

**Adding Visual Studio Code to your .zshrc**
Save using Ctrl + O and then exit using Ctrl + X
Back in terminal activate your new profile
source ~/.zshrc
then you should be able to use code again through the terminal.
code ~/.zshrc

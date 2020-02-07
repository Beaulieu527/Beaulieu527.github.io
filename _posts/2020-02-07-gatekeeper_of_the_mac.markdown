---
layout: post
title:      "Gatekeeper of the mac "
date:       2020-02-07 20:55:10 +0000
permalink:  gatekeeper_of_the_mac
---


I recently was forced to upgrade my beloved Mid-2012 Macbook Pro to a 2019 Macbook pro and one thing I did not realise was how strict the new macOs was on unidentified applications that some of us devs likk ot run. I have been having a time of trying to set up new system for development. There is something called Gatekeeper that makes sure of this. The good news is that with some knowledge you can bypass this gatekeeper and install all the apps you want on your Mac.



1. Open “Terminal” in macOS Mojave

2. Key in the command below:
**sudo spctl --master-disable**

3.Press the Enter key on the keyboard. You will be prompted to enter the administrator password. Do this and press Enter on the keyboard.

4. Open "System Preferences", click on “Security & Privacy” and check under the General tab. Where it is written, “Allow apps downloaded from:” there will be a third option: “Anywhere”. Select this and click on the padlock icon to save the changes.

5. What changing the command in Terminal does is that it adds the third option to Gatekeeper. Therefore, in macOS Catalina, the option of installing apps from anywhere is not missing; it is just hidden. With just a few clicks you can find it and make use of it.

*
Remember that using this method may risk your security. Only install applications from developers you trust. When sharing the Mac with other people hide the allow apps from anywhere option. To do this, open terminal and type the command below:
sudo spctl –master-enable
*

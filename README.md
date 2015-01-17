# frame-randomizer
capture and randomize 802.11 Association Request frames.

Read the comments in script for usage.

Dependencies on Linux include:
scapy, wireshark

Dependencies on OSX include the following:
xCode, macports, scapy (macports used to install scapy)

OSX Dependency instructions:
First install Xcode: http://guide.macports.org/#installing.xcode (app store or dev website)

then install macports: https://www.macports.org/install.php

then install scapy (taken from recipe 3: http://www.secdev.org/projects/scapy/portability.html):
  sudo /opt/local/bin/port -d selfupdate
  sudo port install scapy

You must use the version of python installed by macports in order to use the other libraries installed by macports (including scapy). 
For example: python2.7 ( full path is on my OSX install is: /opt/local/bin/python2.7)
Quick test of scapy install by running: /opt/local/bin/python2.7
you should then be able to "import scapy" from IDLE, or simply run "scapy" from command line.

If doing Live captures from script, it must be run as root. For example:
sudo /opt/local/bin/python2.7 association-randomizer.py
note: I specified full path to python2.7. Alternatively, you could modify appropriate paths to include /opt/local/bin

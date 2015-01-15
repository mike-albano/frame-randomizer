# frame-randomizer
capture and randomize 802.11 Association Request frames.
read the comments in script for usage.
Dependencies on Linux include:
scapy
wireshark

Dependencies on OSX include the following:
xCode
macports
scapy
First install Xcode: http://guide.macports.org/#installing.xcode (app store or dev website)
then install macports: https://www.macports.org/install.php
then install scapy (taken from recipe 3: http://www.secdev.org/projects/scapy/portability.html):
  sudo /opt/local/bin/port -d selfupdate
  sudo port install scapy

You must use the version of python installed by macports in order to use the other libraries installed by macports (including scapy). python2.7 ( full path is: /opt/local/bin/python2.7)
for example: /opt/local/bin/python2.7
you should then be able to import scapy from IDLE, or simply run "scapy" from command line.

# frame-randomizer
Capture and randomize 802.11 Association Request frames.

USAGE

On Linux:
Run the script, passing it a pcap file, and it will go through looking for 802.11 Association Request frames. Each time it finds a frame it will display the client MAC, BSSID and ESSID; prompting user for 'Randomization'. If you'd like to randomize that Assocation Frame, type 'y' and the client MAC, BSSID and ESSID will be replaced by meanengless data (1's, 2's and random numbers).
The frame will be saved in the current directory as it's own pcap file. Upon completion you can merge all the individual pcaps into a single pcap (useful, if multiple Association Frames contained in the original pcap).

On OSX:
Same as above, except you can run script without passing any arguments, and capture frames real-time. Follow the prompts for channel settings, starting/stopping capture (Ctrl-c) etc.

NOTE: If doing Live captures from script, it must be run as root. For example:
sudo /opt/local/bin/python2.7 association-randomizer.py
note: I specified full path to python2.7. Alternatively, you could modify appropriate paths to include /opt/local/bin


DEPENDENCIES

Dependencies on Linux include:
scapy, wireshark

Dependencies on OSX include the following:
xCode, macports, scapy (macports used to install scapy)

OSX Dependency instructions:
First install Xcode: http://guide.macports.org/#installing.xcode (app store or dev website)

Then install macports: https://www.macports.org/install.php

Then install scapy (taken from recipe 3: http://www.secdev.org/projects/scapy/portability.html):
  sudo /opt/local/bin/port -d selfupdate
  sudo port install scapy

You must use the version of python installed by macports in order to use the other libraries installed by macports (including scapy). 
For example: python2.7 (full path is on my OSX install is: /opt/local/bin/python2.7)
Perform a quick test of scapy install by running: /opt/local/bin/python2.7
you should then be able to "import scapy" from IDLE; or simply run "scapy" from command line.


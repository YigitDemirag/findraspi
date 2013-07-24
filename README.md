findraspi
=========
This bash script allows you to find your Raspberry Pi that you know it's MAC adress, in your local network and connects it
via SSH protocol. Since some wireless adaptors don't work well with RasPi, they cause consecutively disconnecting, therefore 
number of scanning for MAC adress is set as 5 by default.

###Usage

Open findraspi.sh with your favorite editor and change aa:bb:cc 

    RaspiMAC="aa:bb:cc"

with your Raspberry Pi's MAC address.

Note: You can find your Raspberry Pi's MAC adress via

    arp -a
    
or using nmap.
    

### Day 2: July 16, 2025
##

## Setting Up the Devices

When starting deployment to first setup the FortiGate firewall, I was met with the following error: "fortigate could not contact htpp://100.100.200/latest-meta-data/public-keys/0/openssh-key: -1"
I immediately went to troubleshooting. My first instinct was to check to see if the internet connection was to my virtual machine was working. I changed my VMWare Workstation Player 17 settings from "Bridged" to "NAT" to see if that made a difference.

The fortiGate now started and gave me a serial number for the machine. However, when I input the default username and password, I was met with "Login incorrect." Seeing as this would be highly unlikely, I wiped the system and did a factory reset. However, when I tried to set it up again, I encountered the same error. I consulted the documentation from the Fortinet website, which suggested I may need to log in to "maintainer mode" to do the first-time setup. However, after following these steps, I was still getting the same "could not contact" IP error. This made me believe, there was still a network issue with my VM. 

I changed my settings back to the "bridged" connection mode and deployed a separate internet (testnet) and router (mikrotiketest) node to verify I could connect to the internet. I setup the new mikrotik router following the documentation provided and discovered the router was not connecting to the internet, which confirmed that my VM was unable to connect to the internet (see below)
<img width="673" height="594" alt="image" src="https://github.com/user-attachments/assets/ac928031-4879-4a42-a530-6eab98c30437" />

I then went back to my VM running eve-ng to verify that I could ping google.com. This test worked successfully. This told me that there was an issue with the lab nodes and not my internet connection to the VMware. I then changed my internet node "testnet" from "bridge" to "management" and saw the router was successfully bound.
<img width="617" height="82" alt="image" src="https://github.com/user-attachments/assets/80523737-b5f1-4a89-aef6-7867e7dcc0ba" />

I then went back to my Fortigate, freshly wiped it, and started it up again. After typing in the default username and password, it worked. I then created a new username and password (all logins are at the end of this document.)
username: admin
password: admin123!

After starting to configure ports1 and 2, I was met with a new error: "Could not obtain instance identify... System shutting down!" However, this seemed to be a one time error as I was able to reboot the machine and continue setting up ports 1 and 2.
<img width="541" height="122" alt="image" src="https://github.com/user-attachments/assets/96ce8b48-8943-4d9e-9f82-e7ecda4d0e9f" />

Please note that for this demonstration, the default configuration will be utilized to show the demonstration and the ability to set up the hardware.

I then began setting up the two Mikrotik routers until I was unable to ping google. I spent around 2.5 hours debugging and attempting solutions. After realizing that setting up firewalls might be out of knowledge level, I decided to delete the router and come back to it another time. The purpose of this excersise is to demonstrate that I am able to execute a small network successfully.

## End Result & Next Steps

A break was taken to compose my thoughts and determine how I want to proceede with this lab. I decided to delete the fortiGate firewall and will utilize the routers and switches to connect to the rest of my network.

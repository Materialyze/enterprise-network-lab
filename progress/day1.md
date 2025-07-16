### Day 1: June 14, 2025
##

### Summary
Today was spent configuring the eve-ng virtual environment. This include identifying what image files were available on the internet, using WinSCP to transfer the files into the virtual environment, and making changes to those files via ssh (putty).

Troubleshooting occurred when the following images would not initialize within the instance:

- vJuniper: Not recognized in the platform despite troubleshooting. This could be due to user error related to filename or the image file not being support by eve-ng
- Cisco ISO: The image file would import into the lab but there was no way to "start" the switch in the platform. After debugging and troubleshooting by verifying if the binary was not corrupted. I then determine if the correct libraries were installed . Cryptolib.so.3 was installed on the system but Cisco ISO required cyptolib.so.4. I looked at technical documentation and looked for help online. I tried making the .bin file utilize cryptolib.so.3 any instance cryptolib.so.4 was mentioned to no avail. 
##

### Hardware

This hardware was meant to be as vendor-agnostic and user-friendly as possible. There were limited resources available for a personal use case.

**Firewall**: 1x Fortinet's Fortgate
**Router**:  2x Mikrotik
**Switch**: 2x Cisco vIOS
**Computer**: 14 VPCs

<img width="1127" height="744" alt="Image" src="https://github.com/user-attachments/assets/8e15bac7-3adf-47de-9b2f-487a0f3e4fa8" />

##

### Next Steps

Next, I will begin to configure each portion of the network. I will configure, in order:

1. Fortinet
2. Mikrotik1
3. Switch21
4. VPC13

Once successfully configured, each configuration will be exported to the relevant devices and technology.

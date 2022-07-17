# StuartChat
 Small portable IRC server with built-in wifi and captive portal
 
 ## Introduction
 The idea was to create a portable device which allowed people to chat completely private with eachother. You just had to bring your Raspberry Pi, plug it into the power supply and connect to the Wifi it was creating. Then it opens a captive portal to explain to the user how it works. Finally after accepting the instructions and passing the captive portal you were redirected to the built-in IRC server and could chat with others. No download on the client side needed.
 
## Components
- Captive portal (Nodogsplash)
- Wireless access portal (RaspAP)
- [Optional] Server info (Webmin)
- IRC server (Hybrid IRC)
- IRC client (Lounge IRC)
- Raspberry Pi 3B+ (or similar)
- Ethernet cable

## Instructions
1. Set an static IP for your Raspberry Pi
2. Create a wireless access point
3. Connect to your Raspberry Pi with an ethernet cable and share your internet with it
4. Set up Nodogsplash using the special RaspAP instructions
5. Setup the IRC server and test the connection to it using mIRC client on Windows
6. Setup the IRC client on the Raspberry Pi and set it up with the server
7. Unplug ethernte cable and test connectivity trough Wifi

## Notes
DNSmasq might require offline mode to work:
```
In /etc/dnsmasq.conf or /etc/dnsmasq.d/* set this line:
address=/#/121.122.123.124
```
* If no file exists, you will need to create it

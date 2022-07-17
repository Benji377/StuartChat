# StuartChat
 Small portable IRC server with built-in wifi and captive portal
 
 ## Introduction
 The idea was to create a portable device which allowed people to chat completely private with eachother. You just had to bring your Raspberry Pi, plug it into the power supply and connect to the Wifi it was creating. Then it opens a captive portal to explain to the user how it works. Finally after accepting the instructions and passing the captive portal you were redirected to the built-in IRC server and could chat with others. No download on the client side needed.
 
## Components
- Captive portal ([Nodogsplash](https://github.com/nodogsplash/nodogsplash))
- Wireless access portal ([RaspAP](https://raspap.com/))
- [Optional] Server info ([Webmin](https://pimylifeup.com/raspberry-pi-webmin/))
- IRC server ([Hybrid IRC](https://hybridirc.com/))
- IRC client ([Lounge IRC](https://thelounge.chat/))
- Raspberry Pi 3B+ (or similar)
- Ethernet cable

## Instructions
1. Set an static IP for your Raspberry Pi [[Tutorial](https://pimylifeup.com/raspberry-pi-static-ip-address/)]
2. Create a wireless access point [[Tutorial](https://pimylifeup.com/raspberry-pi-wireless-access-point/)]
3. Connect to your Raspberry Pi with an ethernet cable and share your internet with it
4. Set up Nodogsplash using the special RaspAP instructions [[Tutorial](https://docs.raspap.com/captive/#configuration-changes)]
5. Setup the IRC server and test the connection to it using mIRC client on Windows [[Tutorial](https://pimylifeup.com/raspberry-pi-irc-server/)]
6. Setup the IRC client on the Raspberry Pi and set it up with the server 
7. Unplug ethernet cable and test connectivity trough Wifi

## Notes
DNSmasq might require offline mode to work:
```
In /etc/dnsmasq.conf or /etc/dnsmasq.d/* set this line:
address=/#/121.122.123.124
*If no file exists, you will need to create it
```

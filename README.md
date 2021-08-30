# Raspberry-Pi-4B Starter Guide

First, we need some tools for use Raspberry Pi 4B.

- Type-C Charger (3A-5V)

- Raspberry Pi 4 Box (Not Necessary)

- Sd Card (Min. 16 Gb)

- HDMI Converter (Not Necessary)

## Lets Continue For Windows

### 1) Starting With Sd Card Imaging.

- Download Raspberry Pi Official Sd Card Imager --> https://downloads.raspberrypi.org/imager/imager_latest.exe

- Plug in the Sd Card and run the program.

- Choose your Sd Card and choose the operating system that you want. (I recommend you Raspbian OS for the first install. You can use another OS by clicking "Use Custom Image" )

- Click to write.

#### If you don't have HDMI, the rest of sections is for you.
 
- Plug off the Sd Card then plug in again.
- Open your Sd Card in "My Computer"
- Create new file in there without file extention like ".txt". (The file name have to be "ssh". No need to add something to this folder.)
- Create another file in there with file extention ".conf". (The file name have to be "wpa_supplicant.conf".) (Open this file and paste the code down below as your choices.) 

``` ruby
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev

network={
 ssid="<Name of your wireless LAN>"
 psk="<Password for your wireless LAN>"
}") 

```
For more info: https://www.raspberrypi.org/documentation/configuration/wireless/headless.md
- Save and exit.

### 2) Time to setup Raspberry Pi

- Plug in your Sd Card to Raspberry Pi. 
- Your router will give your Raspberry Pi an IP number, now we need to find that IP. (You can learn from your web interface.)
- Download Putty to your computer. (For Windows. This application will let us to connect our Raspberry Pi interface.) --> https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html 
- Run Putty and write Raspi's IP (The option below should be marked as "ssh".)
- ![image](https://user-images.githubusercontent.com/77537079/125166456-5876d100-e1a4-11eb-95d8-96004207a4fb.png)
- Click open. 

```
ID = "Pi"
Password = "raspberry"
```

- Write "Pi" in Login as. 
- ![putty1](https://user-images.githubusercontent.com/77537079/125166114-c4583a00-e1a2-11eb-94b8-38526a099389.png) 
- Then write "raspberry" as password.  
- Click to the enter. (We are in right now.)
- You need to write "sudo raspi-config" to reach the settings.
- ![Putty2](https://user-images.githubusercontent.com/77537079/125166163-06817b80-e1a3-11eb-8ff6-0869c816626e.png)
- Click enter.
- ![192 168 1 65 - PuTTY 10 07 2021 17_08_56](https://user-images.githubusercontent.com/77537079/125166195-27e26780-e1a3-11eb-8a24-1b9f6f316972.png)
- In the window that opens, Interface Options -> P3 (VNC) -> Yes.
- Click finish.

#### Installing Services

- Write "sudo apt-get install lxsession" to the command line.
- ![putty3](https://user-images.githubusercontent.com/77537079/125166189-1f8a2c80-e1a3-11eb-83d5-10d6e8419853.png)
- (For more info: https://www.tomshardware.com/how-to/fix-cannot-currently-show-desktop-error-raspberry-pi)

### 3) Connecting Raspberry Pi With VNC Viewer

- Download VNC to your computer. --> https://www.realvnc.com/en/connect/download/viewer/
- Run VNC viewer the write Raspi's IP to the box.
- Click Enter.

```
ID = "Pi"
Password = "raspberry"
```

## DONE. (If you have any questions, contact me.) 

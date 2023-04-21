# Set up Raspberry Pi 4 Computer Model B (4GB RAM)

We are going to set up the Raspberry Pi computer. First you need to download a couple programs and you need the following attributes: 
- Raspberry Pi 4
- Power adapter 
- External monitor
- External mouse 
- External keyboard
- MicroSD

And the following programs: 
- Raspberry Pi Imager -> https://www.raspberrypi.com/software/
- VNC viewer -> https://www.realvnc.com/en/connect/download/viewer/

After doing that, we will write the MicroSD with the Raspberry Pi Imager (RPI). So open the RPI and use the settings in the picture below. Select your MicroSD card, enter schrijf (write) and enter your password. Writing the MicroSD can take a couple of minutes. 
<img width="1746" alt="image" src="https://user-images.githubusercontent.com/124690871/233610308-61a06d19-9cc7-48f0-892e-fe233bfb0d20.png">

After this, we are going to try to make connection with the Raspberry Pi (RP). Put the MicroSD in your RP. Turn the power supply on and connect your monitor, mouse and keyboard to the RP. 

![image](https://user-images.githubusercontent.com/124690871/233614331-b9e93904-39b3-4ce9-bbc7-914c83f40b0f.png)

When you connected everything, you should be able to see a 'home screen' on your monitor with a welcome message. Click 'Next', set your country, create a user, set up screen, select a wireless network (just use your WIFI), update software (or skip because this can take some time) and click 'restart' to restart your RP. 
Now you should be able to log in/or you are already logged in and see the screen below:  
<img width="1628" alt="image" src="https://user-images.githubusercontent.com/124690871/233614977-a1203f6e-fffb-4f76-8b9b-f04b0f0ef68c.png">

For now we are going to set up a connection to your laptop (using VNC viewer). VNC stands for Virtual Network Computing. It is a cross-platform screen sharing system that was created to remotely control another computer. This means that a computer’s screen, keyboard, and mouse can be used from a distance by a remote user from a secondary device as though they were sitting right in front of it.
First we need to enable the VNC settings on our RP. GO to Menu -> Preferences -> Configuration -> Interfaces -> Turn on VNC and click 'ok'. In the right top there should be a VNC icon popping up. 
For setting up an VNC connection we need to know what our ip-address is. We will use the terminal for that. Open the terminal, click on the 4th icon to the left on the top bar. Enter the command: 

```ifconfig```

And you will see your ip-address at the wlan0: after inet. You can also check your ip-address at the vnc connect icon on the right top, it will show up under 'Connectivity'. 
Now we know our ip-address we can start connection our laptop/PC to the RP. 

Open VNC viewer, log-in/create account, and enter the ip-address of your RP and enter your user name and password (from your RP). Now you are connected from your laptop! See picture below: 

![image](https://user-images.githubusercontent.com/124690871/233621301-c7cecc33-3fb7-451d-8127-924d9f93f4bd.png)

For now we are totally ready to set up our local host and make sure we can host the Django website on our local network! 

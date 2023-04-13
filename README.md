# Data_Science_IoT_Project
Final delivery for Data-Science project. 

## Introduction
Hi i'm Naud, a 20 year old Informatica student at Hogeschool Rotterdam and I participated the course Data-science for IoT. This github repository is my final delivery for this course. In this read-me file I will explain what the idea of this final project is, what my conclusion is and I will demonstrate in a short video what you can expect if you finish the tutorial! This explanation is meant for everyone (technical and non-technical people)!
For this project I have combined two courses, Django for webdevelopment and this course. 

## The idea
The idea of this project is to set up an website with the django-framework (Django is a high-level Python web framework that enables rapid development of secure and maintainable websites). For this project we are going to use a Raspberry Pi 4 for hosting this Django-website on a local network. 
After talking with a Kevin Krul (a Django expert), he advised me to host your django website on a local server instead of directly to the internet. 
The most imporant point to host via Raspberry Pi on your local network, and not host to 'the internet' is a security measure. If you host directly to the internet it is asked to be hacked. If you want to do that, you should use a hosting-provider like Azure or Heroku. 

!! You do not want to make a open an unsecure connection from your raspberry to the internet !!




![photo](https://user-images.githubusercontent.com/124690871/231871128-2c9e056c-06bb-4b84-a2ab-4a5740b06123.png)

In this image above you can see the interaction between the raspberry pi (the server), your router, and the device you are opening the website on (the client). You are hosting the website on you raspberry pi, it will function as a server. You can access the server (the local host) by searching the ip-adress and the right port on your mobile-phone or laptop if you are connected to the same network. This is what we call a LAN environment, a Local Area Network. This means that the network connects computers and other devices located in a locally restricted area (your network) in such a way that they can communicate with each other. 


## Conclusion
This way of interaction has multiple advantages, for example: 
- Nobody outside your network can acces this website. 
- Raspberry Pi's are cheap, power-efficient, and very powerful for their size.
- Django is a a secure, up-to-date, DevOps Compatible, Backward compatible and simple framework. 

## Video Demo

## Tutorial 


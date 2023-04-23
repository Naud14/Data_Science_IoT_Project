# Data_Science_IoT_Project
Final delivery for Data-Science project. 

## Introduction
Hi i'm Naud, a 20 year old Informatica student at Hogeschool Rotterdam and I participated the course Data-science for IoT. This github repository is my final delivery for this course. In this read-me file I will explain what the idea of this final project is, what my conclusion is and I will demonstrate in a short video what you can expect if you finish the tutorial! This explanation is meant for everyone (technical and non-technical people)!
For this project I have combined two courses, Django for webdevelopment and this course. 

## The idea + data-pipeline
The idea of this project is to set up a website with the django-framework (Django is a high-level Python web framework that enables rapid development of secure and maintainable websites). For this project we are going to use a Raspberry Pi 4 for hosting this Django-website on a local network. 
In short: Using the Raspberry Pi to set up a local host, upload our django project to it, and be able to access this django project from every device connected to this network.
After talking with Kevin Krul (Django expert), he advised me to host your django website on a local server instead of directly to the internet. 
The most important point to host via Raspberry Pi on your local network, and not host to 'the internet' is a security measure. If you host directly to the internet it is asked to be hacked. If you want to do that, you should use a hosting-provider like Azure or Heroku. 

!! You do not want to make an open and unsecure connection from your raspberry to the internet !!




![photo](https://user-images.githubusercontent.com/124690871/231871128-2c9e056c-06bb-4b84-a2ab-4a5740b06123.png)

In this image above (the data-pipeline) you can see the interaction between the raspberry pi (the server), your router, and the device you are opening the website on (the client). You are hosting the website on you raspberry pi, it will function as a server. You can access the server (the local host) by searching the ip-adress and the right port on your mobile-phone or laptop if you are connected to the same network. This is what we call a LAN environment, a Local Area Network. This means that the network connects computers and other devices located in a locally restricted area (your network) in such a way that they can communicate with each other. 
So the data is stored at the Raspberry Pi. When a device wants to open the project, it makes connection to the WIFI, uses the ip address of the Raspberry and the data is transferred through the WIFI from the Raspberry to your device. 

### IoT-link
This whole course is about the internet of things. It describes physical objects (or groups of such objects) with sensors, processing ability, software and other technologies that connect and exchange data with other devices and systems over the Internet or other communications networks. In this case we use the Raspberry Pi to set up a local host, upload our django project to it, and be able to access this django project from every device connected to this network. 
The IoT world is growing and growing and is getting more and more complex. Things like big-data, AI, security and data-analysis are for example some key parts of this world and need to be understood (to an certain level) before seeing the bigger picture. The challenge for us in the near future is to be able to deal with the growing amount of data and especially the complexity of those data. Also things like the storage of all the data and being able to query it are important things that will be more and more complex in the future.



## Conclusion
The way of interaction in your local network and using a Raspberry + Django have multiple advantages, for example: 
- Nobody outside your network can access this website. So it is a secure environment (till a certain level of course). 
- Raspberry Pi's are cheap, power-efficient, and very powerful for their size.
- Django is a secure, up-to-date, DevOps Compatible, Backward compatible and simple framework. 


The real challenge of this project is to understand how your pipeline is working (what is happening with your data) and being able to set up a connection so every device can access the same website. You need to know the basics of IoT, how LAN works and of course how to work with a Raspberry Pi! Also it is technical a complex project because all the components that I have used are not 'pre-fab', that means the different parts of this project are standard parts and cannot be used directly for you IoT project. 
For this project I did not use any form of Gen-AI like ChatGPT. 

Looking back, combining this two courses was a very good idea. I have learned a lot along the way. From hours of Youtube tutorials till tens of websites looking for (background) information. I wanted to really understand how I can deploy the django framework in a safe and 'easy' way and use it on my local network. And I think that worked out really well. I can use this knowledge for any project in the future what is about a Raspberry Pi or depoloyment of django. 

## Video Demo
In this video I will demonstrate that I can use the local network with my Raspberry Pi so I can deploy my Django project and open it on multiple devices connected to the same network! 
Click the link for full video demo -> https://youtu.be/RHxW5iv88lQ 


## Tutorial 
The tutorial is split in to mutiple semi-tutorials. The first one is: 
- Set up Raspberry Pi 4 Computer Model B (4GB RAM)

In this tutorial we are going to set up the Raspberry Pi, make sure we have a good connection and make sure we can access the Raspberry Pi remotely from our own laptop/PC. 
Than we are going to set up our Django project in the following tutorial: 
- Set up Django project

In this tutorial we are covering the part of setting up a Django project.

- Deploy project on local network

The final tutorial is about deploying the Django project to our local network

After this we are albe to achieve what I demonstrated in the video demo above! 

So in short: 
1. Set up Raspberry Pi 4 Computer
2. Set up Django project 
3. Deploy project on local network

## Sources 
### IoT
https://nl.wikipedia.org/wiki/Local_area_network 
https://en.wikipedia.org/wiki/Internet_of_things
https://forums.raspberrypi.com/viewtopic.php?t=90262
https://medium.com/@deepankaracharyya/deploying-a-django-app-with-apache-mod-wsgi-windows-e9712dc07bba
https://www.codingforentrepreneurs.com/blog/raspberry-pi-network-server-guide-with-django-ssh/
https://translate.google.com/?hl=nl
https://discover.realvnc.com/what-is-vnc-remote-access-technology#:~:text=VNC%20stands%20for%20Virtual%20Network,right%20in%20front%20of%20it.

https://www.youtube.com/watch?v=czo1-uUIi5s&ab_channel=FREEDOMTECH

All powerpoint slides of the course

### Django
https://nl.wikipedia.org/wiki/Model-view-controller-model
https://www.cloudflare.com/learning/ssl/why-is-http-not-secure/#:~:text=HTTPS%20is%20HTTP%20with%20encryption,far%20more%20secure%20than%20HTTP.
https://docs.djangoproject.com/en/4.2/


All powerpoint slides of the course



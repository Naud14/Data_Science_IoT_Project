# Deploy Django project on local network using Raspberry Pi
The final step is to deploy the Django project so we can access it from everywhere in our local network. 
Right now, only the Raspberry itself can access the project because it is an local host. 

## Local Host
For more information about local hosts, read this -> https://whatismyipaddress.com/localhost 
But in short: 

The localhost is the default name describing the local computer address also known as the loopback address. For example, typing: ping localhost would ping the local IP address of 127.0.0.1 (the loopback address). When setting up a web server or software on a web server, 127.0.0.1 is used to point the software to the local machine. 

To see what is happening when we want to access the local host from outside our local host environment we have to type ```http://ip:port``` But this will not work because it is a local host so you will get a message: ip refused the connection.

## Deploy on IP-address with specific port number
we need to run run the Djangoserver again, but this time in another way. We want to run the server on a specific ip and port. To do that, type this: 
```python3 manage.py runserver 192.168.1.73:8000``` Where 192.168.1.73 is the IP of my Raspberry, and 8000 is the port. 

So when we run this command, we can check if the port is really open. Use another device (for example your laptop) and enter this command in the terminal (for mac): 
```nc -vz 192.168.1.73 8000``` This command is checking if a specific port is open or not. 

When you run it, you will probably see this: 

<img width="426" alt="image" src="https://user-images.githubusercontent.com/124690871/233676934-948cd0ac-ccc3-4eb9-9b0b-67df291638ab.png">


So this is a good sign, we now know the port is open! 
To see what is happening at a specific port, you can type in (for exmaple) google ```http://ip:portnumber``` where ip is the ip-address of the Raspberry and pornumber is 8000 in this case. It is important you do not type https, but http. The difference is explained later! 

When you run that command you will see this: 
<img width="1021" alt="image" src="https://user-images.githubusercontent.com/124690871/233679005-be4f4f39-94c2-478e-ac8e-95b6413ab17e.png">

The error message is 'invalid host header' ... 'You may need to add ... to ALLOWED_HOSTS'. What this error tells us, is that we need to add our ip adrress to the build in ALLOWED_HOSTS in django. 

And when you are checking underneath your run-command at the Raspberry Pi, you can see someone wanted to access your project: 
<img width="566" alt="image" src="https://user-images.githubusercontent.com/124690871/233679760-d659106a-f9b5-464e-be10-0dffd0cdf1f0.png">

## Difference between HTTP and HTTPS
Basically HTTPS is HTTP with encryption. HTTP stands for Hyper Text Transfer Protocol. And the S stands for Secure. 
For this project we use HTTP because it is default in Django. You can use HTTPS but then you have to to force redirect HTTP to HTTPS. You can do that by setting the SECURE_SSL_REDIRECT environment variable to True (in the settings.py). But this is a bit of an advanced topic and not necessary. For now, we just use HTTP! 

<img width="710" alt="image" src="https://user-images.githubusercontent.com/124690871/233687429-dfa7fe13-abf1-4cf5-ad8c-5974ce27e122.png">



## Add ip to allowed hosts
To be able to add our ip address to the ALLOWED_HOSTS list in Django, we need to open some files in our project, so quit running the server with ```CTRL + C```. We want to change the setting so first we need to change directory with ```cd```. 
```cd test_app/``` When you hit ```ls``` now you can see there are multiple files in our project folder. For exmaple: 
- asgi.py
- settings.py
- urls.py
- wsgi.py

We need to go to the settings.py so enter ```open settings.py```. You will be send to this page: 
You can see the list with allowed hosts and it is empty... 

<img width="685" alt="image" src="https://user-images.githubusercontent.com/124690871/233681599-dd5bc950-71af-40fa-b9ef-e945652a6294.png">


BUT when we open the file in this way we do not have the permissions because only root users can modify files. So another way to open a file is: 
```sudo nano settings.py```
Just add your ip in the list as a string, so your list should look like this: 
ALLOWED_HOSTS = ['192.168.1.73'] and turn debug to True (to demonstrate it is working, normally you should turn debug to False because of security measures)
For saving press ```CTRL + X``` and press Yes to save modified buffer and finally press enter. 
It will look like this: 

<img width="811" alt="image" src="https://user-images.githubusercontent.com/124690871/233683740-3d58ce2a-5909-40cd-abd1-8162b50f5fed.png">

Then go back one file because we want to be able to access the manage.py file. So hit ```cd ..```. 
And again run the server on the specific ip and port! 

You can try to access the server from another device and you will see the server!!
For example when I enter ```http://192.168.1.73:8000``` in google on my laptop (so not connected in any physical way to the Raspberry Pi) I will also get the message of succesfully installation!

<img width="1523" alt="image" src="https://user-images.githubusercontent.com/124690871/233686113-d757498b-edae-4284-be1a-404c21e3a7eb.png">

## Conclusion
When you came to this point, you can access with this ip and port the Django project from everywhere on your local network! So if you are connected to the same WIFI as the Raspberry is, you can access this project from every device! 

I hope you learned something!!


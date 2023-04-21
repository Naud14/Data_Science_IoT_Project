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

And when you are checking underneath your runcommand at the Raspberry Pi, you can see someone wanted your project: 
<img width="566" alt="image" src="https://user-images.githubusercontent.com/124690871/233679760-d659106a-f9b5-464e-be10-0dffd0cdf1f0.png">



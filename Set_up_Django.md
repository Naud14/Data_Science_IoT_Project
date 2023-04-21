# Set up Django project
In this tutorial we are going to set up a django project on our raspberry pi! 

First we will make sure we have all updates and installations needed for creating an django project. 
Open the terminal on your Raspberry Pi (if you are not connected to your Raspberry Pi, please walk through the first tutorial). 
Enter the following commands: 
```sudo apt upgrade```

```sudo apt install```

 ```sudo apt install python3 python3-pip```   Install python3 and pip
 
 ```sudo pip3 install django```   Install django
 
 ```mkdir djangoproject```   Make directory where we can put our project in, in this case djangoproject
 
 ``` cd djangoproject```    Move to directory of the project, in this case to djangoproject
 
 ``` sudo django-admin startproject test_app```    Make new django project named 'test_app'
 
 Use the commands ```cd``` and ```ls``` to change directory and to see whats in the directory. 

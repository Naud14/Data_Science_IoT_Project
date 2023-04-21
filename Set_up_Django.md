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
 Use ```pwd``` to see your current position (print working directory). 
 
 Go into the test_app and see whats in there. If it is good, there will be two files. 
 - First the manage.py 
 - Second the test_app file

If those two files are in there, you succesfully made a django project. For now we have to set it up so we can run the project. 
Run the command: 
```sudo python3 manage.py migrate``` For migration on the django project

If you hit ```ls``` now you can see django added a database in our project. So we are fully ready to run the project! 

For running the project we need to call this command: 
```python3 manage.py runserver```

This command wil run the django server automatically on 127.0.0.1:8000 (port 8000). 
So to see this django website, we just need to type this ip-address and portnumber in our searchmachine (for example google). 

If you did this, you should see this message: 
It means your Django project is working! And as an local host! 

![image](https://user-images.githubusercontent.com/124690871/233638539-bfd44ca5-6bc9-4b3c-bb58-1b8f05c89e7c.png)

For Django documentation click this link -> https://docs.djangoproject.com/en/4.2/ 



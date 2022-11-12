# How do you create a simple server? 

# Steps 
- create application on local computer 
- create controller that responds to web requests 
- test on localhost:8080 

# 1 - Creating Application 
For this step, you have two options, the first: using the **Micronaut Command Line Interface** (which I used) or with **Microlaunch** (which is similar to Springs initializer). 

You must specify the **--build arguement** as well as the **--lang** arguement. If not defined default build is **gradle** and default language is **java**. 

## Here's the command I used: 
![command](https://user-images.githubusercontent.com/109105989/201495738-c80fff77-d5fe-4747-94e4-c186a3e61be7.png)

## If builded properly you'll receive: 
![successCommand](https://user-images.githubusercontent.com/109105989/201495748-52b83648-ddb8-4104-91ca-d9ede5e02a71.png)

# 2 - Creating Controller 
In order to create a microserver that responds to a user's requests we need a **controller**. 

## Create Controller 
```bash 
simpleserver/src/main/java/com/hayde/SimpleContrller.java
```


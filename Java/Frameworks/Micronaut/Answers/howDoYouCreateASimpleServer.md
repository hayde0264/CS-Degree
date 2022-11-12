# How do you create a simple server? 

# Steps 
- create the application on a local computer 
- create a controller that responds to web requests 
- test on localhost:8080 

# 1 - Creating Application 
For this step, you have two options, the first: using the **Micronaut Command Line Interface** (which I used) or with **Microlaunch** (which is similar to Spring's initializer). 

You must specify the **--build argument** as well as the **--lang** argument. If not defined default build is **Gradle**, and the default language is **java**. 

## Here's the command I used: 
![command](https://user-images.githubusercontent.com/109105989/201495738-c80fff77-d5fe-4747-94e4-c186a3e61be7.png)

## If built properly you'll receive: 
![successCommand](https://user-images.githubusercontent.com/109105989/201495748-52b83648-ddb8-4104-91ca-d9ede5e02a71.png)

# 2 - Creating Controller 
In order to create a microserver that responds to a user's requests, we need a **controller**. 

## Create Controller: 
```bash 
simpleserver/src/main/java/com/hayde/SimpleContrller.java
```
## Initialize Controller: 
![initializedController md](https://user-images.githubusercontent.com/109105989/201496230-37350555-9b66-4d94-b06f-4376f1b80b36.png)

1. The annotation tells us this class is defined as a **@Controller** mapped to the path /ping 
2. The **@Get** annotation maps the **index method** to the **GET** request from /ping
3. By default, Micronaut responses uses application/JSON as **Content-Type**, but we are returning a String, **, not a JSON object**, so we set
  the media type to text/plain
4. Returns the String PONG

# 3 - Run the application 

## Command: 
![runmnApp](https://user-images.githubusercontent.com/109105989/201496482-1749199d-04b0-47fe-a67e-74e1a3eae279.png)
## If successful:  
![running](https://user-images.githubusercontent.com/109105989/201496514-8cd61b0b-4725-43fa-a8ec-26f915cbc4e3.png)
## Check localhost: 
![PONG](https://user-images.githubusercontent.com/109105989/201496530-a70f1d3b-4e87-490d-97b7-fc1433e4a87a.png)


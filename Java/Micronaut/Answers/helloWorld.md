# Hello World

# Steps: 
1. Build an application from the command line  
2. Create a controller class that, when a client requests "ping" responds with "PONG"
3. Start Server 
4. Test



# 1. 
## Build project from the command line: 
``` 
mn create-app com.example.guides --build=maven --lang=java
``` 

# 2. 
## Create Controller File: 
```bash 
cd main/java/example/micronaut
``` 

## Within Controller File (SampleController.java) add:

![Screen Shot 2022-12-10 at 7 51 08 PM](https://user-images.githubusercontent.com/109105989/206881314-2e0169fb-412f-460e-980e-8a0703da0d89.png)

- @Controller annotation maps the path /ping 
- @Get annotation maps the index method to a HTTP GET request on /ping 
- By default, Micronaut responses use JSON as Content-Type. However, I wanted to return a String, not a JSON object. 


# 3.
## Start the application on port 8080:
```bash 
./mvnw mn:run
``` 

## If successful: 

![Screen Shot 2022-12-10 at 7 56 56 PM](https://user-images.githubusercontent.com/109105989/206881438-2d8a5580-3b87-4a21-b4b1-6ff8d7752e31.png)

# 4. 
## Test with /ping 

![Screen Shot 2022-12-10 at 7 57 25 PM](https://user-images.githubusercontent.com/109105989/206881458-2eb6b217-2943-406e-82ce-5f895409dc40.png)



# References 
Amo, S. & Lopez, I. (2022). *CREATING YOUR FIRST MICRONAUT APPLICATION*. Micronaut. <https://guides.micronaut.io/latest/creating-your-first-micronaut-app-maven-java.html> 




# How do you make a simple server? 

Making a simple RESTful server using Jersey. In this instance, Jersey uses the lightweight 
**Grizzley HTTP server**. 

**project sources located in** - src/main/main 
**project tests located in** - src/test/java 

# Steps: 
1. **create maven archetype** 
2. **initialize build**
3. **make our custom POJO** 
4. **test url** 


# 1. Create archetype 
```zsh 
mvn archetype:generate -DarchetypeArtifactId=jersey-quickstart-grizzly2 \
-DarchetypeGroupId=org.glassfish.jersey.archetypes -DinteractiveMode=false \
-DgroupId=com.example.hayde -DartifactId=core -Dpackage=com.example.hayde \
-DarchetypeVersion=3.1.0
``` 
## If successful: 
![Screen Shot 2022-11-26 at 7 37 49 PM](https://user-images.githubusercontent.com/109105989/204114123-93385b0e-dab2-430f-8db2-0f27effdb3db.png)

# 2. Initialize build
```zsh 
mvn clean package // to compile and package into a WAR 
``` 

## If successful: 
![Screen Shot 2022-11-26 at 7 40 51 PM](https://user-images.githubusercontent.com/109105989/204114168-9c28c6a5-f9f6-4094-b3c1-b3a025ad6b04.png)

# 3: Make our custom POJO 
My POJO exists at: **(src/main/java/com/example/hayde/MyResource.java)** 

## Initially, the file looks like this: 
![Screen Shot 2022-11-26 at 7 47 14 PM](https://user-images.githubusercontent.com/109105989/204114269-55fa9eab-2cea-4e5c-9fe4-d35f004fee04.png)

## Let's customize: 
![Screen Shot 2022-11-26 at 7 48 52 PM](https://user-images.githubusercontent.com/109105989/204114311-0de99a28-1b3c-4c01-8cb2-a2c0750d4028.png)

## Update (src/test/java/com/example/hayde/MyResourceTest.java): 
## From: 
![Screen Shot 2022-11-26 at 7 57 23 PM](https://user-images.githubusercontent.com/109105989/204114512-1f11c9cd-0d3a-4e00-bbf1-dacdcf291202.png)
## To: 
![Screen Shot 2022-11-26 at 7 58 07 PM](https://user-images.githubusercontent.com/109105989/204114533-c8ff2d1b-ae82-45cc-b997-4a2548317856.png)

## 4: Test url 
```zsh 
mvn clean test // compiles the project and updates project unit tests 
mvn exec:java // to start server
``` 
## If successful: 
![Screen Shot 2022-11-26 at 8 01 31 PM](https://user-images.githubusercontent.com/109105989/204114595-4cbd320f-1f59-412a-bd38-a0a24881e3a7.png)

## curl http://localhost:8080/ping: 
![Screen Shot 2022-11-26 at 8 02 45 PM](https://user-images.githubusercontent.com/109105989/204114638-1e813d89-14c5-418c-82ea-f4a2393ee2e0.png)



  
# References 
Eclipse. (2022). *Jersey 3.1.0 User Guide*. <https://eclipse-ee4j.github.io/jersey.github.io/documentation/latest3x/index.html> 


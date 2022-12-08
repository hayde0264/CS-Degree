# Scheduling Tasks 

This demo will build an application that prints out the current time every five seconds using Spring's @Scheduled annotation. 

# Steps: 
1. Use the spring project initializer to build a custom ZIP file 
2. Add the *awaitility* library to pom.xml 
3. Create a scheduled task (src/main/java/com/exmaple/scheduilingtask/ScheduledTasks.java) 
4. Enable scheduling (src/main/java/com/example/schedullingtask/SchedulingTaskApplication.java) 
5. Clean package & Test

# 1. 
Navigate to <https://start.spring.io> and choose the dependencies you'll need for the application; this will generate 
a ZIP file with the archive of the web application. 

## 
![Screen Shot 2022-12-08 at 4 17 01 PM](https://user-images.githubusercontent.com/109105989/206569287-20278bb9-0585-450e-9eee-a9d8de039a3d.png)

## Generate and Unzip 
![Screen Shot 2022-12-08 at 4 17 55 PM](https://user-images.githubusercontent.com/109105989/206569397-855baf66-1287-4016-843d-cd46aa8d3ab2.png)

## Add to project 
![Screen Shot 2022-12-08 at 4 19 11 PM](https://user-images.githubusercontent.com/109105989/206569602-bb997650-ec38-41b9-9f2c-de27708e2e8e.png)

# 2. 

## Add awaitility library to pom.xml 
![Screen Shot 2022-12-08 at 4 21 27 PM](https://user-images.githubusercontent.com/109105989/206570165-6940989e-c2fc-4dc2-9b0c-d9ae92aeb39b.png)

## Use command: 
```bash 
mvn package 
``` 

# 3. 

## Create ScheduledTask.java

![Screen Shot 2022-12-08 at 4 29 12 PM](https://user-images.githubusercontent.com/109105989/206571347-6ce54424-c1f9-434b-bef2-f1ffc5c0eb2a.png)


# 4. 

## Enable Scheduling in SchedulingTaskApplication.java 
![Screen Shot 2022-12-08 at 4 31 10 PM](https://user-images.githubusercontent.com/109105989/206571833-b9cfe049-92e9-462b-a534-1a39b69c7c21.png)

# 5. 
## Clean package 
```bash 
mvn clean
``` 

## Test
```bash 
./mvnw spring-boot:run
``` 

## If successful: 
![Screen Shot 2022-12-08 at 4 37 41 PM](https://user-images.githubusercontent.com/109105989/206572940-2448e8e6-6c99-4134-b4a5-29d8f01690e2.png)


# References 
spring. (2022). *Scheduling Tasks*. VMware Tanzu. <https://spring.io/guides/gs/scheduling-tasks/> 

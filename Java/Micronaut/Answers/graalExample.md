# Graal example 


```xml 



```java 

  package example.micronaut;
  
  
  import io.micronaut.serde.annotation.Serdeable;
  
  
  @Serdeable
  public class Conference {
          private final String name;
  
          public Conference(String name) {
                  this.name = name;
          }
  
          public String getName() {
                  return name;
          }
  }
``` 

```java 


  package example.micronaut;
  
  import jakarta.inject.Singleton;
  import java.util.Arrays;
  import java.util.List;
  import java.util.Random;
  
  
  @Singleton
  public class ConferenceService {
          private static final List<Conference> CONFERENCES = Arrays.asList(
                          new Conference("Greach"),
                          new Conference("GR8Conf EU"),
                          new Conference("Micronaut Summit"),
                          new Conference("Devoxx Belguim"),
                          new Conference("Oracle Code One")
                          );
          public Conference randomConf() {
                  return CONFERENCES.get(new Random().nextInt(CONFERENCES.size()  ));
          }
  }
``` 

```java
  package example.micronaut;
  
  
  import io.micronaut.http.annotation.Controller;
  import io.micronaut.http.annotation.Get;
  
  
  
  @Controller("/conferences")
  public class ConferenceController {
          private final ConferenceService conferenceService;
  
          public ConferenceController(ConferenceService conferenceService) {
                  this.conferenceService = conferenceService;
          }
  
          @Get("/random")
          public Conference randomConf() {
                  return conferenceService.randomConf();
          }
  }
``` 


# What is the compile plugin? 

The compile plugin allows you to compile your sources, which tell Maven **which lifecycle(s) to execute**. 

**compiler:compile** - is bound to the compile phase with the main source files 
**compiler:testCompile** - is bound to the test-compile phase with the test source files 

## Use cases: 
- **compile using a different JDK** 
- **compile using -source and -target javac Options** 
- **compile using the --release javac option** 
- **compile using memory allocation enhancement** 
- **passing compiler arguments**



## Before: 
```zsh 
mvn compile 
mvn testCompile 
```


## After: 
<img width="565" alt="Screen Shot 2022-11-26 at 12 23 39 AM" src="https://user-images.githubusercontent.com/109105989/204073631-983abdf0-da15-4426-b923-e85a26a4b414.png">
## 

  
# References 
Apache. (2022). *Available Plugins*. <https://maven.apache.org/plugins/index.htmll>

What is the deploy plugin? 

The deploy plugin lets you add **artifact(s) to remove repositories for sharing with other developers**. 

**deploy:deploy** - will automatically install artifacts and poms  
**deploy:deploy-file** - will install a single article and its pom 

## Using this plugin requries: 
- **information about the repository** 
- **information bout the artifact(s)** 
- **a deployer** 


## Usage: 
```zsh 
mvn deploy 
mvn deploy-file
``` 

  
# References 
Apache. (2022). *Available Plugins*. <https://maven.apache.org/plugins/index.htmll>



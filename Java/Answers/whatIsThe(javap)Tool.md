# What is the javap command? 

The javap command will **disassemble one or more java class files**. What's returned depends on the options used. 
For example, when **no** options are used, the command **prints the protected and public fields, and the methods of the included 
classes**. 

## Options include: 
- **help, --help, or -?** - prints a help message for the javap command 
- **-version** - prints release information 
- **-verbose or -v** - prints additional information about the selected class 
- **-l** - prints the line and local variable types 
- **-public** - shows only public classes and members 
- **-protected** - shows only protected and public classes and members 
- **-package** - shows package, protected, public classes, and members (default) 
- **-private or -p** - shows all classes and members 
- **-c** - prints disassembled code, for example, Java bytecodes 
- **-s** - prints internal type signatures 
- **-sysinfo** - shows system information such as path, size, date, MD5 (of the specified class) 
- **-constants** - shows static final constants 
- **--module module or -m module** - specifies the module containing classes to be disassembled 
- **--module0path path** - specifies where to find application modules 
- **--system jdk** - specifies where to find system modules 
- **--class-path path, -classpath, or -cp path** - specifies the path that the javap command uses to find user class files 
- **-bootclasspath path** - overrides the local boostrap class files 
- **-Joption** - passes the specified option to the JVM 


  


# References 
Learn Java. (2022). *Oracle*. <https://dev.java/learn> 


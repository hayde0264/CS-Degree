# What is the javadoc tool? 

The javadoc tools will **parse and declare** documentation comments within java files. Javadoc will produce 
a corresponding HTML page(s) that will **describe the public and protected classes, nested classes, interfaces, constructors, 
methods, and fields**. 

## Options include: 
- **-breakiterator** - which computes the first sentence with BreakIterator (the first sentence is copied to the package, class, or member summary) 
- **-doclet class** - generates output by using an alternate doclet. 
- **-docletpath path** - specifies where to find doclet class files
- **-exclude pkglist** - will exclude specified packages, as well as their subpackges using the **-subpackages** option 
- **--expand-requires value** - instructs the javadoc tool to expand the set of modules to be documented 
- **-help or --help** - displays the online help, which lists all of the javadoc and doclet command-line options 
- **--help-extra or -x** - prints a synopsis of non-standard options and exits 
- **-Jflag** - passes flag directly into the (JRE) that runs the javadoc tool
- **-version** - will report the verison of the (JRE) being used to run the javadoc tool 
- **-locale name** - specifies the locale that the javadoc tool uses when it generates documentation 
- **-package** - shows only package, protected, and public classes and members 
- **-private** - shows all classes and members 
- **-protected** - shows only protected and public classes and members (default) 
- **-quiet** - shuts off messages so that only the warnings and errors appear to make them easier to view 
- **--show-members value** - specifies which fields and methods are documented
- **--show-types value** - specifies which types are documented 
- **-subpackages subpkdlist** - generates documentation from sources files in the specified packages and recursively in their subpackages 
- **-verbose** - provides detailed messages while the javadoc tool runs 
- **--version** - prints javadoc version information 



# References 
Learn Java. (2022). *Oracle*. <https://dev.java/learn> 


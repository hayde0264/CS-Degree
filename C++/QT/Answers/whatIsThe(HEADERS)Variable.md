# What is the HEADERS variable? 

The HEADERS variable is where the developer can notify qmake of the header files for the project. Qmake will detect if moc is required by the classes within the headers and then will add the appropriate dependencies. 

## For example: 
```bash 
HEADERS = someclass.h \
          anotherclass.h \
          somewindow.h
``` 

# References 
Qt. (2022). *Creating Project Files | qmake Manual*. <https://doc.qt.io/qt-6/qmake-project-files.html> 

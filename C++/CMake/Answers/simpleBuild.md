# Building a basic project 


The simplest CMake project can be built with a single CMakeList.txt file with only **three commands**. 

## The commands are: 
- **cmake_minimum_required()** - which explains versioning 
- **project()** - which sets the name of the project 
- **add_executable()** - which tells CMake to create an executable using a specified file 


## Steps: 
1. Create a project directory 
2. Create a CMakeList.txt file with three commands 
3. Create an execuable file 
4. Make the project 
5. Build the project 

# 1.
## Create directory 
```bash
mkdir test 
``` 

# 2. 
## Create a CMakeList.txt file with three commands 
```bash 
cd test 
vim CMakeList.txt 
``` 
## For instance: 
<img width="515" alt="Screen Shot 2022-12-15 at 12 12 12 AM" src="https://user-images.githubusercontent.com/109105989/207777847-2233c92f-7832-481a-a69e-908ba595ab2f.png">

# 3. 
## Create an executable output file (which was identified in the CMakeList.txt)
```bash 
vim test.cxx 
``` 
# 4. 
## Before: 
<img width="438" alt="Screen Shot 2022-12-15 at 12 13 35 AM" src="https://user-images.githubusercontent.com/109105989/207778031-25cb64d1-9740-4369-9006-fb34c3501cfc.png">

## Use cmake .. /(dir) 
```bash 
cmake ../test 
``` 

## After: 
<img width="572" alt="Screen Shot 2022-12-15 at 12 16 01 AM" src="https://user-images.githubusercontent.com/109105989/207778323-d83e1531-1e4c-40af-9ffc-049760d0c600.png">

# 5. 
## Build with cmake --build . 
```bash 
cmake --build . 
``` 


# References 
CMake. (2022). *Step 1: A Basic Starting Point*. <https://cmake.org/cmake/help/latest/guide/tutorial/A%20Basic%20Starting%20Point.html#exercise-1-building-a-basic-project>






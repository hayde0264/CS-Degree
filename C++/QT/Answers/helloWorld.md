# Hello, world. 

## Steps 
1. Create a directory *test* and add test.cpp 
2. Use qmake to set up a new QT project 
3. Add widgets to (.pro) file 
4. Generate a makefile with (-makefile) 
5. Make the app with (make) 
6. Open (.app) 


# 1. 

## Create text directory 
```bash 
mkdir /Users/hayde/Desktop/Code/c++/test 
```
## Add test.cpp 
```bash 
vim test.cpp 

```
```cpp 
  #include <qapplication.h>
  #include <qpushbutton.h>
  
  int main(int argc, char** argv) {
          QApplication app(argc, argv);
  
          QPushButton hello("Hello, world.", 0);
          hello.resize(100, 30);
          hello.show();
  
          return app.exec();
  }
  ```
  
# 2. 
  ```bash 
  qmake -project -o test.pro 
  ```
  
  ## After command 
  <img width="484" alt="Screen Shot 2022-12-06 at 9 56 50 PM" src="https://user-images.githubusercontent.com/109105989/206076954-23fc74fc-6672-42ee-a72a-1b3b2a64a1b5.png">
  
  ## Inside of test.pro 
  <img width="568" alt="Screen Shot 2022-12-06 at 9 57 52 PM" src="https://user-images.githubusercontent.com/109105989/206077105-2b4bdc13-1b58-4728-84bc-243dbf63444c.png">

# 3. 

## Add qt += WIDGETS 
  <img width="568" alt="Screen Shot 2022-12-06 at 9 59 35 PM" src="https://user-images.githubusercontent.com/109105989/206077455-0bbe1393-3306-4cb5-bbb0-31b807398ab4.png">

# 4. 
```bash 
qmake -makefile 
```
## Before 
<img width="462" alt="Screen Shot 2022-12-06 at 10 01 35 PM" src="https://user-images.githubusercontent.com/109105989/206077623-b2e2ae4e-2dc1-4209-b1bf-2af2fa1bf69c.png">

## After 
<img width="491" alt="Screen Shot 2022-12-06 at 10 02 19 PM" src="https://user-images.githubusercontent.com/109105989/206077780-dd6b2dd7-176e-41e1-97d3-06771e1b403a.png">


# 5. 
```bash 
make 
```
## If done properly 
<img width="569" alt="Screen Shot 2022-12-06 at 10 04 05 PM" src="https://user-images.githubusercontent.com/109105989/206077978-745310cf-74aa-417f-89fc-26b187691c01.png">

## Creates a binary file (test.o) && (test.app) 
<img width="563" alt="Screen Shot 2022-12-06 at 10 05 59 PM" src="https://user-images.githubusercontent.com/109105989/206078341-3583ae4a-4a42-41d5-a64e-0c0cfd347be6.png">

# 6. 
```bash 
open test.app
```
## Result 

<img width="1440" alt="Screen Shot 2022-12-06 at 10 08 47 PM" src="https://user-images.githubusercontent.com/109105989/206078741-05c570b4-51f4-4e92-bc8c-fb6faa9dc4b7.png">

# References 
Larsen, C. (2016, May 6). *Building Qt apps on the command line*. <https://csl.name/post/qt-gcc/> 

  
  

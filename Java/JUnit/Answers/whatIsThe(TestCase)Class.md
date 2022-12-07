# What is the TestCase class? 


## Methods included: 
```bash 
String getName() // returns the name of a test case 
void setName(String) // sets the name of a test case by String 
TestResult run() // convenience method to run test cases and report to TestResult 
void runTest() // allows you to override a testing method if you don't want a method to be invoked by reflection 
void setUp() // override that allows you to create objects against which to test 
void tearDown() // override to dispose of objects no longer needed once a test has finished 
```



# References 
Beck, K. (2003, September 23). *JUnit Pocket Guide*. O'Reilly Media. <https://www.amazon.com/JUnit-Pocket-Guide-Look-up-Advice-ebook/dp/B002QX43Z2/ref=sr_1_15?crid=2CZMB5XJF1GXM&keywords=junit&qid=1670452993&sprefix=junit+%2Caps%2C83&sr=8-15> 

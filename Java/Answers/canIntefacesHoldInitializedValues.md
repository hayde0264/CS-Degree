# Can Interfaces hold initialized values? 

Since any fields placed within an interface are automatically **static and final**, you can use the interface as a tool for **creating groups of constant values**. 

## For instance: 
```java 
    public class InitializingInterfaces {
      private static void printMonth(String month) {
        System.out.println("We're in month " + month + ".");
      }
  
       public static void main(String[] args) {
          printMonth(MonthsAsString.JANUARY); // Prints - We're in month January.
          printMonth(MonthsAsString.FEBUARY); // Prints - We're in month February.
          printMonth(MonthsAsString.MARCH); // Prints - We're in month March.
          printMonth(MonthsAsString.APRIL); // Prints - We're in month April.
          printMonth(MonthsAsString.MAY); // Prints - We're in month May.
          printMonth(MonthsAsString.JUNE); // Prints - We're in month June.
          printMonth(MonthsAsString.JULY); // Prints - We're in month July.
          printMonth(MonthsAsString.AUGUST); // Prints - We're in month August.
          printMonth(MonthsAsString.SEPTEMBER); // Prints - We're in month September.
          printMonth(MonthsAsString.NOVEMBER); // Prints - We're in month Novemeber.
          printMonth(MonthsAsString.DECEMBER); // Prints - We're in month December.
        }
      }
  
    interface MonthsAsString {
      String
        JANUARY = "January",
        FEBUARY = "February",
        MARCH = "March",
        APRIL = "April",
        MAY = "May",
        JUNE = "June",
        JULY = "July",
        AUGUST = "August",
        SEPTEMBER = "September",
        OCTOBER = "October",
        NOVEMBER = "Novemeber",
        DECEMBER = "December";
    }
  ``` 
  
  
# References 
Eckel, B. (2006, February 10). *Thinking in Java* (4th ed.). Pearson. <https://www.amazon.com/Thinking-Java-4th-Bruce-Eckel/dp/0131872486/ref=sr_1_1?crid=23ZTC7TRPPHR1&keywords=thinking+in+java&qid=1667521991&qu=eyJxc2MiOiIxLjg0IiwicXNhIjoiMC45NiIsInFzcCI6IjEuMTUifQ%3D%3D&sprefix=thinking+in+java%2Caps%2C87&sr=8-1>

 
  

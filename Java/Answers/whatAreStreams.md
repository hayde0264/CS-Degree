# What are streams? 

**streams** - are a Java API which lets you manipulate collections of data in a **declarative manner**. Streams can be processed 
in parallel **transparently**, without having to write multithreaded code. 

## Before:
```java 
List<Stats> lowBattingAverage = new ArrayList<>(); 
for (Stats avg: stats) 
    if (avg.getAverage() < 250) { 
        lowBattingAverage.add(avg);
    } 
} 

Collections.sort(lowBattingAverage, new Comparator<Stats>() { 
    public int compare(Stats s1, Stats s2) { 
        return Integer.compare(s1.getAverage(), s2.getAverage()); 
    } 
}); 

List<String> lowBattingAveragePlayer = new ArrayList<>(); 
for (Stats s : lowBattingAverage) { 
    lowBattingAveragePlayer.add(s.getPlayer()); 
}
``` 

## After: 
```java 
import static java.util.Comparator.comparing; 
import static java.util.stream.Collectors.toList; 

List<String> lowBattingAveragePlayer = stats.stream()
                                            .filter(d -> d.getAverage() < 250) 
                                            .sorted(comparing(Stats::getAverage)) 
                                            .map(Stats::getPlayer) 
                                            .collect(toList()); 
``` 
## 
This code is written in a **declarative way** because I specified what I wanted to receive (filtered players with low batting averages) rather than 
specifying **how to implement the operation** (avoiding control-flow). 



# References 
Fusco, M., Mycroft, A., Urma, R.G. (2014, September 2). *Java 8 in Action: Lambdas, Streams, and functional-style programming* (1st ed.). Manning Publications. <https://www.amazon.com/Java-Action-Lambdas-functional-style-programming/dp/1617291994/ref=sr_1_1?crid=3HQU2KUN42FRP&keywords=java+8+in+action&qid=1669665829&sprefix=java+8+in+action%2Caps%2C85&sr=8-1> 



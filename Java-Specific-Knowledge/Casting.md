# Casting

Casting is an operation that allows us
to **change the type of a value**.

``` java 
public class Casting {


    public static void main(String[] args) {
        double d1 = 3.2;
        double d2 = 3.999999;
        int i1 = (int) d1;                      // 1
        int i2 = (int) d2;                      // 2
        double d3 = (double) i2;                // 3

    }

}
``` 
1. i1 has value 3
2. i2 has value 3
3. d3 has value 3.0

# Implemement an algorithm to determine if a string has all unique characters. 

**Time**: O(n) where n == length of string. 
**Space**: O(1) since the for loop will never iterate throuugh more than the 128 elements.

1. Figure out if the string is a ASCII string or a Unicode string. 
2. Immediately return false if the string length exceeds the number of unique characters in the alapabet (128-character alphabet). 
2. Create an array of boolean values. 
3. Within the array, create a variable *i* which will indicate wheather the character *i* is contained in the string. 
4. The second time you come access this character you immediately return false. 

## Java 
``` java 
public class IsUnique {
    boolean isUniqueChar(String str) {
        if (str.length() > 128) return false;

        boolean[] char_set = new boolean[128];
        for (int i = 0; i < str.length(); i++) {
            int val = str.charAt(i);
            if (char_set[val]) {
                return false;
            }
            char_set[val] = true;
        }
        return true;
    }
}
``` 

# References 
McDowell, G. (2015). *CRACKING the CODING INTERVIEW*. Career Cup. <https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/0984782850/ref=sr_1_1?crid=2THGTI447EPQ4&keywords=cracking+the+coding+interview&qid=1665794466&qu=eyJxc2MiOiIxLjQ0IiwicXNhIjoiMC42MSIsInFzcCI6IjAuNTAifQ%3D%3D&sprefix=cracking+the+coding+interview%2Caps%2C84&sr=8-1>

# What is an interface? 

An interface is a **collection of method declarations**, but these declarations contain **no data and no bodies**. Which means interfaces contain only **method signatures**. Interfaces require implementing classes **to implement all of the methods declared within the interface**. 

## Implementing Single Interfaces: 
```java 
  
  interface Sellable { // interface for objects that can be sold
                       
    public String itemDescription(); // decription of an item
                                     
    public int itemPrice(); // retail price
                                     
    public int salePrice(); // sale price
  }
  
   
  class Shirt implements Sellable {
    
    private String description;    
    private String size;
    private int price; 
                  
    public Shirt(String decription, String size, int price) {        
        this.description = decription;              
        this.size = size;                           
        this.price = price;
    }   
    
    public String itemDescription() { return description; } // notice interface implementation
    public int itemPrice() { return price; } // notice interface implementation
    public int salePrice() { return price / 2; } // notice interface implementation
    public String shirtSize() { return size; }
  } 
``` 
## Implementing Multiple Interfaces: 
```java 
  
  interface Sellable { // interface for objects that can be sold
  
    public String itemDescription(); // decription of an item
  
    public int itemPrice(); // retail price
  
    public int salePrice(); // sale price
  }
  
  interface Transportable { // Interface for objects that can be sold
  
    public int weightOfItem(); // item weight
  
    public boolean isHazardous(); // is item hazardous
  
  }
  
  interface Insurable extends Transportable, Sellable {
  
    public double insureBox();
  
  }
  
  
  class Shirt implements Sellable {
  
    private String description;
    private String size;
    private int price;
  
    public Shirt(String decription, String size, int price) {
        this.description = decription;
        this.size = size;
        this.price = price;
    }
  
    public String itemDescription() { return description; } // notice interface implementation
    public int itemPrice() { return price; } // notice interface implementation
    public int salePrice() { return price / 2; } // notice interface implementation
    public String shirtSize() { return size; }
  }
  
  class ShipItem implements Sellable, Transportable {
    // declarations that will be included in interface arguements
    private String decription;
    private int price;
    private int weight;
    private boolean hazardous;
  
// ship item specific declarations
⚠   private int height;
⚠   private int width;
⚠   private int depth;
  
    public ShipItem(String decription, int price, int weight, boolean hazardous) { // Constructor for interace methods
      this.decription = decription;
      this.price = price;
      this.weight = weight;
      this.hazardous = hazardous;
    }
  
    public ShipItem(int height, int weight, int depth) { // Constructor for ShipItem object
      this.height = 0;
      this.weight = 0;
      this.depth = 0;
    }
  
    public String itemDescription() { return decription; } // notice interface implementation of Sellable
    public int itemPrice() { return price; } // notice interface implementation of Sellable
    public int salePrice() { return price / 2; } // notice interface implementation of Sellabled
  
  
    public int  weightOfItem() { return weight; } // notice interface implementation of Transportable
    public boolean isHazardous() { return hazardous; } // notice interface implementation of Transportable
  
    public double insureBox() { return price * 1.4; } // notice interface implementation of Insurable
  
    public void setBox(int height, int width, int depth) {
      this.height = height;
      this.width = width;
      this.depth = depth;
    }
  }
``` 

# References 
Goodrich, M. Tamassia, R. (1994, January 1). *Data Structures and Algorithms in Java* (4th ed.). Wiley, John & Sons, Incorporated. <https://www.amazon.com/Michael-T-Goodrich-Structures-Algorithms/dp/B008UYJYF0/ref=sr_1_1?crid=1OJL9289EWZ94&keywords=data+structures+and+algorithms+in+java+4th+edition&qid=1667519269&qu=eyJxc2MiOiIwLjAwIiwicXNhIjoiMC4wMCIsInFzcCI6IjAuMDAifQ%3D%3D&sprefix=data+structures+and+algorithms+in+java+4th+edition%2Caps%2C83&sr=8-1> 



# Attributes 

All HTML elements can have **attributes**. 

**attributes** - pro ide additional information about elements. They are always specified in the **start tag**, and they usually come in **name/value pairs** like name="value." 

# The href Attribute 
The **<a>** tag defines a **hyperlink**. The **href** attribute within the **<a>** tag specifies the **URL link**. 

## For instance: 
``` html 
<a href="https://www.google.com">Visit Google</a> 
``` 

![href](https://user-images.githubusercontent.com/109105989/197936169-63ecb29e-f167-4a9a-a9db-01f8a98137b6.png)

  
# The src Attribute 
The **<img>** tag is used to **embed an image in an HTML page**. The **src** attribute **specifies the path to the image that will be displayed**. 

## For instance: 
``` html 
<img src="jungle.png"> 
``` 
  ![jungle](https://user-images.githubusercontent.com/109105989/197936553-7688cbbf-4442-4b3b-964a-07622d1ea7a1.png)
  
# The width and height Attributes 
The **<img>** tag should also contain the **width** and **height** attributes. The width and the height of an image are measured in **pixels**. 

## Example: 
``` html 
<img src="jungle.png" width="300" height="600"> 
``` 
<img src="jungle.png" width="300" height="600"> 

# The style Attribute 
The **style** attribute is used to add styles to elements (colors, fonts, sizes, and more). 

## Make a paragraph blue: 
```html 
<p style="color:blue;">This is a blue paragraph.</p> 
``` 

# The lang Attribute 
The **lang** attribute declares the language of the webpage, and this **should always be included**. The lang attribute assists **search engines and browsers**. 

## For example, this specifies using the English language: 
```html 
<!DOCTYPE html> 
<html lang="en"> 
<body> 
... 
</body> 
</html> 
``` 

# The title Attribute 
The **title** attribute defines extra information about an element. The value of the tile attributes is displayed when you hover over an element. 

## For example: 
```html 
<p title="This is a tooltip">Within a paragraph.</p> 
``` 

# Good practices
- always use **lowercase** attributes 
- always **quote** attribute values 
- stick with **double-quotes** rather than single 


# References  
HTML Tutorial. (2022). *W3 Schools*. <https://www.w3schools.com/html> 

# JavaScript
## Object Literals
### Syntax:

``` JavaScript
var = objectName = {
    // properties:
    key: value,
    key: value,
    // methods:
    method: function;
}
```

### To access elements in an object:

``` JavaScript
var varName = objectName.key;
var varName = objectName.method();
var varName = objectName['key'];
```

---
## Document Object Models (DOM)
![DOM](Images/pic_htmltree.gif)
### DOM:
Is the way that JavaScript reads HTML files, it creates a tree of objects by the tag and the class and id attributes.

The DOM lets JavaScript access and update HTML and CSS content in order to create dynamic HTML.

``` JavaScript
var = getElementById('id');
getElementByClassName('class');
getElementByTagName('HTML tag name');
querySelectorAll('CSS selector');
getAttribute();
hasAttribute();
setAttribute();
removeAttribute();

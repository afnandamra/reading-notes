## HTML
### Chapter 2
* **Text**
    * You can style the text by these tags:
        * Structural markup:
            * __Bold__ `<b>Bold Text goes here.</b> `
            * _Italics_ `<i>Italics Text goes here.</i> `
            * <sup>Superscript</sup>
            `<sup>Super text goes here.</sup>`
            * <sub>Subscript</sub> 
            `<sub>Sub text goes here.</sub>`
            * Line break ` <br /> `
            * Horizontal rule ` <hr />`
        * Semantic markup:
            * __Bold__ `<strong>Bold Text goes here.</strong> `
            * _Italics_ `<em>Italics Text goes here.</em> `
            * "Quotations"
                * `<blockquote>Longer quotes go here</blockquote>`
                * ` <q>Shorter (inline) quotes go here</q> `
            * Abbreviations <abbr title="Architect">Arch.</abbr> ` <abbr title="Architect">Arch.</abbr> `
            * Acronyms <acronym title="Abdul Aziz Al Ghurair School of Advanced Computing">ASAC</acronym> ` <acronym title="Abdul Aziz Al Ghurair School of Advanced Computing">ASAC</acronym> `
            * Citations ` <cite>Reference</cite>`
            * Definitions ` <dfn>terminology</dfn>`
            * Author Details `<address>contact details</address>`
            * Insert `<ins>New information</ins>`
            * Delete `<del>Old information</del>`
            * Strikethrough `<s>strikethrough</s>`

---
## CSS
### Chapter 10
#### What is CSS and why we use it?
CSS adds style to the webpage to make it more attractive, it can add new elements to the page (Boxes, borders, or images ...etc), modify existed elements (font, color, or size ...etc), or style certain elements (lists, tables, and forms).

#### How to use CSS?
``` CSS
    p {
    font-family: Arial;} 
```
This indicates that all `<p>` elements should appear in Arial typeface.
* `<p>` : Selectors, indicates which element the rule applies to.
* `font-family: Arial;` : Declarations, indicate how selector elements should be styled.

example:
``` CSS
h1, h2, h3 {
    font-family: Arial;
    color: yellow;}
```
This will change the font and the color to all h1, h2, h3 headings.

#### How to add CSS to HTML?
* #### External CSS File:

``` HTML
<link href="css relative path" type="text/css" rel="stylesheet" />
```
* #### Internal CSS:

``` HTML
<style type="text/css">
css code goes here
</style>
```

----

## JavaScript
### Chapter 2
### Basics
#### How JS makes web pages more interactive?

* **A script** is a series of instructions that the computer can follow in order to achieve a goal.
    * to write a script, you first need to have a goal to achieve, and steps to follow, after that you can start writing your script.
* **An expression** is a result of a single value, which can be assigned or returned using operators (+, -, /, *, ++, --, %).
* **A function** is a way for you to reuse a set of statements or a script you assign to a function.
    * Declaring a function:
        ``` JavaScript
            function functionName() {
            function code;
            }
        ```
    * Calling a function:
        ``` JavaScript
            functionName();
        ```
    * If a function needs or has information, it goes between the brackets ().

----
## JavaScript
### Chapter 4
### Decisions and Loops:

#### Comparison Operators:
* == : equal to (same value).
* != : not equal to.
* === : strict equal (same data type and value).
* !== : strict not equal to.
* \> : greater than.
* < : less than.
* \>= : Greater than or equal to.
* <= : less than or equal to.

#### Logical Operators:
* && : logical and.
* \|\| : logical or.
* ! : logical not.

#### If statements:
``` JavaScript
if (condition1){
    run if condition1 is true
} else if (condition2){
    run if condition2 is true
} else {
    run if all conditions are false
}
```

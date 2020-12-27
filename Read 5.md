# CSS
## What is CSS and why we use it?
CSS adds style to the webpage to make it more attractive, it can add new elements to the page (Boxes, boarders, or images ...etc), modify existed elements (font, color, or size ...etc), or style certain elements (lists, tables, and forms).

## How to use CSS?
``` CSS
    p {
    font-family: Arial;} 
```
This indicades that all \<p> elements should appear in Arial typeface.
* `<p>` : Selectors, indicates which element the rule applies to.
* `font-family: Arial;` : Declarations, indicate how selector elements should be styled.

example:
``` CSS
h1, h2, h3 {
    font-family: Arial;
    color: yellow;}
```
This will change the font and the color to all h1, h2, h3 headings.

### How to add CSS to HTML?
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
---
## Color
* Foreground color
* Background color

You can add color in CSS in three different ways:
* RGB values: rgb(100,100,90)
* HEX code: #ee3e80
* Color names: Green
* HSL: Hue (angle between 0 and 360) Saturation (percentage) Lightness (percentage) : hsl(0,100%,54%)

### Opacity
Can be added using the opacity property `opacity: 0.5;` or added to the RGB color `rgba(100,100,90,0.5);` or added to the HSL color `hsla(30,100%,50%,0.5);`
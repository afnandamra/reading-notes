# Domain Modeling
* **Domain model:** is the process of creating a conceptual model in code for a specific problem. And a domain model that's articulated well can verify and validate your understanding of that problem.
* **A model describes:**
    * the various entities
    * their attributes and behaviors
    * the constraints that govern the problem domain
* **object-oriented model:** An entity that stores data in properties and encapsulates behaviors in methods. 
* Here's some tips to follow when building your own domain models.
    1. When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
    2. Model its attributes with a constructor function that defines and initializes properties.
    3. Model its behaviors with small methods that focus on doing one job well.
    4. Create instances using the new keyword followed by a call to a constructor function.
    5. Store the newly created object in a variable so you can access its properties and methods from outside.
    6. Use the this variable within methods so you can access the object's properties and methods from inside.

----
# HTML
## Tables
* **syntax:**

```html
<table>
   <thead>
      <tr>
         <th></th>
         <th scope="col">1st col head</th>
         <th scope="col">2nd col head</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <th scope="row">row head</th>
            <td>cell</td>
            <td>cell</td>
         </tr>
         <tr>
            <th scope="row">row head</th>
            <td>cell</td>
            <td>cell</td>
         </tr>
   </tbody>
   <tfoot>
      <tr>
         <td></td>
         <td colspan="2">merged cell</td>
      </tr>
   </tfoot>
   </table>
```

----
# JavaScript
## Functions, Methods, and Objects

``` js
var = objectName = {
    // properties:
    key: value,
    key: value,
    // methods:
    method: function;
}
```
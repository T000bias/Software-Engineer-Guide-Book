# CSS Reference Sheet

# Content
- [CSS Reference Sheet](#css-reference-sheet)
- [Content](#content)
  - [Media Queries](#media-queries)
  - [Flexbox](#flexbox)
  - [CSS Selectors](#css-selectors)
  - [Type Selector](#type-selector)
  - [ID Selector](#id-selector)
  - [Descendant Selector](#descendant-selector)
  - [Combined Selectors](#combined-selectors)
  - [Class Selector](#class-selector)
  - [Comma Combinator](#comma-combinator)
  - [The Universal Selector](#the-universal-selector)
  - [Adjacent Sibling Selector](#adjacent-sibling-selector)
  - [General Sibling Selector](#general-sibling-selector)
  - [Child Selector](#child-selector)
  - [First Child Pseudo-selector](#first-child-pseudo-selector)
  - [Only Child Pseudo-Selector](#only-child-pseudo-selector)
  - [Last Child Pseudo-Selector](#last-child-pseudo-selector)
  - [Nth child  Pseudo-Selector](#nth-child--pseudo-selector)
  - [Nth Last Child Pseudo-Selector](#nth-last-child-pseudo-selector)
  - [First of Type Selector](#first-of-type-selector)
  - [Nth of Type Selector](#nth-of-type-selector)
  - [Only of Type Selector](#only-of-type-selector)
  - [Last of Type Selector](#last-of-type-selector)
  - [Empty Selector](#empty-selector)
  - [Negation Pseudo-class](#negation-pseudo-class)
  - [Attribute Selector](#attribute-selector)
  - [Attribute Value Selector](#attribute-value-selector)
  - [Attribute Starts with Selector](#attribute-starts-with-selector)
  - [Attribute Ends with Selector](#attribute-ends-with-selector)
  - [Attribute Wildcard Selector](#attribute-wildcard-selector)

## Media Queries
## Flexbox
## CSS Selectors
## Type Selector 

Selects elements by their type of tag.

```css
/* Syntax */
tagName {
    width:50px;
}

/*Examples*/
div {
    height:30px
}

```
## ID Selector

Selects elements with an id.
```css
/* Syntax */
#idname {

}

/* Examples */
/* <h2 id="idName"> */
#idName {
    width:500px;
}
```
## Descendant Selector

The element inside of another element will be selected.

```css
selectedElement targetElemenet {
    /*  */
}

```
## Combined Selectors

You can combine any selector with the descendent selector

```css
    /* Selects all <span> elements that are inside of elements with id="cool" */
    #cool span {
        width: 50px;
    }

    /* You can combine the class selector with other selectors, like the type selector */


    /* Examples */

    ul.important {
        /* Selects all <ul> elements that have class="important" */
    }

    #big.wide {
        /* Selects all elements with id="big" that also have class="wide" */
    }
```
## Class Selector

Selects elements by their class attribute.

```css
    /* Selects all elements with the attribute class="className" */
    .className {
        property: value;
    }
```
## Comma Combinator

You can combine selectors with commas.

```css

    A,B {
        /* This selects all A and B elements. You can combine any selectors this way, and you can specify more than two */
    }


```
## The Universal Selector

The universal selector (*) can selects every element in your document

```css
    /* Syntax */

    * {
        /* You can select all elements with this selector. */
    }

    /* Examples */

    p * {
    
    /* Selects any elements inside all <p> elements. */
    }

    ul.fancy * {
    /* Selects every element inside all 
    <ul class="fancy"> elements. */
    }
```
## Adjacent Sibling Selector

Selects an element that directly follows another element. 

Elements that follow one another are called siblings. They're on the same level, or depth.

```css

    A + B {
        /* This selects all B elements that directly follow A. */
    }

    p + .intro {
    /* Selects every element with class="intro" that directly follows a <p>. */
    }
```
## General Sibling Selector

Select elements that follows another element. This gets all of the following elements instead of one like adjacent selector.

```css

    A ~ B {
        /* You can select all siblings of an element that follow it */
    }
```
## Child Selector

Select direct children of an element.

```css
    /* Syntax */
    A > B {
        /* Selects all B that are a direct children A */
    }
```
## First Child Pseudo-selector

Selects the first child element inside of another element.

```css
selector:first-child {
    /* You can select the first child element. A child element is any element that is directly nested in another element */
}

/* Examples */

p:first-child {
    /* Selects all first child <p> elements */
}

div p:first-child{
    /* selects all first child <p> elements that are in a <div> */
}
```
## Only Child Pseudo-Selector

Selects an element that is the only element inside of another one

```css
/* Syntax */

selector:only-child {
    /* You can select any element that is the only element inside of another one */
}

/* Examples */
span:only-child {
    /* Selects the <span> elements that are the only child of some other element. */
}

ul li:only-child {
    /* selects the only <li> element that are in a <ul> */
}
```
## Last Child Pseudo-Selector

Selects the last element inside of another element

In cases where there is only one element, that element counts as the first-child, only-child and last-child.

```css
/* Syntax*/

selector(s):last-child {
    /* Selects an element that is the last child element inside of another element */
}

/* Examples */

span:last-child {
    /* selects all last-child <span> elements. */
}

ul li:last-child {
    /* selects the <li> elements inside of any <ul>. */
}
```
## Nth child  Pseudo-Selector

Selects an element by its order in another element.


```css
/* Syntax*/

selector(s):nth-child(a) {
    /* Selects the nth (EX 1st, 3rd, 12th) child element in another element.*/
}

/* Examples */

:nth-child(8) {
    /* selects every element that is the 8th child of another element. */
}

div p:nth-child(2) {
    /* selects every element that is the 8th child of another element. */
}
```
## Nth Last Child Pseudo-Selector

Selects an element by its order in another element, counting from the back.

```css
/* Syntax*/

selector(s):nth-last-child(a) {
    /* Selects the children from the bottom of the parent. This is like nth-child, but counting from the back */
}

/* Examples */

:last-child(2) {
    /* selects all second-to-lastchild elements. */
}


```
## First of Type Selector

Selects the first element of a specific type.

```css
    /* syntax */
    selector(s):first-of-type {
        /* Selects the first element of that type within another element. */
    }

    /* Example(s) */
    
    span:first-of-type {
        /* selects the first <span> in any element */
    }
```
## Nth of Type Selector

Selects a specific element based on its type and order in another element with even or odd instances of that element.

```css
/* Examples */

div:nth-of-type(2) {
    /* selects the second instance of a div */
}

/* Formula */

selector:nth-of-type(An+B) {
    /* The nth-of-type formula selects every nth element, starting the count at a specific instance of that element. */
}


/* Formula example */

span:nth-of-type(6n+2) {
    /* Selects every 6th instance of a <span>, starting from and including the second instance */
}

selector(s):nth-of-type(odd) {
    /* selects all odd instances of the example class. */
}
```
## Only of Type Selector

Selects elements that are the only ones of their type within their parent element.

```css

    /* Syntax */
    :only-of-type {
        /* Selects the only element of its type within another element. */
    }

    /* Example(s) */

    p span:only-of-type {
        /* Selects a <span> within any <p> if it is the only <span> in there. */
    }
```
## Last of Type Selector


Select the last element of a specific type.

```css

    /* syntax */

    :last-of-type {
        /* Selects each last element of that type within another element */
    }

    /* Examples */

    div:last-of-type {
        /* selects the last <div> in every element. */
    }

    p span:last-of-type {
        /* selects the last <span> in every <p>. */
    }


```
## Empty Selector

Selects elements that don't have children.

```css

    /* syntax */

    :empty {
        /* Selects that doesn't have any other elements inside of them */
    }

    

    /* Example(s) */

    div:empty {
        /* selects all empty <div> elements */
    }
```
## Negation Pseudo-class

Selects all elements that don't match the negation selector.

```css

    /* Syntax */

    :not(x) {
        /* Selects all elements that do not match selector "x". */
    }

    /* Examples */

    :not(#fancy){
        /* Selects all elements that do not have id="fancy". */
    }

    div:not(:first-child){
        /* Selects every <div> that is not a first-child. */
    }

    :not(.big, .medium){
        /* Selects all elements that do not have class="big" or class="medium". */
    }

```
## Attribute Selector

Selects all elements that have a specific attribute.

```css

    /* Syntax */
    [attribute] {
    
    }


    /* Example(s) */

    a[href] {
        /* Selects all <a> elements that have a href="anything" attribute. */
    }

    [type] {
        /* selects elements that have a type="anything" attribute. */
    }

    input[disabled] {
        /* selects all <input> elements with the disabled attribute. */
    }
```
## Attribute Value Selector

Select all elements that have a specific attribute value.

```css
    /* Syntax */

    [attribute="value"] {
        /* Attribute selectors are case sensitive, each character must match exactly. */
    }

    /* Example(s) */

    input[type="checkbox"] {
        /* selects all checkbox input elements. */
    }
```
## Attribute Starts with Selector

Selects all elements with an attribute value that starts with specific characters.

```css

    [attribute^="value"] {

    }

    /* Example(s) */

    .toy[category^="swim"] {
        /* selects elements with class "toy" and either category="Swimwear" or category="Swimming". */
    }
```
## Attribute Ends with Selector

Selects all elements with an attribute value that ends with specific characters.

```css

    /* Syntax */

    [attribute$="value"] {

    }

    /* Example(s) */

    img[src$=".jpg"] {
        /* selects all images display a .jpg image. */
    }
```
## Attribute Wildcard Selector

Selects all elements with an attribute value that contains specific characters anywhere

```css

    /* Syntax */

    [attribute*="value"] {

    }

    /* Examples */

    img[src*="/thumbnails/"] {
        /* Selecs all image elements that show images from the "thumbnails" folder. */
    }

    [class*="heading"] {
        /* Selects all elements with "heading" in their class, like class="main-heading" and class="sub-heading" */
    }
```
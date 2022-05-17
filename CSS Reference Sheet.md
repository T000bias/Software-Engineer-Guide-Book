# CSS Reference Sheet

# Table of Content
- [CSS Reference Sheet](#css-reference-sheet)
- [Table of Content](#table-of-content)
  - [Media Queries](#media-queries)
    - [Create a Media Query](#create-a-media-query)
    - [Responsive Images](#responsive-images)
    - [Responsive Typography](#responsive-typography)
    - [Retina Image](#retina-image)
  - [Flexbox](#flexbox)
    - [display property](#display-property)
    - [flex-direction property](#flex-direction-property)
    - [justify-content property](#justify-content-property)
    - [align item property](#align-item-property)
    - [flex-wrap property](#flex-wrap-property)
    - [flex-shrink property](#flex-shrink-property)
    - [flex-basis property](#flex-basis-property)
    - [flex shorthand property](#flex-shorthand-property)
    - [order property](#order-property)
    - [align-self property](#align-self-property)
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

---

### Create a Media Query

Media Queries consist of a media type, and if that media type matches the type of device the document is displayed on, the styles are applied. You can have as many selectors and styles inside your media quuery as you want.

```css

    /* The CSS inside the media query is applied only if the media type matches that of the device being used. */

    /* When the device's width is less than or equal to 100px. */
    @media (max-width: 100px) {

    }

    /* When the device's height is more than or equal to 350px. */
    @media (min-height:350px) {

    }
```

---

### Responsive Images

To make images responsive with CSS add these properties.

```css

    img {
        /* The max-width of 100% will make sure the image is never wider than the container it is in */
        max-width: 100%;

        /* height of auto will make the image keep its original aspect ratio. */
        height: auto;
    }
```

---

### Responsive Typography

Instead of using em or px to size text, you can use viewport units for responsive typography. Viewport units, like percentages. are relative units, but they are based off differenet items. Viewport units are relative to the viewport dimensions (width or height) or a device, and percentages are relative to the size of the parent container element.

```css

    /* viewport values */
    p {
        /* Viewport width is a percentage of the viewport's width */
        /* 10% of the viewport width. */
        width:10vw;

        /* Viewport height is a percentage of the viewport's height */
        /* 3% of the viewport height. */
        height:3vh;

        /* Viewport minimum is a percentage of the viewport's smaller dimension of height or width. */
        /* 70% of the viewport's smaller dimension. */
        font-size:70vmin;

        /* Viewport maximum is a percentage of the viewport's bigger dimension of height or width. */
        /* 100% of the viewport's bigger dimension. */
        background:100vmax
    }

```

### Retina Image

Pixel density is an aspect that could be different on one device from others and this density is known as Pixel Per Inch (PPI) or Dots Per Inch (DPI). Due to the difference in pixel density between a "Retina" and "Non-Retina" displays with a High-Resolution Display in mind would render to a High-Resolution display.

To make images High-resolution is to define their width and height value as only half of what the original file is

---



## Flexbox
### display property
Placing the CSS property 
<code>display:flex;</code> on an element allows you to use other flex properties.

Adding <code>display:flex;</code> to an element turns it into a flex container.

This makes it possible to align any children of that element into rows or columns.

---
### flex-direction property
<code>flex-direction:;</code> controls if the flex items are columns or rows.


Values

<code>flex-direction:row;</code>

<code>flex-direction:column;</code>

<code>flex-direction:row-reverse;</code>

<code>flex-direction:column-reverse;</code>

**NOTE - The default value for the <code>flex-direction</code> is row.**

---
### justify-content property

![axes](https://www.w3.org/TR/css-flexbox-1/images/flex-direction-terms.svg)


The direction the flex items are arranged is called the **main axis**.

```css
/* Aligns all the flex items to the center inside the flex container */
justify-content:center;

/* Default Value
Aligns items to the start of the flex container.
row: pushes the items to the left
column: pushes the items to the top */
justify-content:flex-start;


/* Aligns items to the end of the flex container. For a row, this pushes the items to the right of the container. For a column, this pusheds the items to the bottom of the container. */
justify-content:flex-end;

/* Aligns items to the center of the main axis, with extra space placed between the items. The first and last items are pushed to the very edge of the flex container. */
justify-content:space-between;

/* First and last items are not locked to the edges of the container, the space is distributed around all the items with half space on either end of the flex container */
justify-content:space-around;

/* Distributes space evenly between the flex items with a full space at either end of the flex container */
justify-content:space-evenly;
```

---
### align item property


The `align-items` property is similar to `justify-content`. `align-items` property is to align flex items along the cross axis.

Flex containers also have a **cross axis** which is the opposite of the **main axis**. For rows, the **cross axis** is vertical and for columns, the **cross axis** is horizontal

```css
    /* Values */
    
    /* Aligns items to the start of the flex container. For rows, this aligns items to the top of the container. For columns, this aligns items to the left of the container */
    align-items:flex-start;

    /* Aligns items to the end of the flex container. For rows, this aligns items to the bottom of the container. For columns, this aligns items to the right of the conatainer. */
    align-items:flex-end;

    /* Align items to the center. For rows, this vertically aligns items (equal space above and below the items). For columns, this horizontally aligns them (equal space to the left and right of the items). */
    align-items:center;

    /* Stretch the items to fill the flex container. For example, row items are stretched to fill the flex container top-to-bottom. This is the default value if no align-item value was given */
    align-items:stretch;

    /* Align items to their baselines. Baseline is a text concept, think of it as the line that the letters sit on */
    align-items:baseline;

```

---
### flex-wrap property

The flex-wrap moves extra items into a new row or column. The break point of where the wrapping happens depends on the size of the items and the size of the container.

```css

    /* Values */

    /* This is the default setting, and does not wrap items */
    flex-wrap:nowrap;

    /* Wraps items onto multiple lines from top-to-bottom if they are in rows and left-to-right if they are in columns. */
    flex-wrap:nowrap;

    /* Wraps items onto multiple lines from bottom-to-top if they are in rows and right-to-left if they are in columns. */
    flex-wrap:nowrap;

```

---
### flex-shrink property

`flex-shrink` allows an item to shrink if the flex container is too small. Items shrink when the width of the parent container is smaller than the combined widths of all the flex items within it.

`flex-shrink` property takes numbers as values. The higher the number, the more it will shrink compared to the other items in the container.

---
### flex-basis property

`flex-basis` specifies the initial size of the item before CSS makes adjustments with `flex-shrink` or `flex-grow`.

---
### flex shorthand property

The `flex-grow`, `flex-shrink`, and `flex-basis` properties can all be set together by using the `flex` property.

---
### order property

The `order` property is used to tell CSS the order of how flex items appear in the flex container. By default, items will appear in the same order they come in the source HTML. The property takes numbers as values, and negative numbers can be used.

---
### align-self property

The `align-self` property allows you to adjust each item's alignment individually, instead of setting them all at once. `align-self` accepts the same values as `align-items` and will override any value set by the `align-items` property.

---

## CSS Selectors

---

### Type Selector 

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
### ID Selector

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
### Descendant Selector

The element inside of another element will be selected.

```css
selectedElement targetElemenet {
    /*  */
}

```
### Combined Selectors

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
### Class Selector

Selects elements by their class attribute.

```css
    /* Selects all elements with the attribute class="className" */
    .className {
        property: value;
    }
```
### Comma Combinator

You can combine selectors with commas.

```css

    A,B {
        /* This selects all A and B elements. You can combine any selectors this way, and you can specify more than two */
    }


```
### The Universal Selector

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
### Adjacent Sibling Selector

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
### General Sibling Selector

Select elements that follows another element. This gets all of the following elements instead of one like adjacent selector.

```css

    A ~ B {
        /* You can select all siblings of an element that follow it */
    }
```
### Child Selector

Select direct children of an element.

```css
    /* Syntax */
    A > B {
        /* Selects all B that are a direct children A */
    }
```
### First Child Pseudo-selector

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
### Only Child Pseudo-Selector

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
### Last Child Pseudo-Selector

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
### Nth child  Pseudo-Selector

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
### Nth Last Child Pseudo-Selector

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
### First of Type Selector

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
### Nth of Type Selector

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
### Only of Type Selector

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
### Last of Type Selector


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
### Empty Selector

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
### Negation Pseudo-class

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
### Attribute Selector

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
### Attribute Value Selector

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
### Attribute Starts with Selector

Selects all elements with an attribute value that starts with specific characters.

```css

    [attribute^="value"] {

    }

    /* Example(s) */

    .toy[category^="swim"] {
        /* selects elements with class "toy" and either category="Swimwear" or category="Swimming". */
    }
```
### Attribute Ends with Selector

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
### Attribute Wildcard Selector

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
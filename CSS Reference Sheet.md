# CSS Reference Sheet

# Content
1. CSS Selectors
    - [Type Selector](#type-selector)
    - [ID Selector](#id-selector)
    - [Descendant Selector](#descendant-selector)
    - [Combined Selectors](#combined-selectors)
    - [Class Selector](#class-selector)
    - [Comma Combinator](#comma-combinator)
    - [The Universal Selector](#the-universal-selector)
    - [Adjacent Sibling Selector](#adjacent-sibling-selector)
    - [General Sibling Selector](#general-sibling-selector)
    - [First Child Pseudo-selector](#first-child-pseudo-selector)

# CSS Selectors

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
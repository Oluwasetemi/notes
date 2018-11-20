
Table of content

<b>Objectives</b>

1. Define CSS and the role that it plays in web development
2. View websites before and after CSS has been added
3. Understanding the general rule for CSS syntax
4. Adding CSS to an html document-internal, in-line, external
5. Writing CSS proficiently

*CSS Reset*

*CSS Normalize*

## CSS Basics

### CSS Introduction

CSS is the presentational layer of the web. It shows the appearance of what we all view in the web browser: the color, the position, the arrangement and it seats on the foundational structure of the HTML and requires a deep understanding of HTML to writes effectively.

HTML and CSS with another call JavaScript has become the core technology of the web. The general structure is below(every css you will be writing in years to come must adhere to the core rule below) Understanding this structure will go quite a mile in learning how to write css.  

Writing Styles - 
inline using HTML Attributes, 
HTML Style tags, 
External style using link tag

### CSS Syntax 
```css
selectorlist {  
  property: value;  
  [more property:value; pairs]
}
```

... where selectorlist is: selector[:pseudo-class] [::pseudo-element] [, more selectorlists]

See selector, pseudo-class, pseudo-element lists below.

Selectors: Element, ID-#, and Class-. 

Others- attributes with various modifiers
	pseudo-class
	pseudo-element

Examples 
```css
p {
  color: red;
}

/*this speak to a paragraph contained in an html to change the color from the default appearance to a red color.*/

strong {
  color: red;
}

types
div.menu-bar li:hover > ul {
  display: block;
} 
```

We need to understand the selectorlist, :pseudo-class, ::pseudo-element, properties, values - possible values and default values.

### [Selectors](selectors.md)

From the section that explains they basic syntax of css we would note the `seclectorList` and it is very importance if you will understand css in general. 

SelectorList includes several ways of selecting elements in the html. In your quest to be an expert in writing css you will need to be able to demystify the  concept of selecting element engaging several ways made possible by elements, attributes, pseudo class, pseudo element and other specialized way of picking out a node from the DOM tree.

**Selectors: Element, ID-#, and Class-. **

**Others- attributes with various modifiers
pseudo-class
pseudo-element**

1. Type Selector - a type of an Element - an HTML Tag. 

We can select Element for styling in an html page but selecting the HTML tag individual or collectively. Examples p, img and so on. 

```css		
p {}
img, audio, video {}
```

2. ID - The ID provides a unique name for an HTML element. could be either the ID directly or a more specific element with it's specific id `Element#myid`. 
It is very specific and powerful. Don't use in an overly way. Denoted by #.

```css
#ID {}
	
Element#ID {}
```

3. Class - very similar to ID , denoted by . and can also stand alone or be combined with an Element. 

```css
Element.class OR .class.class {}
	
Element.class {}
```

4. Universal selector - A general selector for selecting everything. It is denoted *.

5. Descendant combinator - Since HTML is tree like and the root(html) is the root of the tree and we will have head and body as descendants of the root element. We could have ElementA and ElementB where ELementB is a descendants. Select ElementB that is a descendant of ElementA.ElementA ElementB {}p span {}ul a {}

6.  Child combinator - ul>li {}

7.  Adjacent sibling combinator - It selects the neighbor element. The direct sibling sitting side by side using the + sign.Element+Element {}

8.  General sibling combinator - Not many of us knows the tilda key on our keyboard. It's the key above the Left shift key. It selects an element preceded by another element using the ~.ElementA~ElementB {}

9.  Negation pseudo-class - It negates the selection using the psuedo class to select the inverse of the selected Elements.Element:not(p) {}.class:not(a) {}

10.  Attribute combinator - It is the combination of various ways in which we can use several modifiers to make selecting attributes of an element easy. Element[attr] {} /* an Element with an attr */Element[attr="value"] {}  /*an Element whose 'attr' value is exactly equal to 'value' */Element[attr~="value"] {} /* an ELement whose attr value is a list of whitespace-separated values, one of which is exactly equal to 'value'  */Element[attr^="value"] {} /* an Element whose attr value begins exactly with the string 'value' */Element[attr$="value"] {} /* an Element whose attr value ends exactly with the string 'value'. */Element[attr*="value"] {} /* an Element whose attr value contains the substring 'value' */Element[attr|="value"] {} /* an Element whoose attribute attr has a hypen-separated list of values beginning (from the left) with 'value' */

11.  Structural pseudo-classes - 

12. Link pseudo-classes

13. User action pseudo-classes - 

14. Lang pseudo-classes - 

15. Target pseudo-class - 

16. UI element states pseudo-classes - 

17. The first-line pseudo-element - 

18. The first-letter pseudo-element -

19. The before pseudo-element -

20. The after pseudo-element -


[Sizzle](https://sizzlejs.com) - A pure-JavaScript CSS selector engine designed to be easily dropped in to a host library.

### Specificity and inheritance and cascading
Specificity is the means by which browsers decide which CSS property values are the most relevant to an element and, therefore, will be applied. 

Specificity is based on the matching rules which are composed of different sorts of CSS selectors.As per CSS rules, directly targeted elements will always take precedence over rules which an element inherits from its ancestor.When multiple declarations have equal specificity, the last declaration found in the CSS is applied to the element. Specificity only applies when the same element is targeted by multiple declarations.
Specificity is a weight that is applied to a given CSS declaration, determined by the number of each selector type in the matching selector.

Rules to Note on Specificity

* Universal selector (*), combinators (+, >, ~, '') and negation pseudo-class (:not()) have no effect on specificity. (The selectors declared inside :not() do, however.)
	
* Inline styles added to an element (e.g., style="font-weight:bold") always overwrite any styles in external stylesheets, and thus can be thought of as having the highest specificity.
	
* ID selectors are highly specific.
	
* Class selectors, attributes selectors and pseudo-classes are less specific compared to ID selectors and Inline styles.
	
* Type selectors and pseudo-elements.

The !important exception
The amount of specificity a selector has is measured using four different values (or components), which can be thought of as thousands, hundreds, tens and ones — four single digits in four columns:

1. Thousands: Score one in this column if the declaration is inside a style attribute (such declarations don't have selectors, so their specificity is always simply 1000.) Otherwise 0.

2. Hundreds: Score one in this column for each ID selector contained inside the overall selector.

3. Tens: Score one in this column for each class selector, attribute selector, or pseudo-class contained inside the overall selector.

4. Ones: Score one in this column for each element selector or pseudo-element contained inside the overall selector.

Note: Universal selector (*), combinators (+, >, ~, ' ') and negation pseudo-class (:not)have no effect on specificity.
The following table shows a few isolated examples to get you in the mood. Try going through these, and making sure you understand why they have the specificity that we have given them.
Note: If multiple selectors have the same importance and specificity, which selector wins is decided by which comes later in the Source order.

### Inheritance In CSS
inheritance controls what happens when no value is specified for a property on an element. 

Refer to any CSS property definition to see whether a specific property inherits by default ("Inherited: yes") or not ("Inherited: no").


#### Inherited Properties
When no value for an inherited property has been specified on an element, the element gets the computed value of that property on its parent element. Only the root element of the document gets the initial value given in the property's summary.

#### Non-inherited Properties
When no value for a non-inherited property has been specified on an element, the element gets the initial value of that property (as specified in the property's summary).

#### Cascade
The cascade is an algorithm that defines how to combine property values originating from different sources. It lies at the core of CSS, as emphasized by the name: Cascading Style Sheets. 
This article explains what the cascade is, the order in which CSS declarations cascade, and how this affects you, the web developer.
The CSS cascade algorithm's job is to select CSS declarations in order to determine the correct values for CSS properties. 
CSS declarations originate from different origins: 

1. the user-agent style sheet, 
2. the author style sheet, 
3. and the user style sheet.

Though style sheets come from these different origins, they overlap in scope; to make this work, the cascade algorithm defines how they interact.The cascading algorithm determines how to find the value to apply for each property for each document element.

1. It first filters all the rules from the different sources to keep only the rules that apply to a given element. That means rules whose selector matches the given element and which are part of an appropriate media at-rule.

2. Then it sorts these rules according to their importance, that is, whether or not they are followed by !important, and by their origin. The cascade is in ascending order, which means that !important values from a user-defined style sheet have precedence over normal values originated from a user-agent style sheet:

3. In case of equality, the specificity of a value is considered to choose one or the other.


## Box Model 
let's introduce box-sizing! It is a CSS property that defines how to calculate the total width and height of an element. 
content-box gives you the default CSS box-sizing behaviour. 
If you set an element's width to 100 pixels, then the element's content box will be 100 pixels wide, and the width of any border or padding will be added to the final rendered width. while * border-box tells the browser to account for any border and padding in the values you specify for an element's width and height. If you set an element's width to 100 pixels, that 100 pixels will include any border or padding you added, and the content box will shrink to absorb that extra width. This typically makes it much easier to size elements.


CSS Basic Box Model is a module of CSS that defines the rectangular boxes—including their padding and margin—that are generated for elements and laid out according to the visual formatting model. This model defines how CSS lays out elements, including their content, padding, border, and margin areas.

CSS Box Model: Mastering margin collapsing, Visual formatting model are some of the things we will focus on.

Browser's rendering engine represents every element as a rectangular Box with each box composed of 4 main parts, 
	
* content edge

The content area, bounded by the content edge, contains the "real" content of the element, such as text, an image, or a video player. Its dimensions are the content width (or content-box width) and the content height (or content-box height). It often has a background color or background image.If the box-sizing property is set to content-box (default), the content area's size can be explicitly defined with the width, min-width, max-width, height, min-height, and max-height properties.
	
* padding edge

The padding area, bounded by the padding edge, extends the content area to include the element's padding. Its dimensions are the padding-box width and the padding-box height.The thickness of the padding is determined by the padding-top, padding-right, padding-bottom, padding-left, and shorthand padding properties.
	
* border edge

The border area, bounded by the border edge, extends the padding area to include the element's borders. Its dimensions are the border-box width and the border-box height.The thickness of the borders are determined by the border-width and shorthand border properties. If the box-sizing property is set to border-box, the border area's size can be explicitly defined with the width, min-width, max-width, height, min-height, and max-height properties. When there is a background (background-color or background-image) set on a box, it extends to the outer edge of the border (i.e. extends underneath the border in z-ordering). This default behavior can be altered with the background-clip css property.background-clip: border-box | padding-box | content-box | text
	
* margin edge

The margin area, bounded by the margin edge, extends the border area to include an empty area used to separate the element from its neighbors. Its dimensions are the margin-box width and the margin-box height.

The size of the margin area is determined by the margin-top, margin-right, margin-bottom,margin-left, and shorthand margin properties. 
When margin collapsing occurs, the margin area is not clearly defined since margins are shared between boxes.

Properties controlling the flow of content in a oxoverflowoverflow-xoverflow-y
Properties controlling the size of a boxheightwidthmax-heightmax-widthmin-heightmin-width
Properties controlling the margins of a boxmarginmargin-bottommargin-leftmargin-rightmargin-top
Properties controlling the paddings of a boxpaddingpadding-bottompadding-leftpadding-rightpadding-top

Other properties visibility

### CSS Backgrounds and Borders: Using multiple backgrounds

Exercise
Create a form for registering participant for a meeting in your organization
*use html 5 form validation

*CSS Advanced
### Layout Modes
CSS Flex and CSS  Grid
I will be explain modern layout systems using flex box and grid systems. We will examine critically the the display and the positional edge in every rendered element to give us a clear view as to how we can arranged the generated boxes to make meaning to our users. 

Typography
Several Functions 
e.g calc(), 
repeat(),
At-rule @media, 
@support

Basic styling with space management
CSS Variables  and CSS types(data types) with possible values
CSS Frameworks - BootstrapCSS Project 
Reference
* [css reference io](https://cssreference.io)
* [CSS Selector Game](http://flukeout.github.io/)

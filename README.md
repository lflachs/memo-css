# CSS Memo

## Insert a stylesheet

*You can also type style:css in visual studio, then tab* 

    <link rel="stylesheet" href="style.css">

---

## Id or Class?

id (#) can be use on one specific element. Class (.) can be used on multiples elements. 

In visual studio, you can type the name of your element followed by the right symbol and the name of your Id or class then tab.

ex: div.myDiv ⇒ <div id="myDiv">

---

## CSS selector

![CSS%20Memo/Untitled.png](CSS%20Memo/Untitled.png)

In your CSS sheet, you should declare first **the element you want to target**, then change its **proprety** by giving the **new value.** 

---

## Box Model

![CSS%20Memo/Untitled%201.png](CSS%20Memo/Untitled%201.png)

There is multiple way to change margin and padding:

    myDiv{
    	padding:10px;
    	/* 10 px everywhere */
    	padding: 10px 20px;
    	/* 10px up and bottom, 20px left and right */
    	padding: 10px 20px 40px 50px;
    				/* top right, bottom, left (like a clock) */
    	padding-right: 20px
    }

---

## Box-sizing

It's recommended that you change the box-sizing to border-box so that when you define an element size it doesn't take consider the padding and margin.

![CSS%20Memo/Untitled%202.png](CSS%20Memo/Untitled%202.png)

[https://connorshea.gitlab.io/blog/css-that-doesnt-suck.html](https://connorshea.gitlab.io/blog/css-that-doesnt-suck.html)

    *, *:before, *:after {
      box-sizing: border-box;
    }

---

## Browser default proprety

By Default, there is some css proprety applied by the browser, for ex there is margin and padding arround the body:

To reset it you can type

    html, body{
    	padding:0; 
    	margin:0;
    }

---

## Display : block, inline, inline-block

![CSS%20Memo/Untitled%203.png](CSS%20Memo/Untitled%203.png)

**Block :** Elements are one under the others the block element will take the full width available, but you can change its size.

⇒ *div, h1 (and other "h"s), p, form, header, footer, section*

**Inline :** Elements are in the same line, the element take only the needed width, you can't change its size.

⇒ *span, a, img*

**Inline-block:** Elements are in the same line, the elements takes only the widththey need, but you can change their size using height and width.

**None :** Element is completely removed from the html flow and is invisible 

---

## Display: none/visibility Hidden?

- Display: none ⇒ make the content out of the html flow.
- Visibility: hidden ⇒ make it invisible but stay in the flow.

[CSS Layout - The display Property](https://www.w3schools.com/css/css_display_visibility.asp)

---

## Max-width

Setup the max-width will allow your element to resize when the viewport is smaller than the width you want for this element.

[CSS Layout - width and max-width](https://www.w3schools.com/css/css_max-width.asp)

---

## Positions

![CSS%20Memo/Untitled%204.png](CSS%20Memo/Untitled%204.png)

[https://css-tricks.com/absolute-positioning-inside-relative-positioning/](https://css-tricks.com/absolute-positioning-inside-relative-positioning/)

**Static :** Default, the element follow the normal html workflow

**Absolute:** The element stop following the workflow, and you can move it by giving top left right bottom property.

if there is a parent element that have a absolute or relative position : the element will be positioned regarding this element

in other case, the element will be positioned rergarding the body

**Relative:** The element stop following the workflow and you can move it by giving top left  right bottom property that will be the position relative to its normal position.

**Fixed:** The element stay always at the same place, even if we scroll

**Sticky:** The element follow the user flow, when scrolling it will stay at the top of the browser window until it reach the end of its parent.

---

## Center in CSS

### Margin auto:

If your element is a block element you can use the margin:auto method

    div{
    	width:500px;
    	height:500px;
    	margin:0 auto;
    }

## Text-align: center

The trick here is to give to the parent the proprety text-align:center and give to the child a display of linline-block.

    .parent{
    	text-align:center;
    }
    
    .children{
    	display:inline-block;
    	width:500px;
    	height:500px;
    }

## Left right :50% - Absolute

If the element is an absolute element you can set right and left to 50%

    div{
    	position:absolute
    	left:50%;
    	right:50%;
    	transform: translate(-50%, -50%);
    }

You can also center horizontally using transform: translate(-50%, -50%);

---

## Ressources

[Learn web development](https://developer.mozilla.org/en-US/docs/Learn)

[CSS-Tricks](https://css-tricks.com/)

[Layout Land](https://www.youtube.com/layoutland)
# Flexbox

Flexbox is a layout method for arranging items in rows or columns. You can easily stretch or shrink items with this technique.

We used to do layouts with floats, but they were quite limited. Vertical centering or responsively dividing space between child elements were really difficult to achieve.

In a few examples we will look at flexbox basics so we can easily build complex layouts.

The very best resource I have found is the '[a guide to flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)' tutorial on CSS Tricks. We will probably reference that guide a few times during the exercises.

## Box model

Before starting to learn flexbox, we need to understand the box model. Let's look at some examples.

### Note - Default margin

Remove `margin: 0;` from `*` element. This will show that the `body` element has a margin of `8px` by default. You can see this in the devtools. The browser adds some default styling to some elements, a lot of 'css resets' will remove this.

### Step 1 - Block vs inline

In CSS there are two kind of elements: block and inline.

Block:

- Breaks a line
- Fills 100% width of the parent container
- Can be sized with `width` and `height`

Inline:

- Does not break a line
- Cannot be sized with `width` and `height`
- Some weird vertical/horizontal padding & margin properties

Inline-block:

- Same as inline, but can be sized with `width` and `height`

### Step 2 - Size of the box

There are a few properties that can be used to size the box. First, lets look at `padding`. Padding will increase size of the box from the **inside**. This is useful when you want the background color to stay the same.

If you add `margin`, it will increase the size of the box from the **outside**. This is useful when you want to add some space around the box or between elements.

Finally we have the `border` property. This is used to add a border around the box.

### Step 3 - Border box

If we add `box-sizing: border-box;` a box, it will change the way the size is calculated.

- `content-box`: the default. Width and height values apply to the element’s content only. The padding and border are added to the outside of the box.
- `padding-box`: Width and height values apply to the element’s content and its padding. The border is added to the outside of the box. **Firefox only**
- `border-box`: Width and height values apply to the content, padding, and border.

Margin will always be added to the outside of the box.

### Step 4 - Always use `border-box`

It is best to always work with `border-box` because it is the most consistent way of sizing. Add this for [each element](https://css-tricks.com/inheriting-box-sizing-probably-slightly-better-best-practice/) on the page.

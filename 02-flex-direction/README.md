# Flexbox and flex direction

The best reference for flexbox for me is the [CSS Tricks flexbox tutorial](https://css-tricks.com/snippets/css/a-guide-to-flexbox/).

Note: I added a border to show what happens with the `container` div.

## Display flex

Right now the `item` divs are using **normal flow**. Which means that they behave like a block elements.

Add `display: flex;` to `.container`. Now you can see that the boxes will be aligned next to eachother. They no longer behave like block objects.

This is almost the same as adding `display: inline;` to the `item` divs. But look at the spacing.

**Question**: Does anyone know why the spaces are here?
**Answer**: Because text has spacing between words, and we have spaces in our HTML. Add `<p>Hello world</p>` and increase the spaces, you can see they collapse. This is also happening with our `item` divs. Remove the spaces and you will see they no longer have spacing.

## Flex direction

The default direction is `flex-direction: row;`. You can see that nothing has changed if we add it to `.container`.

We also have the option to change the direction. The other option is `flex-direction: column;`. This will look familiar.

**Show**; remove the `display: flex;` and `flex-direction: column;` from `.container` and it will look the same.

This does **not** mean that `flex-direction: column;` and _normal flow_ is the same thing. Let's look at `flex-grow` for this.

## Flex grow

Add `height: 300px;` to `.container`. We now have some extra space which we can use with flexbox.

The `item` divs are now using their own size, based on the content. By using the `flex-grow` property, we can change the size of the `item` divs.

Add `flex-grow: 1;` to the `.green` div. You can see that it will fill up the remaining space, because we allow it to grow.

**Show**: The flexbox guide and explain what `1` means.

If we disable `height: 300px;` there will be no reason to grow, so we are back to the old state.

Now disable `flex-grow: 1;` and change `flex-direction: column;` on `.container` to `flex-direction: row;`. Now enable `flex-grow: 1;` on `.green` and you will see that it will fill up the remaining space.

**Show**: The cool thing about this is that it is _responsive_.

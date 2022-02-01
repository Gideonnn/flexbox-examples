# Flexbox resizing

The opposite of `flex-grow` is `flex-shrink`.

## Intrinsic width

If we have no intrinsic width, like `width` or `min-width`, then the element will be sized to its content. In this case that is 0px.

Add `width: 150px;` to the `.item` divs.

## Default value

The default value for `flex-shrink` is `1`. You can see that in the flexbox guide.

**Show**: resize the window and notice the `.item` divs are resized evenly.

## Shrink factor

Add `flex-shrink: 2;` to `.red`. This means it will shrink twice as fast as the other items.

By adding `flex-shrink: 0;` to `.blue` we can make it not shrink at all.

## Flex grow

We can combine both `flex-shrink` and `flex-grow` to make the element shrink and grow at the same time.

Add `flex-grow: 1;` to `.item`. This will make all items grow equally, and still shrink correctly once the `width` has been reached.

## min-width

Even if `flex-grow` is set, the `width` property is still used for shrink decisions. We can also use `min-width`, but it has some quirks.

Remove `flex-grow` from `.item`.
Remove `flex-shrink` from all items.
Add `border: 5px solid purple;` to `.container`.

Now we can see that the container is not pushed off-screen and every item shrinks evenly.

Change `width` to `min-width` and notice that the container is pushed off-screen.

## flex-basis

For better control, we can use `flex-basis` instead of `width`. This is a flexbox-specific property to define the initial size of an element.

There is an order of properties which flexbox uses to determine the size of an element:

1. `flex-basis` is highest priority, but it does respect `min-width` and `max-height`.
2. The specified `width` of the element.
3. The content of the element.

Set flex-basis to `auto` and text in the elements:

- Red
- GreenGreenGreen
- Blue

Add `flex-grow: 1;` to `.item` and notice that the `item` divs are not the same size.

**Show**: flexbox guide graphic linked to under the `flex-basis` section.

Change `flex-basis` to `0` and notice the difference.

## Flex 💪

Until now we have been using `flex-grow`, `flex-shrink` and `flex-basis`. There is a property called `flex` which does all three. Just like `margin` and `padding`.

The default is `flex: 0 1 0%`. Which means `flex: <grow> <shrink> <basis>`.

It is recommended to always use this property, instead of using them seperately. You can just omit the `<grow>` and `<shrink>` values if you do not need them.

So using `flex: 1;` instead of `flex-grow: 1;` is fine.

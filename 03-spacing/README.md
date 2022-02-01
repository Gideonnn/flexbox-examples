# Flexbox spacing

We can use two different methods to space elements in a flexbox and we will look at them both.

The `item` divs now have a `width` assigned and we are not using `flex-grow` here.

## Justify content

Add `justify-content: flex-start;` to the parent flexbox and notice nothing changes. This is the default value.

Most used will probably be `center`.

**Show**: difference between `space-evenly`, `space-around` and `space-between`.

Bonus: show `gap: 10px;` with `justify-content: space-between;`

## Align items

Add `height: 300px;` to the `.container` div. Then add `height: 50px;` to the `.item` divs.

Now add `align-items: center;` to `.container`.

Bonus: there is also `align-self: flex-end;` which will align the specific item it is applied to.

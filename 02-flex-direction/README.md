## Step 1

Add `display: flex;` to `.container`. Now you can see that the boxes will be aligned next to eachother. They no longer behave like block objects.

## Step 2

Add `flex-direction: row;` to `.container` and notice that nothing is changed. So the default direction is row.

## Step 3

Change it to `flex-direction: column;` and notice the difference. `column` is used for vertical aligntment and `row` is used for horizontal alignment.

## Step 4

Notice that the `.container` div is still spanning the whole width of the `body`. To change this we need to add `display: flex;` to `body`. We can also add `flex-direction: column;` to `body` and it goes back to before.

## Question

What is the difference between not using `display: flex;` and `flex-direction: column;`, and using it?

## Answer

If we do not use `display: flex;` for `body` we rely on the elements intrinsic height, with flex we can control it.

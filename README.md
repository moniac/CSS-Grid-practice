# CSS Grid Practice

## What is `CSS Grid`?

CSS Grid is a new method of defining layouts in CSS. Where it differs from our old way of working is that Grid is two-dimensional. Basically, you define the height and the width, define the segments and are then able to place your content where you wish, without the use of any CSS hacks.

## Why should I learn `CSS Grid`? What about the older 😩 browsers?

I used to be of the opinion that there is little reason to learn something that won't be widely implemented yet. After [watching a presentation by Morten Rand-Hendriksen](https://www.youtube.com/watch?v=txZq7Laz7_4), my opinion has changed on the matter.

There is no need for us to wait, we should push CSS Grid forward. A nice solution for the older browsers that _don't_ support `CSS Grid` is to simply serve them the mobile version of the website. 

This means that instead of developing for screen sizes, we develop for browser versions.

Here is a small example of what that would look like;

`@supports (display: flex) {
  div {
    display: flex;
  }
}`

`
@supports not (display: flex) {
  div {
    float: right;
  }
}
`

As you can see here, CSS can detect if someone can use CSS Grid or not. This makes our life much easier.

What sometimes is overlooked by some, is that by applying Grid to an element, you override properties such as floats. This is really nice because it saves us work in the end.

## Let's start!

# CSS Grid Practice

## What is `CSS Grid`?

CSS Grid is a new method of defining layouts in CSS. Where it differs from our old way of working is that Grid is two-dimensional. Basically, you define the height and the width, define the segments and are then able to place your content where you wish, without the use of any CSS hacks.

## Why should I learn `CSS Grid`? What about the older 😩 browsers?

I used to be of the opinion that there is little reason to learn something that won't be widely implemented yet. After [watching a presentation by Morten Rand-Hendriksen] (https://www.youtube.com/watch?v=txZq7Laz7_4), my opinion has changed on the matter.

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

## Let's start! - Breaking down the terminology

#### `display: grid;`
Perhaps the most important one to know, the ability to define an element as a Grid container.
What this will do is *remove any existing floats and clears* and turn the element into a Grid container.

#### `grid-template-columns: 100px 100px;`
This segments the container horizontally in defined pieces, right now it will have two blocks of a 100px wide each.

#### `grid-template-rows: 100px 100px;`
This segments the container vertically in defined pieces, right now it will have two blocks of a 100px tall each.

### Other ways of defining segments in `grid-template-*`

You can imagine it would be really annoying if you needed a container that has 5 columns and you have to type 100px 5 times.

That's why there is a small function that will help you with this, it works like this;
`grid-template-columns: repeat(5, 100px);`

This will do the same thing as;
`grid-template-columns: 100px 100px 100px 100px 100px;`

### Fragments

Let's say you have a container, you give it two columns, you know you want the first column to be a 100px, and the second one can take up the rest of the space.

Usually you would something like this;
`grid-template-columns: 100px 80%;`

Which works, but there are better ways of going about this.
One of those ways is using Fragments, defined as `fr` in CSS.

`grid-template-columns: 100px 1fr;`

Another way of going about this would be;

`grid-template-columns: 100px auto;`

This will make the second column as wide as the available space.

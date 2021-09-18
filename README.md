# Custom framework

This is a project for TOP in which you are supposed to create your own simple grid-based framework and clone a site with it.

**This framework is nonresponsive and _heavily_ inspired by [960 grid system](http://960.gs/)**

## Utilities
This framework has 2 utilities - **CSS reset** and **default font properties** for body.
  
The font properties:

```
body {
  font-size: 1.125rem;
  font-family: "Open Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
}
```

## Classes
### Foundations
  **container**: container is 96Opx wide
  
  **row**: a row is as wide as the container (960...)

### Blocks
Every block has 10px margin left and right, in other words the gutters are 20px.
There are 12 blocks total, each is 60px + 20px wider than the last

  **block-1**: smallest block, 60px wide with 10px left and right margin = 80px total width
  
  **block-2**: 140px wide
  
  **block-3**: 220px wide
  
...and so on.
 
 ### Fillings
You use fillings to position blocks as you see fit.
Always fill the row with 12 blocks / fillings.
Left fillings belong to the left and right fillings to the right (duh).
There are 12 left and right fillings in total and these fillings are as big as blocks.
  
  **left-1**: 80px wide like block-1
  
  **right-1**: 80px wide like block-1
  
  **left-2**: 160px wide like block-2
  
  **right-2**: 160px wide like block-2
  
...and so on.

## How to use

1. Intiate a container like so
```
 <div class="container">
 
 </div>
```

2. Add a row(s)
```
 <div class="container">
  <div class="row">
  
  </div>
  <div class="row">
  
  </div>
 </div>
```

 3. Fill the row with content using blocks and fillings (**the row must contain 12 blocks in total!**)
```
 <div class="container">
  <div class="row">
    <div class="block-2 left-5 right-5">
      <p>I am 160px wide with 400px padding left and right!</p>
    </div>
  </div>
  <div class="row">
    <!-- THIS CREATES A 2 COLLUMN LAYOUT -->
    <div class="block-4 left-2">
      <p>I am 320px wide with 160px padding left!</p>
    </div>
    <div class="block-4 right-2">
      <p>I am 320px wide with 160px padding right!</p>
    </div>
  </div>
 </div>
```

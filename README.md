# Grid Framework
This is a simple twelve column grid framework that uses CSS flexbox.
I used the approach used by bootstrap and the class names are the same.
- from [The Odin Project's curriculum](https://theodinproject.com)

# Table of contents

- [How to use](#how-to-use)
- [Built with](#built-with)
- [Features](#features)
  - [\_reset.scss](#_resetscss)
  - [\_utilities.scss](#utilitiesscss)
  - [\_grid.scss](#gridscss)
  - [\_main.scss](#mainscss)
- [What I learned](#what-i-learned)

# How to use
- Copy the framework.css to your project.
- Or clone the repository to make changes -`git clone https://github.com/peter-abah/grid-framework.git`

# Built with
- scss
- css

# Features
The framework is composed of four scss files

## \_reset.scss
reset styles by Eric Meyer

## \_utilities.scss
Consists of classes for margin, flex, fixed position and border radius
- `.mx-auto` sets margin-left and margin-right to auto
- `.me-auto` sets margin-left to auto
- `.me-auto` sets margin-right to auto
- `.d-flex` sets display to flex
- `.flex-col` sets flex-direction to column
- `.flex-wrap` sets flex-wrap to wrap
- `.d-block` sets display to block
- `.fixed-top` sets postion to fixed and sets top and left to 0
- `.fixed-bottom` sets position to fixed and sets bottom and left to 0
- `.rounded-circle` sets border-radius to 50%
- `.img-fluid` sets max-width to 100% and height to auto to prevent overflow

## \_grid.scss
This contains the container and grid classes. It consists of:
- `.container` creates a responsive element at automatically resizes at several breakpoints. The implementation is the same as 
bootstrap `.container ` classes.The breakpoints are:
    * below 576px: the container has a full width.
    * `$sm` 576px: The container resizes to 540px.
    * `$md` 768px: The container resizes to 720px.
    * `$lg ` 992px: The container resizes to 960px.
    * `$xl` 1200px: The container resizes to 1140px.
    * `$xxl` 1440px: The container resizes to 1320px.
    * The `.container` class can also have a suffix of the breakpoints like `.container-lg`. This will make the element to have a
    100% width until it reaches the breakpoints. For example `.container-lg` will have a width of 100% at any width below 960px and at 960px and above it will behave like `.container` class.
    * `.container-fluid` This sets the width to 100% at all screen sizes

- `.row` This acts as a row in the grid and accomodates the `.col` classes. The implementation is also the same as bootstrap
classes with the `.col` classes. The row classes can contain `.col-*` classes where \* is any number from 1 to 12 inclusive, but 
the `.col-*` classes must add up to 12 or lower to avoid unexpected behavior. If the `.col` class is used without any number suffix it will automatically resize to fill the `.row` parent.
- The column classes can also have a form of `col-**-*` where \** is a breakpoint {sm, md, lg, xl, xxl} and \* is a number between
1 to 12 e.g `.col-xl-6`. 
It works the same way like the `.col-*` classes but when the screen is at a width below the breakpoint, the columns will
fill the entire width and stack on top each other.

## \_main.scss
This files just imports the partials

## What I learned
I used this project to practice my scss skills and also to understand Bootstrap better
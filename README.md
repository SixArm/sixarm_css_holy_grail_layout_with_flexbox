# SixArm.com » CSS » <br> Holy Grail layout with flexbox

To accomplish a CSS "Holy Grail" layout with flexbox,
we use the excellent work published by Philip Walton,
in the open source "Solved By Flexbox" repository:
https://github.com/philipwalton/solved-by-flexbox/blob/master/demos/holy-grail.md

Files:

  * [demo.css](demo.css)
  * [demo.html](demo.html)


## Changes ##

We have edited the CSS code with the goal of making it easier for beginners:

 * Added comments and examples
 * Added blank classes to make it easier to see how to customize this.
 * Omitted inessential items, such as margin, padding, color, border, etc.
 * Renamed classes to make them more generic and also more semantic.


## Naming Conventions ##

The CSS code uses the naming conventions of SuitCSS:

  * .ComponentName
  * .ComponentName-partName
  * .ComponentName--modifierName
  * .ComponentName.is-stateOfComponent

If you know CSS well, and you want to optimize this file for speed,
then you may want to elide the blank classes, combine equal classes,
delete these comments, and ideally also use a CSS preprocessor.


## Header, Leader, Footer ##

The "header" and "footer" are the typical HTML5 tags.

The "leader" is our naming convention for the middle area
that goes between the header tag and the footer tag.
We hope the HTML standard will add a tag for this area.

Some coders call it "master container", or "body content",
or similar names. You can rename "leader" if you prefer.

Usage:

    <header class="HolyGrail-header">...</header>
    <div class="HolyGrail-leader">...</div>
    <footer class="HolyGrail-footer">...</footer>


## Main Area ##

The layout has three major areas:

 * The first area. This is the left column on a big screen, or the top row on a small screen.
 * The main area. This is the middle center area on any size scren, and it grows to fit.
 * The last area. This is the right column on a big screen, or the bottom row on a small screen.

Usage:

    <aside class="HolyGrail-leader-first">Show first, at top or left</aside>
    <main class="HolyGrail-leader-main">Show in main area, in the middle</main>
    <aside class="HolyGrail-leader-last">Show last, at bottom or right</aside>

We recommend using the HTML tag `main` for the main area.
We suggest using the HTML tag `aside` for the other two areas,
unless you have a better tag, such as `nav` for a navigation area.

If you're building a page that you want to be indexed by search engines,
then we suggest you write the `main` area first because it may improve SEO.

## Media queries for responsive layout ##

 * A small screen layout uses three rows.
 * A large screen layout uses three columns.

We choose 768 pixels as the start of a large screen size.

If you prefer different settings, or prefer more than two
screen sizes, then you'll want to edit these media queries.

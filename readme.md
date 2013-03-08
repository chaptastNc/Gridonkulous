Gridonkulous: A tiny fluid grid for Less
========================================

Gridonkulous is a simple fluid grid system for Less. You can use it with semantic class names or numerical class names, your choice. It's mobile-first and easy to combine with media queries to create a fully responsive grid, starting from any number of columns.

**[View Demo](http://demo.madebyraygun.com/gridonkulous)** | **[Download](https://github.com/daltonrooney/Gridonkulous/archive/master.zip)**

###Usage

Import grid.less into your Less stylesheet and change the variables at the top if necessary. You can set up your grid with any number of columns and set your gutter in px, ems, or %; Each column is 100% by default (mobile-first design) so set a breakpoint where you want the columns to kick in.

###Example

```html
<div class="row">
	<div class="col primary"> ... </div>
	<div class="col secondary"> ... </div>
</div>
```

```css
@media only screen and (min-width: @breakpoint) {
	.primary { .columns(8); }
	.secondary { .columns(4); }
}
```

**In your markup:** Add a "row" class to the containing element for each row and a "col" class to each element in your grid. You can use semantic class names (i.e.: primary, secondary) or numerical class names (i.e.: one, two, thirteen).

**In your stylesheet:** Add the .columns() mixin to already existing classes or create new classes. Wrap it inside a media query using the @breakpoint variable for mobile-first layout. If you need multiple breakpoints, just add them in order: 

```css
@media only screen and (min-width: 600px) {
	.primary { .columns(8); }
	.secondary { .columns(4); }
}

@media only screen and (min-width: 900px) {
	.primary { .columns(9); }
	.secondary { .columns(3); }
}
```

### Credits

Made by [Raygun](http://madebyraygun.com). Inspired by [The Semantic Grid System](http://semantic.gs) and [Dead Simple Grid](https://github.com/mourner/dead-simple-grid).
#Tatami CSS
Tatami is a beautiful, fully responsive, style agnostic CSS boilerplate written in LESS.

It is based on other similar projects as [Skeleton](getskeleton.com), [Preboot](getpreboot.com) and [Boostrap](twitter.github.io/bootstrap/‎). It includes:

* a flexible CSS grid;
* a base stylesheet;
* a set of useful LESS mixins.

##Flexible CSS Grid
Tatami includes LESS mixins to obtain fluid and fixed grids.

`#grid > .base-classes()` prints grids base classes.

`#grid > .grid(@width, @pxGutterWitdh, @numberOfColumns)` prints fixed grid specific classes.

`#grid > .grid(@maxWidth, @%gutterWidth, @numberOfColumns)` prints fluid grid specific classes.

`#grid > .mobile(@width, @pxGutterWitdh)` prints specific classes for mobile devices.

####Usage Example

```Less
\#grid > .base-classes();

\#grid > .grid(1170px, 30px, 12);

\#grid > .grid(percentage(1), 
percentage(0.02564102564103), 12);

@media only screen and (min-width: 980px) and (max-width: 1169px) {
	#grid > .grid(980px, 24px, 12);
}
@media only screen and (min-width: 768px) and (max-width: 979px) {
	#grid > .grid(768px, 20px, 12);
}

\#grid > .mobile(767px, 20px);
```

##Base stylesheet
Check the files into the expamles folder.

Tatami defines a set of variables which guide the aspect defined in the base stylesheet.

```Less
//Controls root font size
@fontSize: 14px;

//Controls root base line and element margins
@baselineSize: 20px;

//Controls ul lateral size
@lateralSize: 30px;

//background color
@backgroundColor: #fff;

//root text color
@textColor: #444;

//hr and blockquote border colors 
@bordersColor: darken(spin(@textColor, 5), 10%);
@formsBorderColor: lighten(spin(@textColor, -10), 20%);
@formsFocusBorderColor: darken(spin(@textColor, 10), 20%);

//titles color
@titlesColor: darken(spin(@textColor, 5), 10%);

//link and link:hover colors
@linkColor: @textColor;
@linkHoverColor: arken(spin(@textColor, 5), 10%);

//button colors
@buttonColor: #ccc;
@buttonHoverColor: #aaa;

//base font stack and titles font stack
@baseFontStack: "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
@titlesFontStack: "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
```

##LESS Mixins

####Generic Mixins

`.clearfix()` a micro clearfix mixin;

`.center-block()`;

`.size(@width, @height)`;

`.square(@size)`;

`.resizable(@direction)`;

`.hide-text()` an image replacement mixin;

`.text-truncate()` a text overflow management mixin;

`.content-columns(@width, @count, @gap)` a CSS3 columns mixin;

`.opacity(@opacity)`

`.input-block-level()` a mixin to full-width input elements;

`.appearance(@string)`;

`.retina-image(@file-1x, @file-2x, @width-1x, @height-1x)`;

`placeholder(@color)`;

`user-select(@select)`;

`background-clip(@type)`;

`box-sizing (@type)`;

####Border Radius Mixins

`border-radius(@topright, @bottomright , @bottomleft , @topleft)`;

`border-radius(@radius)`;

`border-top-radius(@radius)`;

`border-right-radius(@radius)`;

`border-bottom-radius(@radius)`;

`border-left-radius(@radius)`;

####Shadow Mixins

`text-shadow(@string)`;

`drop-shadow(@string)`;

`inset-shadow(@string) `;

####Gradient Mixins

```Less
\#gradient {
	.horizontal(@startColor: #555, @endColor: #333)

	.vertical(@startColor: #555, @endColor: #333)

	.directional(@startColor: #555, @endColor: #333, @deg: 45deg) 

	.horizontal-three-colors(@startColor: #00b3ee, @midColor: #7a43b6, @colorStop: 50%, @endColor: #c3325f)

	.vertical-three-colors(@startColor: #00b3ee, @midColor: #7a43b6, @colorStop: 50%, @endColor: #c3325f)

	.radial(@innerColor: #555, @outerColor: #333)

	.striped(@color: #555, @angle: 45deg)
}
```

####IE Mixins

`reset-filter()` a mixin to reset IE filters;

####CSS Animations Mixins

`transition(@transition)`

`transition-property(@transition-property)`

`transition-duration(@transition-duration)`

`transition-delay(@transition-delay)`

`transition-duration(@transition-duration)`

`rotate(@degrees)`

`scale(@ratio)`

`translate(@x, @y)`

`skew(@x, @y)`

`translate3d(@x, @y, @z)`

`backface-visibility(@visibility)`

####Button Style Mixin

`buttonStyle (@baseColor, @hoverColor, @textColor, @borderColor)`
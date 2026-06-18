## CSS PART3

# 1_CSS_Units

Definition:
CSS units are used to specify the size of elements, text, margins, padding, width, and height in a web page.

Types of CSS Units
# Absolute Units (Fixed Size)
px – Pixel
cm – Centimeter
mm – Millimeter
in – Inch
pt – Point
pc – Pica

Example:

h1 {
    font-size: 20px;
}
# Relative Units (Responsive Size)
% – Relative to parent element
em – Relative to parent font size
rem – Relative to root font size
vw – 1% of viewport width
vh – 1% of viewport height

Example:

p {
    font-size: 2rem;
}

div {
    width: 50%;
}

# 4_em_rem_px

1 px (Pixel)

Theory: Fixed-size (absolute) unit.

Example:

p {
    font-size: 20px;
}
2 em

Theory: Relative to the parent element's font size.

Example:

.parent {
    font-size: 20px;
}

.child {
    font-size: 2em;
}

Result: 40px

3 rem (Root em)

Theory: Relative to the root (html) font size.

Example:

html {
    font-size: 16px;
}

h1 {
    font-size: 2rem;
}

Result: 32px

# 5_Viewport_Units

## Viewport Units 


Viewport units are relative units based on the size of the browser window.

vw = 1% of viewport width
vh = 1% of viewport height
vmin = 1% of the smaller viewport dimension
vmax = 1% of the larger viewport dimension

Example:

.box {
    width: 50vw;
    height: 50vh;
}

Result:

Width = 50% of browser window width
Height = 50% of browser window height 

# 6_CSS_Floats

CSS Floats

The float property is used to position an element to the left or right of its container, allowing text and other elements to wrap around it.

Values:

left
right
none (default)
Example
img {
    float: right;
}
<img src="image.jpg">
<p>This text will wrap around the image.</p>

# 7_CSS_Positions

CSS position property is used to control the placement of an element on a web page.

Types of Position:

static (default) – Element follows normal page flow.
relative – Positioned relative to its normal position.
absolute – Positioned relative to the nearest positioned parent.
fixed – Stays fixed on the screen even when scrolling.
sticky – Acts like relative until a scroll point is reached, then becomes fixed.
Example
<div class="box">Hello</div>
.box {
  position: relative;
  top: 20px;
  left: 30px;
  background: lightblue;
}

Output:
The box moves 20px down and 30px right from its original position.
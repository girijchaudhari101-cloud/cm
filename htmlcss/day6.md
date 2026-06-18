# CSS_Grid

CSS Grid is a 2-dimensional layout system used to arrange elements in rows and columns. It helps create responsive and organized web page layouts.

Example:
HTML:

<div class="container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
</div>

CSS:

.container {
  display: grid;
  grid-template-columns: repeat(2, 100px);
  gap: 10px;
}
# 1_CSS_Flexbox
CSS Flexbox (Flexible Box Layout) is a one-dimensional layout system used to arrange items in a row or column. It helps align, space, and distribute elements easily.

Example:

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
}
Output
[Item 1]  [Item 2]  [Item 3]

# 2_CSS_Media Queries
CSS Media Queries are used to apply different styles for different screen sizes or devices. They help make websites responsive.

Example:
body {
  background-color: lightblue;
}

/* For screens 600px or smaller */
@media (max-width: 600px) {
  body {
    background-color: lightgreen;
  }
}

# 3_CSS_Clone Landing Page
A CSS Clone Landing Page is the process of recreating the design of an existing website's landing page using HTML and CSS. It helps practice layouts, Flexbox, Grid, responsive design, colors, fonts, and spacing.

Example:

.hero {
  height: 100vh;
  background: #4CAF50;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

button {
  padding: 10px 20px;
  border: none;
  background: white;
  color: green;
  cursor: pointer;
}

# 4_CSS_GRID
CSS Grid is a two-dimensional layout system used to arrange elements in rows and columns. It is useful for creating complex and responsive web page layouts.

Example:

.container {
  display: grid;
  grid-template-columns: repeat(2, 100px);
  gap: 10px;
}
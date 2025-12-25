# SVG Maker
This tool uses jQuery to help preview the contents of an SVG markup. CSS is mostly visual and does not affect functionality.

## HTML
- `txtWidth`: input tag with type `number`. Min 50.
- `txtHeight`: input tag with type `number`. Min 50.
- `txtCode`: textarea tag.
- `txtGrid`: input tag with type `number`. Min 0.
- `cbAppend`: input tag with type `checkbox`.
- 6 button tags with no ids, for inserting template objects.
- `btnPreview`: button tag.
- `svgResult`: SVG tag.

## JavaScript
- `renderSvg()`: Runs when page is loaded, and when `btnPreview` is clicked.
  - Uses the values of `txtWidth` and `txtHeight` to determine the width and height of `svgPreview`.
  - Uses the value of `txtGrid` to draw a grid, only if the value is above 0.
    - Via a `For` loop, draw horizontal lines with spacing between them equal to `txtGrid`'s value in pixels.
    - Via a `For` loop, draw vertical lines with spacing between them equal to `txtGrid`'s value in pixels.
  - Uses the valus of `txtCode` to determine the XML markup of `svgResult`.
- `getDefaultNode(nodeType)`: Returns a XML string based on `nodeType`.
- `addNode(nodeType)`: Runs when one of the buttons is clicked.
  - calls `getDefaultNode()`, passing in `nodeType` as an argument.
  - depending on whether `cbAppend` is checked, the XML string is either appended or prepended to the content in `txtCode`.
  - calls  `renderSvg()`.

 *Note*: Replacing the XML content of an SVG is not straightforward. First, we have to replace the HTML content with itself, *then* replace the content.

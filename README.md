# SVG Maker (TBA)
This tool uses jQuery to help preview the contents of an SVG markup. CSS is mostly visual and does not affect functionality.

## HTML
- `txtWidth`: input tag with type `number`.
- `txtHeight`: input tag with type `number`.
- `txtCode`: textarea tag.
- `btnPreview`: button tag.
- `svgResult`: SVG tag.

## JavaScript
- `renderSvg()`: Runs when page is loaded, and when `btnPreview` is clicked.
  - Uses the values of `txtWidth` and `txtHeight` to determine the width and height of `svgPreview`.
  - Uses the valus of `txtCode` to determine the XML markup of `svgResult`.

 *Note*: Replacing the XML content of an SVG is not straightforward. First, we have to replace the HTML content with itself, *then* replace the content.

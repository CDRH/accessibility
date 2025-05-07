# Checklist: Responsive Design and Zoom

## Responsive Design

- Forms **SHOULD** reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
- Images **SHOULD** reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
- Objects/plugins **SHOULD** reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
- Tables **SHOULD** reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
- Text **SHOULD** reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
- UI components **SHOULD** reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
- Video elements **SHOULD** reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
- Features of the  _content_ MAY be simplified, reduced in size, or eliminated when magnified or when viewed on small viewports.
- Features of the  _interface_ **SHOULD** be simplified, reduced in size, or eliminated when magnified or when viewed on small viewports.

## Zoom

- Text resize/zoom: 
  - The page **SHOULD** be functional when only the text is magnified to 200% of its initial size. 
  - The page **SHOULD** be readable when only the text is magnified to 200% of its initial size. 
  - The spacing between letters, words, lines of text, and paragraphs <mark>**MUST**</mark> be adjustable without loss of content or functionality.
- Content reflow: Content <mark>**MUST NOT**</mark> require scrolling in two directions (both vertically and horizontally)—even when the viewport is set or zoomed to 320 CSS pixels wide (for vertically-scrolling content) or 256 CSS pixels high (for horizontally-scrolling content)—unless both scrolling directions are essential to the usage or meaning of the content.
- Mobile zoom: The page <mark>**MUST**</mark> allow users to zoom in on mobile devices.
- Magnification visual quality: Text **SHOULD** magnify losslessly, or with minimal visual degradation, to retain readability. - Icons and graphics **SHOULD** magnify losslessly, or with minimal visual degradation.

## Orientation

- Content <mark>**MUST NOT**</mark> restrict its view and operation to a single display orientation, such as portrait or landscape, unless a specific display orientation is essential.

## Target Size

- The click/touch target size **SHOULD** be large enough to facilitate easy use with a finger, without risking activating an adjacent link or button.


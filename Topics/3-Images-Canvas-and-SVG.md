# Checklist: Images, Canvas, and SVG

## Image Alt Text

### Informative Images

- Images that convey content <mark>**MUST**</mark> have programmatically-discernible alternative text.
- The alternative text for informative images <mark>**MUST**</mark> be meaningful (accurately conveying the purpose of the image and the author's intent in a way that is useful to those who cannot see the image).
- Alternative text **SHOULD NOT** include words that identify the element as a graphic or image.
- The length of the alternative text for informative images **SHOULD** be concise (no more than about 250 characters).

### Decorative or Redundant Images

- Images that do not convey content, are decorative, or are redundant to content that is already conveyed in text <mark>**MUST**</mark> be given null alternative text (`alt=""`), ARIA `role="presentation"`, or implemented as CSS backgrounds.

### Actionable Images

- All actionable images (e.g., links, buttons, controls) <mark>**MUST**</mark> have alternative text.
- The alternative text for actionable images <mark>**MUST**</mark> be meaningful (accurately conveying the purpose or result of the action).
- Alternative text **SHOULD NOT** include words that identify the element as a link, graphic, or image.
- The length of the alternative text for actionable images **SHOULD** be concise (no more than about 250 characters).

### Form Inputs `type="image"`

- Form inputs with `type="image"` <mark>**MUST**</mark> have alternative text.
- The alternative text for form inputs with `type="image"` <mark>**MUST**</mark> accurately convey the purpose or result of the input action.
- The length of the alternative text for inputs with `type="image"` **SHOULD** be concise (no more than about 250 characters).

### Animated Images

- A method <mark>**MUST**</mark> be provided to pause, stop, or hide any prerecorded video-only content that begins playing automatically and which lasts more than 5 seconds.
- Animated images <mark>**MUST NOT**</mark> flash or flicker more than 3 times per second.

### Complex Images - Extended Descriptions

- Complex images <mark>**MUST**</mark> be briefly described using alt text AND <mark>**MUST**</mark> have a more complete long description.
- The long description (or a link or button to access the long description) **SHOULD** be visible to sighted users.
- The long description **SHOULD** be programmatically associated with the image.

### Images of Text

- An image <mark>**MUST NOT**</mark> include informative text if an equivalent visual presentation of the text can be rendered using real text.
- Images <mark>**MUST NOT**</mark> include informative text, unless the text is essential (such as a logo), or the font, size, color, and background are customizable.

### CSS Background Images

- Purely decorative or redundant CSS images **SHOULD NOT** have a text alternative in the HTML content.
- The alternative text for informative or actionable CSS images <mark>**MUST**</mark> be available as programmatically-discernible text in the HTML content. 
- The alternative text (in the HTML content) for informative or actionable CSS images <mark>**MUST**</mark> adequately and accurately describe the purpose of the image.

### Image Maps

- The alternative text for the `<img>` of a client-side image map <mark>**MUST**</mark> be available as programmatically- discernible text.
- The alternative text for the `<img>` element of a client-side image map <mark>**MUST**</mark> be meaningful (accurately describing the purpose or author's intent in a way that is useful to people who cannot see the image).
- The length of the alternative text for the `<img>` element of client-side image maps **SHOULD** be concise (no more than about 250 characters).
- The alternative text for the `<area>` of a client-side image map <mark>**MUST**</mark> be available as programmatically- discernible text.
- The alternative text for the actionable `<area>` element of a client-side image map <mark>**MUST**</mark> be meaningful (accurately describing the purpose or result of the action in a way that is useful to people who cannot see the image).
- The length of the alternative text for the `<area>` element of client-side image maps **SHOULD** be concise (no more than about 250 characters).
- Server-side image maps **SHOULD NOT** be used when a client-side image map (or other method) can accomplish the same functionality.

## SVG

### SVG as img src

- All SVG `<img>` elements **SHOULD** be set to `role="img"`.
- All informative or actionable SVG `<img>` elements <mark>**MUST**</mark> have meaningful, concise alternative text (via alt, `aria-label`, or `aria-labelledby`).

### Inline SVGs

- All `<svg>` elements <mark>**MUST**</mark> be set to `role="img"`.
- All informative or actionable `<svg>` elements <mark>**MUST**</mark> have meaningful alternative text (via the `<title>` element).
- The alternative text (`<title>`) of an `<svg>` element <mark>**MUST**</mark> be programmatically associated with the `<svg>` element via `aria-labelledby`.
- All text within the image that needs to be spoken by a screen reader <mark>**MUST**</mark> be associated with the `<svg>` element using `aria-labelledby`.
- The total number of characters of alt text associated with the `<svg>` element **SHOULD NOT** exceed 250 characters.

### Embedded SVGs

- SVG **SHOULD NOT** be embedded via `<object>` or `<iframe>`.

### Complex Alternative Text

- Complex `<svg>` images <mark>**MUST**</mark> have meaningful, concise alternative text AND <mark>**MUST**</mark> have a more complete long description.
- A `<desc>` element <mark>**MUST**</mark> be used to provide a detailed description of a complex `<svg>` if it is not provided in any other way.
- The `<desc>` attribute of an `<svg>` element <mark>**MUST**</mark> be programmatically associated with the `<svg>` element (via `aria-labelledby`).
- The length of all associated alternative text (including `<title>` and `<desc>`) for the `<svg>` element **SHOULD** be concise (no more than about 250 characters).

### Text in SVGs

- Text within `<svg>` elements **SHOULD** be eliminated OR **SHOULD** be kept to a minimum.
- All informative `<text>` elements inside `<svg>` elements <mark>**MUST**</mark> be referenced in the alternative text of the `<svg>` element, or in a long description.

### SVG Color Contrast

- SVG images **SHOULD** include a base background color behind the important parts of the image, at a minimum.
- SVG images **SHOULD** be styled to ensure compatibility with Windows High Contrast Mode

### Animated SVG Content

- SVG animations **SHOULD** use JavaScript, rather than the `<animate>` element.
- SVG animations <mark>**MUST**</mark> not flash or blink at a rate of 3 times per second or more.
- SVG animations <mark>**MUST NOT**</mark> auto-play for more than 5 seconds.
- SVG animations <mark>**MUST**</mark> allow users to pause the animation.
- SVG animations **SHOULD NOT** distract the user from the main purpose of the web content.

### Interactive SVGs

- Interactive `<svg>` objects <mark>**MUST**</mark> be fully keyboard- accessible.
- Interactive `<svg>` objects <mark>**MUST**</mark> be fully touchscreen-accessible.
- Interactive `<svg>` objects <mark>**MUST**</mark> communicate the applicable name, role, and value of controls, events, and semantic elements within the `<svg>` object.

## Icon Fonts

- Informative icon fonts without accompanying visible text **SHOULD** be assigned `role="img"`.
- Informative icon fonts without accompanying visible text <mark>**MUST**</mark> have a text alternative.
- Actionable icon fonts without accompanying visible text <mark>**MUST**</mark> have a text alternative.
- The alternative text for informative icon fonts <mark>**MUST**</mark> be meaningful.
- Decorative or redundant icon fonts **SHOULD** be set to `aria-hidden="true"`.

## HTML 5 `<canvas>`

- When `<canvas>` elements are used to display graphics, they <mark>**MUST**</mark> be assigned `role="img"`.
- All `<canvas>` elements <mark>**MUST**</mark> have a text alternative.
- The alternative text for `<canvas>` elements <mark>**MUST**</mark> be meaningful.
- All `<canvas>` elements with complex images <mark>**MUST**</mark> have a detailed text alternative.
- All `<canvas>` elements **SHOULD** have a background fill.
- If text is required in a graphic, it MAY be more appropriate to use SVG instead of `<canvas>`.
- A `<canvas>` element operable with mouse <mark>**MUST**</mark> also be keyboard accessible.

## Multimedia

- All prerecorded video <mark>**MUST**</mark> have synchronized captions.
- Prerecorded audio MAY have synchronized captions.
- All live video with dialog and/or narration <mark>**MUST**</mark> have synchronized captions.
- Live audio consisting mainly of dialog and/or narration **SHOULD** have synchronized captions.
- All prerecorded video and audio <mark>**MUST**</mark> have text transcripts.
- Videos <mark>**MUST**</mark> include audio descriptions of important visual content that is not conveyed through the audio.

## Plug-ins

- All `<object>` elements <mark>**MUST**</mark> have alternative text.
- A full-featured HTML alternative **SHOULD** be provided for Silverlight and Flash objects.
- Accessible Silverlight and Flash objects <mark>**MUST**</mark> use the accessibility API.
- Silverlight and Flash objects <mark>**MUST**</mark> adhere to basic content accessibility principles.
- Silverlight and Flash objects <mark>**MUST**</mark> adhere to multimedia accessibility principles.
- Silverlight and Flash objects <mark>**MUST**</mark> adhere to basic interactive accessibility principles.

## Documents

- An HTML version of non-HTML content **SHOULD** be made available to users.
- Non-HTML documents <mark>**MUST**</mark> adhere to basic accessibility principles.
- PDF files <mark>**MUST**</mark> be in tagged PDF format.
- EPUB files <mark>**MUST**</mark> adhere to HTML accessibility principles, and the accessibility principles of any other technologies used within the EPUB document.
- EPUB files **SHOULD** be in EPUB 3 format.
- EPUB documents **SHOULD** adhere to the additional accessibility principles in the EPUB Accessibility specification.


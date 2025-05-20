# Omeka S Accessibility
Guides and Documentation:
- [Page Title and Headings in Omeka S](#)
- [Image alt text in Omeka S](#)
- [Image alt text best practices](#)

## Page Editor Checklist
Refer to this checklist when creating Simple Pages or other content that uses the block editor.

### Page title and headings

- Page title
 - [ ]`Title` should be concise and unique to the page content. 
   - Omeka S will use this for the page's `<title>` along with the site title; this is what shows up as the title of your browser tab or window.
- Headings
  - [ ] The page must have one Heading 1 (`<h1>`) that serves as the page title. 
    - Add the `<h1>` to the body of the page using either a Page Title Block, a Heading Block, or an HTML Block.
    - The `<h1>` should either match the `Title` or closely correspond to it. For example, when a page title needs to be long, you can put the full title in the `<h1>` and use a more concise version for `Title`.
    - Avoid having multiple Heading 1 (`<h1>`)s.
  - [ ] Use real headings - not text that is just bolded, enlarged or otherwise styled to mimic a heading.
    - Do not skip levels of headings. For example,  don't follow a Heading 2 (`<h2>`) with a Heading 4 (`<h4>`), because you'd be skipping Heading 3 (`<h3>`).
    - Do not use headings for styling purposes. Only use headings for actual heading text. If you need text to be larger or smaller, use the CSS `font-size:` property. If you need non-heading text to be bold, wrap the text in HTML `<strong>` tags or use the CSS `font-weight:` property.

### Text formatting

- Blockquotes
  - [ ] Blockquotes should not be used for indentation or font style purposes. If you need to indent text in an HTML Block, use "Increase indent" button in the HTML editor.
- Lists
  - [ ] Use real, formatted lists (bulleted, numbered, etc.) rather than bare lines of text that have a special character or "1. " typed at the beginning.
- Links
  - [ ] Use meaningful link text rather than bare URLs
      - Good: The [CDRH Accessibility Wiki]() has helpful information about web accessibility.
      - Good: For more information, visit the [CDRH Accessibility Wiki](https://github.com/CDRH/accessibility).
      - Bad: For more information, visit [https://github.com/CDRH/accessibility](https://github.com/CDRH/accessibility).
      - Bad: For more information, [click here](https://github.com/CDRH/accessibility).
- Tables
  - [ ] Make sure tables have a header row at the top (i.e. `<th>`).
  - [ ] Do not use tables for page layout purposes.

### Images, Video, and Audio

- Images
  - [ ] Images must have alt text (`alt="..."`), or follow another accessible method of providing machine-readable alternative text.
  - [ ] Avoid text-in-images when real text on the page will suffice.
  - [ ] Images of scanned documents (with the exception of thumbnails) should be accompanied by transcriptions.
  - [ ] For images that are purely decorative, don't convey content, or contain content that is already conveyed in text, implement them as CSS backgrounds (ask a developer for help) or give them empty alternative text (`alt=""`) and `role="presentation"`.
- Video and Audio
  - [ ] Video files must have captions.
  - [ ] Audio files must have transcriptions.

### Other

- Color contrast
  - [ ] All text—including links and UI elements like menus and buttons, etc.—must meet WCAG 2.1 Color Contrast guidelines. (Use a tool like [WebAIM's Color Contrast Checker](https://webaim.org/resources/contrastchecker/) to test the text color against the background color.)
- Visually hidden elements
  - [ ] To keep text available to screen readers but visually hide it from the page, give it `class="sr-only"`.
    - Use `display: none;` with caution - it will visually hide the text _and_ hide it from screen readers.

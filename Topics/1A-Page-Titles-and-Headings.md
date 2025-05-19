
Related checklist: [Semantic Structure and Navigation](https://github.com/CDRH/accessibility/blob/dev/Checklists/1-Semantic-Structure-and-Navigation.md)


https://github.com/CDRH/accessibility/wiki/CDRH-Accessibility-Wiki
## Page Title

On a typical HTML page, what we think of as the "page title" should usually be set up in two places:
1. In the `<head>` of the HTML document, inside `<title>Title Here</title>` tags
2. In the `<body>` of the HTML document, as a Heading 1 (`<h1>Title Here</h1>`)

The page `<title>` is what your web browser uses for the tab/window title. The `<h1>` is the title text on the page itself. These should correspond, but do not have to match exactly. Since it's particularly important to make the `<title>` concise, you might decide to handle a longer page title by using a shorter version of the page title for the `<title>`, and then using the full, long page title for the `<h1>`.

### Title for Every Page

- The page `<title>` <mark>**MUST**</mark> be present and <mark>**MUST**</mark> contain text.
- The page `<title>` <mark>**MUST**</mark> be updated when the web address changes.
  - This is a concern when something like an AJAX call or a Javascript event changes the content of the page (for example, displaying search results or changing the state of a single-page application).

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Books | Willa Cather Archive</title>
  </head>
  <body>
    <main>
      <h1>Publications in Book Form</h1>
    </main>
```

### Meaningful Page Title

- The page `<title>` <mark>**MUST**</mark> be accurate and informative.
- If a page is the result of a user action or scripted change of context, the text of the `<title>` **SHOULD** describe the result or change of context to the user.
- The `<title>` **SHOULD** be concise.
  - If the `<h1>` for the page is very long, it is standard practice to choose a shorter version for the `<title>`.
- The page `<title>` **SHOULD** be unique, if possible.
  - This is important for helping users of all kinds 
- Unique information **SHOULD** come first in the `<title>`.
  - This also helps users quickly see what page they are on and distinguish between pages
- The page `<title>` **SHOULD** match (or be very similar to) the top heading in the main content.
  - If the `<h1>` for the page is very long, it is standard practice to choose a shorter version for the `<title>`.

## Language

### Primary Language of Page

- The primary language of the page <mark>**MUST**</mark> be identified accurately on the `<html>` element.
  - Every page must have a `lang` attribute inside the `<html>` tag.
- The primary language of the page <mark>**MUST**</mark> be identified with a valid value on the `<html>` element.
  - The HTML `lang` attribute uses [IOS 639-1 Language Codes](https://www.w3schools.com/tags/ref_language_codes.asp), which are two-letter abbreviations for languages. `lang="en"`, for example, tells the browser and/or screen reader that the primary language of the page is English.

Good example:

```
<html lang="en">
```

### Language of Parts within the Page

- Inline language changes <mark>**MUST**</mark> be identified with a valid `lang` attribute.
  - If parts of the page are in a different language than the primary language of the page, 


### Language Codes

- The language code <mark>**MUST**</mark> be valid.
  - Make sure to use one of the official two-letter abbreviations for the language code, not the full name of the language.

## Landmarks

### Creating Landmarks (HTML 5, ARIA)

- Landmarks **SHOULD** be used to designate pre- defined parts of the layout (`<header>`, `<nav>`, `<main>`, `<footer>`, etc.).

### Best Practices for Landmarks

- All text **SHOULD** be contained within a landmark region.
- Multiple instances of the same type of landmark **SHOULD** be distinguishable by different discernible labels (`aria-label` or `aria-labelledby`).
- A page **SHOULD NOT** contain more than one instance of each of the following landmarks: banner, main, and contentinfo.
- The total number of landmarks **SHOULD** be minimized to the extent appropriate for the content.

### Backward Compatibility

- Landmarks **SHOULD** be made backward compatible.

## General UI Components

- In content implemented using markup languages, the purpose of User Interface Components, icons, and regions MAY be programmatically determinable.

## Headings

### Real Headings

- Text that acts as a heading visually or structurally **SHOULD** be designated as a true heading in the markup.
- Text that does not act as a heading visually or structurally **SHOULD NOT** be marked as a heading.

### Meaningful Text

- Headings <mark>**MUST**</mark> be accurate and informative.
- Heading text **SHOULD** be concise and relatively brief.

### Outline/Hierarchy of Content

- Headings **SHOULD** convey a clear and accurate structural outline of the sections of content of a webpage.
- Headings **SHOULD NOT** skip hierarchical levels.

### Heading Level 1 Best Practices

- The beginning of the main content **SHOULD** start with `<h1>`.
- Most web pages **SHOULD** have only one `<h1>`.

## Links

### Designate Links Correctly

- Links <mark>**MUST**</mark> be semantically designated as such.
- Links and buttons **SHOULD** be designated semantically according to their functions.

### Link Text

- A link <mark>**MUST**</mark> have programmatically-discernible text, as determined by the accessible name calculation algorithm.
- The purpose of each link **SHOULD** be able to be determined from the link text alone.
- The link text **SHOULD NOT** repeat the role ("link").
- Features such as labels, names, and text alternatives for content that has the same functionality across multiple web pages <mark>**MUST**</mark> be consistently identified.

### Links to External Sites, New Windows, Files

- A link that opens in a new window or tab **SHOULD** indicate that it opens in a new window or tab.
- A link to a file or destination in an alternative or non-web format **SHOULD** indicate the file or destination type.
- A link to an external site MAY indicate that it leads to an external site.

### Visually Distinguishable from Text

- Links <mark>**MUST**</mark> be visually distinguishable from surrounding text.

### Visual focus indicator

- All focusable elements <mark>**MUST**</mark> have a visual focus indicator when in focus.
- Focusable elements **SHOULD** have enhanced visual focus indicator styles.

## Navigation Between Pages

### Navigation Lists

- A navigation list **SHOULD** be designated with the `<nav>` element or `role="navigation"`.
- A navigation list **SHOULD** include a visible method of informing users which page within the navigation list is the currently active/visible page.
- A navigation list **SHOULD** include a method of informing blind users which page within the navigation list is the currently active/visible page.

### Consistency

- Navigation patterns that are repeated on web pages <mark>**MUST**</mark> be presented in the same relative order each time they appear and <mark>**MUST NOT**</mark> change order when navigating through the site.

## Navigation Within Pages

### Skip Navigation Links

- A keyboard-functional "skip" link **SHOULD** be provided to allow keyboard users to navigate directly to the main content.
- The "skip link" **SHOULD** be the first focusable element on the page.
- A skip link <mark>**MUST**</mark> be either visible at all times or visible on keyboard focus.

### Table of Contents

- A table of contents for the page MAY be included at the top of the content or in the header.
- If a table of contents for the page is included, it
SHOULD reflect the heading structure of the page.

### Reading Order and Tab/Focus Order

- The reading order <mark>**MUST**</mark> be logical and intuitive.
- The navigation order of focusable elements <mark>**MUST**</mark> be logical and intuitive.
- tabindex of positive values **SHOULD NOT** be used.

### Paginated Views

- A paginated view **SHOULD** include a visible method of informing users which view is the currently active/visible view.
- A paginated view **SHOULD** include a method of informing blind users which view is the currently active/visible view.

### Single-Key Shortcuts

- If a single-character-key shortcut exists, then at least one of the following <mark>**MUST**</mark> be true: single-character-key shortcuts can be turned off, remapped, or are only active when the relevant user interface component is in focus.

## Tables

### Semantic Markup for Tabular Data

- Tabular data **SHOULD** be represented in a `<table>`.

### Table caption/name

- Data tables **SHOULD** have a programmatically-associated caption or name.
- The name/caption of a data table **SHOULD** describe the identity or purpose of the table accurately, meaningfully, and succinctly.
- The name/caption of each data table **SHOULD** be unique within the context of other tables on the same page.

### Table Headers

- Table headers <mark>**MUST**</mark> be designated with `<th>`.
- Data table header text <mark>**MUST**</mark> accurately describe the category of the corresponding data cells.

### Simple Header Associations

- Table data cells <mark>**MUST**</mark> be associated with their corresponding header cells.

### Grouped Header Associations

- Table data group headers <mark>**MUST**</mark> be associated with their corresponding data cell groups.

### Complex Header Associations

- Header/data associations that cannot be designated with `<th>` and scope <mark>**MUST**</mark> be designated with headers plus id.

### Nested or Split Tables

- Data table headers and data associations <mark>**MUST NOT**</mark> be referenced across nested, merged, or separate tables.

### Table Summary

- A summary MAY be provided for data tables.
- A data table summary, if provided, **SHOULD** make the table more understandable to screen reader users.

### Layout Tables

- Tables **SHOULD NOT** be used for the purpose of purely visual (non-data) layout.
- Layout tables <mark>**MUST NOT**</mark> contain data table markup.

## Lists

### Semantic Markup for Lists

- Lists <mark>**MUST**</mark> be constructed using the appropriate semantic markup.

## Iframes

### Frame titles

- Iframes that convey content to users <mark>**MUST**</mark> have a non-empty title attribute.
- The iframe title <mark>**MUST**</mark> be accurate and descriptive.
- Frames <mark>**MUST**</mark> have a unique title (in the context of the page).

### Page Title Within an Iframe

- The source page of an iframe <mark>**MUST**</mark> have a valid, meaningful `<title>`.

### Semantic structure across iframes

- The heading hierarchy of an iframe **SHOULD** be designed to fit within the heading hierarchy of the parent document, if possible.

### Hiding iframes that don't contain meaningful content

- Hidden frames or frames that do not convey content to users **SHOULD** be hidden from assistive technologies using `aria-hidden="true"`.

## Other Semantic Elements

### `<strong>` and `<em>`

- Critical emphasis in the text **SHOULD** be conveyed through visual styling.
- Critical emphasis in the text **SHOULD** be conveyed in a text-based format.

### `<blockquote>` and `<q>`

- The `<blockquote>` element **SHOULD** be used to designate long (block level) quotations.
- The `<blockquote>` element **SHOULD NOT** be used for visual styling alone.
- The `<q>` element (for inline quotations) **SHOULD NOT** be used as the only way to designate quotations.

### `<code>`, `<pre>`

- Code **SHOULD** be marked with the `<code>` element and styled to look different from non-code text.
- Blocks of code **SHOULD** be formatted with the `<pre>` element.

### Strikethrough/Delete and Insert

- Strikethrough text **SHOULD** be marked with the `<del>` element.
- Critical strikethrough text <mark>**MUST**</mark> be supplemented with a text-based method to convey the meaning of the strikethrough.
- Text designated for insertion **SHOULD** be marked with the `<ins>` element.
- Critical text designated for insertion <mark>**MUST**</mark> be supplemented with a text-based method to convey the meaning of the insertion.

### Highlighting (`<mark>`)

- Highlighted text **SHOULD** be marked with the `<mark>`element.
- Critical highlighted text **SHOULD** be supplemented with a text-based method to convey the meaning of the highlighting.

## Parsing and Validity

### Complete Start and End Tags

- In content implemented using markup languages, elements <mark>**MUST**</mark> have complete start and end tags.

### Conflicts and duplicates

- IDs <mark>**MUST**</mark> be unique within a web page.
- Names, when provided, of block level elements (e.g.landmarks, tables, iframes, etc.) **SHOULD** be unique within a web page.

### Parent-child relationships

- Markup **SHOULD** adhere to required parent-child relationships of elements and attributes.

### Deprecated Markup

- Deprecated markup **SHOULD NOT** be used.


# Skip to Main Content link

A "Skip to Main Content" link allows screen reader users to skip the header content they would otherwise have to hear on every page, such as the site title and main navigation menu. The following is custom HTML and CSS that can be used on any of our sites.

## HTML for the link

In the `.html` file, place this code inside the `<header>` before any other content (site title and navigation should come after this link). If there is no `<header>` landmark, you can place it inside the `<main>` landmark (or `<div role="content">); make sure it precedes all other content on the page.

```
<a class="sr-only sr-only-focusable skip-link" href="#main_content">Skip to main content</a>
```

### Link target

When the user clicks the link above, it will take them to an element on the same page with `id="main_content"`. It is best to put `id="main_content"` on the `<main>` landmark:

```
<main id="main_content">
```

However, HTML elements can only have 1 `id`. If the `<main>` landmark already has an `id` and you don't want to override that, you can create a `div` inside it with `id="main_content"`, and move all the content that was inside `<main>` inside the `<div id="main_content,"`:

```
<main id="main">
  <div id="main_content">
    ...
  </div>
</main>
```

## CSS 

The following CSS will keep the Skip to Main Content visually hidden (unless the user navigates to it with a keyboard) without hiding it from screen readers.

```
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}

.sr-only-focusable:active, .sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
```

Depending on the site's existing CSS, the default link color may not work well against the background. Feel free to include this CSS, as well, and customize the colors. Be sure they meet WCAG 2.1's minimum color contrast ratios; this link is meant to benefit keyboard-only users as well as screen reader users, so visual contrast matters.

```
a.s:hover, a.sr-only-focusable:focus {
  background-color: white;
  color: #345c87;
}
```

## Test

To test a Skip to Main Content link, use the `tab` key to cycle through the links and other focusable elements on a page. (Use `shift + tab` to go backward in the order.) The Skip to Main Content link should be at the top of the order, before any other links or focusable elements on the page.

Another way to test this in Firefox is to use the built-in [Accessibility Inspector](https://firefox-source-docs.mozilla.org/devtools-user/accessibility_inspector/) to [show the tab order](https://firefox-source-docs.mozilla.org/devtools-user/accessibility_inspector/). Links and other focusable elements will be numbered from start to finish, making it easy to do a quality check on both the Skip to Main Content link and other things on the page.

# Omeka S
While much of the accessibility training will happen behind the scenes in the framework, users will still need to code individual items correctly. 

In order to meet government standards, we are aiming for WCAG 2.2 AA.
## Basics
- [Core concepts](../Core-Concepts.md)
- Headings are real headings
- Logical reading order
- Color contrast (use a contrast checker)
- Try to avoid images of text, if they can't be avoided transcribe/provide alt text
## Tools
- WCAG color contrast checker
## Page Titles
- Should be unique and descriptive
- A standard is that the name of the page is first and the site title (if included) is after
	- This will make it so that users can see the tabbed content
- General rule of thumb is the `<title>` tag will match `<h1>` and sometimes add the site title
	- But sometimes you might want a shorter version in `<title>` 
- Keep an eye on this and let the development team know if the `<title>` doesn't look right
## Headings
- For many sites, the `<h1>` is the name of the site
- But it can also make sense for the `<h1>` is the title of the page
- Avoid multiple `<h1>`
- Use "real" headings `<h1>` `<h2>` `<h3>` `<h4>` etc not `<div class="heading">`
## Other HTML
- Everything on [Core concepts](../Core-Concepts.md)
- Tables are rather complex, you need to mark headers, etc. 
- HTML copy and pasted from Microsoft Word or other GUI applications may or may not be accessible
- When in doubt, ask a front end designer
## Alt tags
- More info coming
- todo: compile a list all the places where alt text is added to the images
## Helper classes 
- We will develop standard helper classes, but in the meantime keep track of what you need styled, apply unique classes, and ask the developers to style the text (e.g. bylines, etc)
## Embeds
- An Omeka S default is to not allow embeds, we will need to uncheck the "Use HTML Purifier" options in settings for this to work


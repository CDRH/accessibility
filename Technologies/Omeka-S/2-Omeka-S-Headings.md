## Page Title and Headings

CDRH Omeka S themes handle heading hierarchy differently than the base Omeka S code. This is in keeping with widely-accepted best practices for page titles and `<h1>`s. WebAIM sums it up this way:

> Because the page's first level heading (`<h1>`) 
> should also describe the page content, 
> the page title and the first level heading text 
> are often the same or similar.

By default, Omeka S takes the text you provide in the `Title` field when editing a page or faceted browse, combines it with the site title, and uses it for the page's `<title>` (which is what your browser uses for the tab or window title, and does not appear in the page itself). However, it does not use the `Title` field text for the page's first level heading (`<h1>`), and thus does not follow the best practice described above. Instead, in the base Omeka S code, the site title (in the header of every page) is an `<h1>`, meaning that the `<title>` and `<h1>` _do not_ correspond in with the default site layout. This also means that the first heading in the body of the page, which generally serves as the visible title of the page, has to be an `<h2>` (according to best practices, a well-formed web page should not have multiple `<h1>`s).

The CDRH's custom themes override the base Omeka S code so that the site title (in the header of each page) is _not_ an `<h1>`. This has several benefits:

1. Since the site title in the header is now a `<div>` and not an `<h1>`, you can add an `<h1>` to the body of the page that describes _that specific page's topic or content.
2. The page's `<title>` and `<h1>` can either match exactly _or_ correlate. For example, if an page needs to have a very long title (for example, the full title of a journal article or essay), you can now put a _shorter_ version of the title in the `Title` field, which will be used in the `<title>`, and then you can put the full title of the page in an `<h1>`.

As a result, those of us who create pages* need to make sure we add an `<h1>` to every page in addition to filling in the `Title` field.

*Faceted Browse does not support additional blocks, so the text in the `Title` field will serve as the `<h1>` of that Faceted Browse page.

Here's a comparison table showing how a page with `Title: About` would be handled differently by CDRH custom themes:

|                              | Omeka S Default       | CDRH Theme                                                                                                                            |
|------------------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `<title>`                      | About \| Nebraskaland | About \| Nebraskaland  <br>_Same as Omeka S Default_                                                                                      |
| First-level heading (`<h1>`) | Nebraskaland          | _Fully customizable. Should match or correspond to_ `<title>`_. <br>Examples: "About," "About Nebraskaland," "About Nebraskaland Magazine", etc._ |

### How to add an `<h1>` to a page

There are two ways to set up the `<h1>` for your page using page blocks:

#### Option 1: Page Title Block

You can use this block (which is added to new pages by default) if your `<title>` and `<h1>` will be exactly the same. It does not offer any styling options, so it will use the theme's template and CSS.

#### Option 2: Heading Block

Put the text for your page `<title>` in the text box, and choose radio button `1`. 

If you click the gear icons, you can add a CSS class to the heading.

#### Option 2: HTML Block

Inside the HTML block, type in your page title, highlight it, and select `Heading 1` from the first dropdown menu.

This is the only option that will allow you to italicize words in the page title. You can use the _I_ button in the text editor to italicize what you need.

If you click Source, you can edit the code surrounding the `<h1>` - for example, if you need to add an `id`, CSS `class`, or another attribute.

#### Note about Faceted Browse

The 
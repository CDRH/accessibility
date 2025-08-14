# Omeka S template overrides for WCAG 2.1 Level AA compliance

## view/faceted-browse/site/page/facets.phtml

This template needs to be overriden to fix a **critical** WCAG 2.1 Level AA violation - 
form elements MUST have labels. As of 2025-08-14, Faceted Browse does not assign a label 
to the "Full Text" facet. Until this changes, we will need to override this partial for
each of our Omeka S sites.

To bring Faceted Browse pages into compliance, copy the contents of the 
[facets.phtml](https://github.com/omeka-s-modules/FacetedBrowse/blob/main/view/faceted-browse/site/page/facets.phtml) 
file from the Faceted Browse module's GitHub repository. Create a facets.phtml file for the 
theme you're working on and paste in the contents. In the theme files, it should be located 
in the folder `/view/faceted-browse/site/page/`.

Paste in the contents of the module's `facets.phtml` file. Find the line 
(~[line 34](https://github.com/omeka-s-modules/FacetedBrowse/blob/39973b23f57864c2a5f606d3d39103dfb1f6dd18/view/faceted-browse/site/page/facets.phtml#L34))
that says

`<?php echo $this->facetedBrowse()->renderFacet($facet); ?>`

...and replace with the following:

``` phtml
<?php if ($facet->type() == "full_text"): ?>
  <label>
    <span class="sr-only"><?php echo $facet->name(); ?></span>
    <?php echo $this->facetedBrowse()->renderFacet($facet); ?>
  </label>
<?php else: ?>
 <?php echo $this->facetedBrowse()->renderFacet($facet); ?>
<?php endif; ?>
```

Then save, commit the new file, and push to the theme GitHub repo.

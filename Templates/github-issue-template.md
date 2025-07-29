# Template for Accessibility Issues
## Steps
  - [ ] Create new issue in product repository
  - [ ] Assign `a11y` label (or `a11y improvements` label for ideas and suggestions for future improvements NOT REQUIRED by ADA Title II)
  - [ ] Assign prioritization label (`Critical`, `Serious`, `Moderate`, or `Minor` - see [prioritization rubric](#prioritization-rubric)) and include in description, as well, in case of label changes
  - [ ] Copy-paste and fill out template below. For guidance on filling out the template, see [Description of fields](#description-of-fields) below.
  - [ ] Add to milestone, if applicable

## Copy-paste into issue

```
## Issue Description



### Impact/Severity


### Link to relevant page(s)
 - 

### Screenshot or Video



---

## For User Interface (UI) or Assistive Technology (AT)-related Issues

### Browser/Technology Used



### Expected Results



## Steps to Reproduce



---

## Remediation Steps (if known)



```

## Prioritization Rubric for Accessibility Issues

| Priority Level            | Description                                                                                                                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Critical               | **Requires an immediate fix.**  Blocks further testing  Is highly visible, occurs on a large number of pages, and/or affects essential site functions                                                            |
| 2. Serious                | **Requires a fix before deadline.**  i.e. all WCAG 2.1 Level AA non-compliant issues that are not site-breaking                                                                                           |
| 3. Moderate               | **Should be fixed before deadline _if_ time permits.** Otherwise, should be fixed promptly after Priority 1 & 2 items for all products are finished (e.g. a “Best Practice” that is highly visible)  |
| 4. Accessibility improvements (`a11y_improvements`)         | **Low priority.**  Non-required potential area of improvement to meet best practices. _Note: this priority level does not have a corresponding priority label. Issues with this priority level should use the `a11y improvements` label. DO NOT use the `a11y` label for low priority issues._                                                                                                                |

### Corresponding GitHub Issue labels:

1. `a11y` and `Priority: Critical`
2. `a11y` and `Priority: Serious`
3. `a11y` and `Priority: Moderate`
4. `a11y improvements`, no priority label


## Description of fields
| Template Component  | Description of Component                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descriptive Title   | Provide a descriptive title that identifies the accessibility issue  Describe the bug and/or how it appears on the website                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Issue Description   | Provide a detailed description of the issue  ALWAYS include a link to at least one page where the bug is happening  If you know which file in the site code the bug is arising from, link to that as well  ALWAYS describe steps to reproduce the issue if it involves an interface or interactive component (search tools, buttons, navigation bars, expand/collapse, etc.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Expected Results    | Detail the expected behavior, what a user expects to happen upon interaction with content                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Platform and AT     | Identify the platform and any assistive technology used in discovering the issue                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Impact/Severity     | Identify the level of impact (e.g., Critical, Serious, Moderate, Minor); often used to prioritize and triage fixes   - Critical: The issue results in blocked content for individuals with disabilities. Until a solution is implemented, content will be completely inaccessible, making the organization highly vulnerable to legal action. Remediation should be a top priority.    - Serious: The issue results in serious barriers for individuals with disabilities. Until a solution is implemented, some content will be inaccessible, making the organization vulnerable to legal action. Users relying on Assistive Technology will experience significant frustration when attempting to access content. Remediation should be a priority.    - Moderate: This issue results in some barriers for individuals with disabilities but would not prevent them from accessing fundamental elements or content. This might make the organization vulnerable to legal action. This failure must be resolved before a page can be considered fully compliant.    - Minor: This is considered an issue that yields less impact for users than a moderate issue. For a page to be considered fully compliant this issue must be resolved but can be dealt with last.  |
| Steps to Reproduce  | Include specifics needed to reproduce the issue, including step-by-step instructions and credentials that should be used to reproduce the issue                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Visual or Video     | Provide a screenshot with visual indicators, video recording of the accessibility issue, or even a code snippet of where the issue occurs                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Remediation         | Whenever possible, try to include recommendations for fixing the issue                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |

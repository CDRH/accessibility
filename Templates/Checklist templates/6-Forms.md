# Checklist: Forms Labels, Instructions, and Validation

## Labels

### Semantic Labels

- [ ] Labels <mark>**MUST**</mark> be programmatically associated with their corresponding elements.
- [ ] Labels <mark>**MUST**</mark> be programmatically-discernible.

### Meaningful Label Text

- [ ] Labels <mark>**MUST**</mark> be meaningful.
- [ ] Labels <mark>**MUST NOT**</mark> rely solely on references to sensory characteristics.

### Icons as Labels

- [ ] Icons MAY be used as visual labels (without visual text) if the meaning of the icon is visually self-evident
AND if there is a programmatically-associated semantic label available to assistive technologies.

### Placeholder Text as Labels

- [ ] Placeholder text <mark>**MUST NOT**</mark> be used as the only method of providing a label for a text input.

### Visibility of Labels

- [ ] Labels <mark>**MUST**</mark> be visible.
- [ ] For user interface components with labels that include text or images of text, the name MUSTcontain the text that is presented visually.

### Proximity of Labels to Controls

- [ ] A label **SHOULD** be visually adjacent to its corresponding element.
- [ ] A label **SHOULD** be adjacent in the DOM to its corresponding element.

### Multiple Labels for One Field

- [ ] When multiple labels are used for one element, each label <mark>**MUST**</mark> be programmatically associated with the corresponding element.

### One Label for Multiple Fields

- [ ] When one label is used for multiple elements, the label <mark>**MUST**</mark> be programmatically associated with each of the corresponding elements.

## Group Labels

### Semantic Group Labels

- [ ] Group labels <mark>**MUST**</mark> be programmatically-associated with the group if the individual labels for each element in the group are insufficient on their own.
- [ ] Group labels <mark>**MUST**</mark> be programmatically-discernible.

### Meaningful Group Labels

- [ ] Group labels <mark>**MUST**</mark> be meaningful.
- [ ] Group labels <mark>**MUST NOT**</mark> rely solely on references to sensory characteristics.

### Proximity of Group Labels

- [ ] Group labels **SHOULD** be visually adjacent to the grouped elements.
- [ ] Group labels **SHOULD** be adjacent in the DOM to the grouped elements.

### Visibility of Group Labels

- [ ] Group labels <mark>**MUST**</mark> be visible.

## Instructions & Other Helpful Info

### Instructions for Forms, Groups, and Sections

- [ ] Instructions for groups or sections **SHOULD** be programmatically-associated with the group.
- [ ] Instructions for groups or sections <mark>**MUST**</mark> be programmatically-discernible.
- [ ] Instructions for groups or sections <mark>**MUST**</mark> be meaningful.
- [ ] Instructions for groups or sections <mark>**MUST**</mark> be visible.
- [ ] Instructions for groups or sections **SHOULD** be visually adjacent to the grouped elements.
- [ ] Instructions for groups or sections **SHOULD** be adjacent in the DOM to the grouped elements.
- [ ] If the instructions for groups or sections are not critical, the instructions **MAY** be hidden until the user requests them.
- [ ] Instructions for groups or sections <mark>**MUST NOT**</mark> rely solely on references to sensory characteristics.

### Instructions for Inputs

- [ ] Instructions for an element <mark>**MUST**</mark> be programmatically-associated with the element.
- [ ] Instructions for an element <mark>**MUST**</mark> be available as programmatically-discernible text.
- [ ] Instructions for an element <mark>**MUST**</mark> be meaningful.
- [ ] Instructions for an element <mark>**MUST**</mark> be visible.
- [ ] Instructions for an element **SHOULD** be visually adjacent to the element.
- [ ] Instructions for an element **SHOULD** be adjacent in the DOM to the element.
- [ ] If the instructions for an element are not critical, the instructions MAY be hidden until the user requests them.
- [ ] Instructions for an element <mark>**MUST NOT**</mark> rely solely on references to sensory characteristics.

### Required Fields

- [ ] Required fields **SHOULD** be programmatically designated as such.
- [ ] Required fields **SHOULD** have a visual indicator that the field is required.
- [ ] The form validation process <mark>**MUST**</mark> include an errormessage explaining that a field is required if the field isn't identified as required both visually and programmatically in the form's initial state.

### Input Purpose

- [ ] The purpose for each common input field that collects an individual's personal data <mark>**MUST**</mark> be programmatically defined based on the list of 53
Input Purposes for User Interface Components.

## Dynamic Forms & Custom Widgets

### Changes in Context

- [ ] Focusing on an element <mark>**MUST NOT**</mark> automatically trigger a change of context, unless the user has been adequately advised ahead of time.
- [ ] Changing an element's value <mark>**MUST NOT**</mark> automatically trigger a change of context, unless the user is adequately advised ahead of time.
- [ ] Hovering over an element with the mouse <mark>**MUST NOT**</mark> automatically trigger a change of context, unless the user has been adequately advised ahead of time.

### Custom Form Inputs

- [ ] Native HTML form elements **SHOULD** be used whenever possible.
- [ ] Custom form elements **SHOULD** act like native HTMLform elements, to the extent possible.
- [ ] Custom form elements **SHOULD** have appropriate names, roles, and values.
- [ ] Updates and state changes that cannot be communicated through HTML or ARIA methods
SHOULD be communicated via ARIA live messages.

## Form Validation

### Error Identification Considerations

- [ ] Error feedback **SHOULD** be made available immediately after form submission (or after an equivalent event if there is no form submission event).
- [ ] Error feedback <mark>**MUST**</mark> be programmatically- associated with the appropriate element.
- [ ] Error feedback <mark>**MUST**</mark> be programmatically- discernible.
- [ ] Error feedback <mark>**MUST**</mark> be meaningful.
- [ ] Error feedback <mark>**MUST**</mark> be visible.

### Success Confirmation Considerations

- [ ] Success confirmation feedback **SHOULD** be programmatically-discernible.
- [ ] Success confirmation feedback **SHOULD** be meaningful.
- [ ] Success confirmation feedback <mark>**MUST**</mark> be visible.


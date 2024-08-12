### CSS Specificity
If there are two or more CSS rules that point to the same element, the selector with the highest specificity value will "win", and its style declaration will be applied to that HTML element.

## Specificity Hierarchy
1. Inline styles - Example: <h1 style="color: pink;">
2. IDs - Example: #navbar
3. Classes, pseudo-classes, attribute selectors - Example: .test, :hover, [href]
4. Elements and pseudo-elements - Example: h1, ::before

### How to Calculate Specificity?
Start at 0, add 100 for each ID value, add 10 for each class value (or pseudo-class or attribute selector), add 1 for each element selector or pseudo-element.
# Note: Inline style gets a specificity value of 1000, and is always given the highest priority!
# Note 2: There is one exception to this rule: if you use the "!important" rule, it will even override inline styles!


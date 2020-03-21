# 3 Pillars of Writing Good HTML and CSS
  1. Responsive Design
  2. Maintainable and Scalable
  3. Web Performance

### Responsive Design
  - Fluid layouts
  - Media queries
  - Responsive images
  - Correct units
  - Desktop-first vs. Mobile-first 

### Maintainable and Scalable
  - Clean
  - Easy-to-understand
  - Encourages growth
  - Reusable
  - Good file structure and organization
  - Good naming conventions
  - Good HTML structure

### Web Performance
  - Less HTTP requests
  - Less code
  - Compress code
  - Less images
  - Compress images

## How CSS works behind the scenes
After the CSS is loaded, it is parsed. The first step in parsing
is to resolve conflicting CSS declarations. Then, the final CSS values
are parsed. This includes parsing relative and percentage-based values
that are specific to the users' device.

The CSS is then stored in the CSS Object Model (CSSOM), which is similar in structure
to the DOM. The CSSOM and the DOM are then placed in the render tree.
Finally, the visual formatting model combines everything for the site to
be rendered on the device. 

### How CSS is Parsed 
![CSS Rule Diagram](./img/CSS%20Rule.png)

#### What does "Cascade" actually mean?
It's the process of combining different stylesheets and resolving conflicts between different CSS
rules and declarations, when more than one rule applies to a certain element.

There are different CSS declarations that can be made; declarations that we write
in the code are called **author** declarations. When the user changes any CSS through
the browser, these are called **user** declarations. Finally, there are
**browser (user agent)** declarations, these are typically browser default CSS rules.

The cascade step combines all the various CSS declarations from these sources, and
resolves conflicts. But how does this all happen?
![CSS Conflict resolution order](./img/CSS%20conflict%20resolution%20order.png)

Specificity Hierarchy:

![Specificity Hierarchy](./img/Specificity%20Hierarchy.png)

So to summarize everything:
  - CSS declarations marked with `!important` have the highest priority
  - You should only use `!important` as a last resort. Always try to use correct specificity. **This makes your CSS more maintainable**
  - Inline styles will *always* have priority over your styles in external stylesheets
  - ID is more specific than Class, which is more specific than Element selectors.
  - A universal (*) selector has no specificity value. It will *always* be over-written by other selectors
  - Rely on specificity, not order of selectors.
  - However, rely on order when using 3rd-party stylesheets. *Always put your author stylesheet last!*

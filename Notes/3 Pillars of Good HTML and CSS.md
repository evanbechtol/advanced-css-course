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

## Web Performance
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

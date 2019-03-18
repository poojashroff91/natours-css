`Three pillars to write good html / css`
- Responsive design
    - Fluid layouts
    - Media queries
    - Responsive images
    - Correct units
    - Desktop first vs mobile first
- Maintainable and Scalable Code
    - Clean
    - Easy to understand
    - Growth
    - Reusable
    - How to organize files
    - How to name classes
    - How to sctructure HTML
- Web performance
    - Less HTTP requests
    - Less code
    - Compress code
    - Use a CSS preprocessor
    - Less images
    - Compress images

`How CSS works behind the scenes?`

Load HTML -> Parse HTML -> **Document Object Model**

Parse HTML -> Parse CSS -> Resolve conflicts (cascade) -> Process final CSS values -> **CSS Object Model**

Models -> Render tree -> Website rendering the visal formatting model -> **Final rendered website**

`Importance` 
- User **!important** declarations
- Author **!important** declarations
- Author declarations
- User declarations
- Default browser declarations

`Specificity`
- Inline styles
- IDs
- Classes, pseudo classes, attribute
- Elements, pseudo-elements

`Source Order`
- The last declaration in the code will apply

`CSS Value Processing`
- Each property has an initial value, used if nothing is declared.
- Browsers specify a **root** `font-size` for each page (usually 16px).
- Percentages and relative values are always converted to pixels
- Percentages are measured relative to their parent's **font-size** if used to specify `font-size`
- Percentages are measured relative to their parent's **width** if used to specify lengths
- `em` are measured relative to their **parent** `font-size` if used to specify `font-size`
- `em` are measured relative to their **current** `font-size` if used to specify lengths
- `rem` are always measured relative to the **document's root** `font-size`
- `vh` and `vw` are simply percentage measurements of viewport's `height` and `width`

`Inheritance`
- Inheritance passes the value for some specific properties from parents to children - **more maintainable code**
- Properties related to text are inherited: `font-family`, `font-size`, `color`
- The computed value of a property is what gets inherited, not the declared value.
- Inheritance of a property only works if no one declares a value for that property
- The `inherit` keyword forces inheritance on a certain property
- The `initial` keyword resets a propert to its initial value.
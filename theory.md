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

`Visual formatting model`
- Algorithm that calculates boxes and determines the layout of these boxes, for each element in the render tree, in order to determine the final layout of the page.
- Dimensions of boxes - Box Model
- Box type - Inline
- Positioning scheme
- Stacking contexts

`Box model`
- Each box in CSS has width, height, padding, border, margin
- Content - text, images, etc. 
- Padding - transparent area around the content, inside of the box
- Border - goes around the padding and the content
- Margin - space between boxes
- Fill area - area that gets filled with background color or background image, doesn't include the margin
- Box sizing : `border-box` The height and the width will be calculated with the padding and border included. So whatever is defined will be the actual height and weight.

`Box types`
- `display` property decides the type of the box
- Block level boxes
    - Elements formatted visually as blocks
    - 100% of parent's width
    - Vertically, one after another
    - Box model applies as shown
    - Default setting
-Inline-block boxes
    - A mix of block and inline
    - Occupies only content's space
    - No line-breaks
    - Box model applies as shown 
- Inline boxes
    - Content is distributed in lines
    - Occupies only content's space
    - No line breaks
    - No heights and widths
    - Paddigns and margins only horizontal (left and right)

`Positioning schemes`
- Normal flow
    - Default positioning scheme
    - Not floated
    - Not absolutely positioned
    - Elements laid out as per their source order
- Floats
    - Element is removed from the normal flow
    - Text and inline elements will wrap around the floated element
    - The container will not adjust its height to the element - need to use clear fixes
- Absolute positioning
    - Element is removed from the normal flow
    - No impact on surrounding content or elements
    - We use top, bottom, left and right to offset the element from its relatively positioned container.

`Stacking context`
- In which order will the elements be rendered on a page.
- The one with the higher z-index appears on the top and the lower z-index appears on the bottom

`BEM`
- Block Element Modifier
- Block: standalone component that is meaningful on its own.
- Element: part of a block that has no standalone meaning
- Modifier: a different version of a block or an element.



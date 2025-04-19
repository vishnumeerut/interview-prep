# What is the Difference Between `<div>` and `<span>`?

Both `<div>` and `<span>` are non-semantic HTML elements.

### Key Differences:

1. **Purpose:**
   - **`<div>`**: Used as a block-level container to group elements together. 
   - **`<span>`**: Used as an inline container for text or other inline elements. 

2. **Display Type:**
   - **`<div>`**: A block-level element, meaning it takes up the full width of its parent container and starts on a new line.
   - **`<span>`**: An inline element, meaning it only takes up as much width as necessary and does not force content onto a new line.

3. **Use Cases:**
   - **`<div>`**: Used for grouping large sections of content like headers, articles, and footers, and is helpful for layout purposes.
   - **`<span>`**: Used for styling or modifying smaller portions of text or inline elements, such as changing the color of a word within a paragraph.

### Examples:

#### `<div>` `<span>` Example:
```html
<div>
    <h1>Article Title</h1>
    <p>This is the content of the article.</p>
</div>

<p>This is a <span style="color: red;">highlighted</span> word.</p>

# What is the Difference Between HTML and XHTML?

HTML (HyperText Markup Language) and XHTML (Extensible HyperText Markup Language) are both used to create and structure content on the web, but they have some key differences.

### Key Differences:

1. **Syntax Rules:**
   - **HTML:** More lenient with syntax. Tags can be left unclosed (e.g., `<li>` without `</li>`).
   - **XHTML:** Stricter syntax. Tags must be properly closed (e.g., `<li></li>`), and all tags must be properly nested.

2. **Case Sensitivity:**
   - **HTML:** Tags and attributes are not case-sensitive (e.g., `<title>` or `<TITLE>` are both valid).
   - **XHTML:** Tags and attributes are case-sensitive, and must be written in lowercase (e.g., `<title>` not `<TITLE>`).

3. **Document Structure:**
   - **HTML:** The document structure can be flexible, allowing for errors in tag nesting.
   - **XHTML:** The document structure must be well-formed, meaning no errors are allowed in the nesting or syntax.

4. **Self-closing Tags:**
   - **HTML:** Some tags like `<img>` do not require a closing tag.
   - **XHTML:** All tags, including self-closing tags, must be properly closed with a slash (e.g., `<img />`).

5. **Error Handling:**
   - **HTML:** Browsers are forgiving and can display a page even if there are errors in the code.
   - **XHTML:** Browsers will not render the page if there are errors in the code; it must be well-formed.

### Example:

#### HTML Example:
```html
<img src="image.jpg">
<p>This is a paragraph.</p>

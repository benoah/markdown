# CSS Inline and Block Level Elements

> If you are struggling with understanding the difference between inline and block-level elements, you can think of it this way: an example of an inline element might be a single word. It will always be positioned between the words around it. It does not require a new line to exist. It will always flow with the text.

> Block-level elements take the width of the container element, and always start on a new line. Unless otherwise specified, they take up the full width of their parent element. A good example of a block-level element might be a paragraph or an image.

> In some cases it is useful to have an element that behaves as an inline element but may also have width and height. These are known as inline-block elements.

                            div {
                                  display: block;

                         }

# `<div> and <span>`

The HTML `<div> and <span>` elements are two elements that we have not yet discussed. "div" is a commonly accepted abbreviation of `"division" , while "span" simply means "from end to end".` In contrast to other HTML tags such as headlines, articles, and sections, these tags have no inherent semantic value. This means they are primarily to be used for presentational markup.

# The CSS Box Model

## Here are the elements that may be controlled using the CSS Box Model

- Position: where the element sits on the page, and if it is positioned relatively to other elements

- Width: the element's width

- Height: the element's height, either as relative or absolute values

- Margin: the element's outside margins in relation to other objects

- Padding: the space between the object's content and its border

- Border: the thickness, style, and color of the element's border

# Validating Markup and Chrome DevTools

## Typical validation problems

- Missing <!DOCTYPE> tag
- Missing or incorrect character encoding
- Incomplete or malformed element tag
- Improperly structured element
- Missing critical tags

# Adding comments to your HTML and CSS

            <!--<p>Content</p>-->
            For CSS elements you comment your code as follows:
                        /*
                          p {
                             color: #4a4a4a;
                             }
                        */

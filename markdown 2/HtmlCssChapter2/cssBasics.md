# CSS Selectors

## The ID Selector

- The ID selector is meant to identify a single, unique element in a document; there should never be more than one instance of a specific ID in any HTML document. IDs become especially important when we work with JavaScript as it will alllow us to target specific elements on the page.

        `<p id="uniqueID">Paragraph</p>

                #uniqueID {
                color: red;
                font-weight: bold
                }

        <a href="#uniqueID">Link</a>

        `
        You will notice that in both cases for CSS styling and links, the hashtag (#) element is used to identify the ID.

# The Class Selector

`<p class="myClass">Paragraph</p>`

    .myClass {
        color: green;
        font-size: 18px;
    }

# Pseudo-classes

    a:link { }

    This specifies an HTML link. While most browser-based default CSS styling provides a standard appearance for HTML <a> links, this is not always the desired one.

    a:visited { }

    This specifies the appearance of a link that has already been visited. Again, most browsers supply a default appearance, this allows us to override it.

    a:hover { }

    This represents the state when the user moves the cursor over a given element.

    a:active { }

    This represents the state when the mouse button is depressed. Note that this is only true when the mouse button is down, and is no longer true once the mouse is released.

    # CSS pseudo-elements

    The syntax for pseudo-elements is the same as that of pseudo-classes. For CSS3, the correct syntax is a double colon, as follows:

    p::first-letter { }

    p::first-line { }

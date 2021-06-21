# HTML Structure, Nesting, & Semantic HTML

- Once you have written some HTML yourself, you will start to see how it actually works in practice and how conceptually simple it is. In terms of learning the language, a big advantage of HTML is that almost all of the elements have a very similar structure – an opening tag, attributes, content, and closing tag. As you will see, some elements do not have ”closing” tags (the <br> and the <img> tags are two examples) but for the most part these are exceptions.

        `<h1 id="headertext">Headline</h1>`

# Nestin

    `<html>
        <body>
           <h1>Headline</h1>
        </body>
    </html>`

-The most general example of this is the <html> element itself – it holds any other page elements, such as the `<head>and<body>` elements. The `<body>` element, in turn, may hold any number of elements as well – anything that will be displayed on the page. We will be coming back to this "nesting" concept as it is important to how HTML is structured and will also be important to understand once we start working with Javascript. Another way of referring to this "nesting" is using a parent/child terminology – the `<html>` tag is parent to the `<head> and <body> tags, and the <body>` tag is the parent to any tags between the `<body> and </body>` tags. We will be referring to this relationship (and more broadly, the ancestor relationship) in this and future modules.

# Semantic Meaning

- This concept of "parentage" also shows how HTML documents may be structured. An HTML document’s structure should have semantic meaning – that is, the way a document is structured should be part of the document's meaning.**think about a book**

// Semantic HTML means that the HTML tags should be used for their intended purpose, and that the content (the HTML) and how it is presented are kept separate.

# Absolute and relative file paths

- based on their relation to one another, understanding where relative and absolute file paths are best used is important.In this case you would have to use an absolute file path to link to this page
  because it has no direct relationship to your document. An absolute file path might look like this:

        ` <a href="http://www.widgets.com/laptops/2017/latest.html">link</a>`

- Notice that we are using a full HTTP query, and the full domain and subdomain, as well as the path to the document.

**To link to a document in a parent folder of the linking document, you would do the following:**

    ´<a href="./latest.html">link</a>´

**A double dot-slash identifies the parent directory, while a single-dot slash identifies the current directory::**

    ´<a href="../latest.html">link</a>´

**If you want to link to a document that is up two levels, simply repeat:**

    ´<a href="../../latest.html">link</a>´

# HTML Lists

- You may be wondering why we have included lists in a discussion about hyperlinks. While lists have many uses, they are also a handy way of containing navigational elements – that is, links – in a single entity.

- Lists come in two forms: ordered and unordered lists. In ordered lists, the order of elements is significant. The general rule for which list to use is that if you need to specify the order of your list elements, use an ordered list. Otherwise, use an unordered list.
  Lists consists of two elements:

> `The <ul> or <ol> element, and the <li> element. The <ul> and <ol> elements declare the list; each <li>` `element, which must be nested within the <ul> or <ol> element, specifies a list item. There can `be any `number of <li> elements within a list. You should notice that, regardless of whether you are` using an unordered or an ordered list, the structure remains the same.
> Here is an example of an unordered list:

    `<ul>
        <li>Birds</li>
        <li>Fish</li>
        <li>Reptiles</li>
    </ul>`

**result**

   <ul>
        <li>Birds</li>
        <li>Fish</li>
        <li>Reptiles</li>
    </ul>

# "Bugs", misspellings, syntax, and different types of errors

Wrongly formed or misspelled element:

    `<htnl>
        <body>
             <h1>Heading</h1>
             <p>Text here</p>
        </body>
    </html>`

- Malformed or incompletely formed element:
- Improperly closed element:
- Missing closing tag for element:

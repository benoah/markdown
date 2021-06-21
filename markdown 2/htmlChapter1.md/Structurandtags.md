# Structure and tags

> `<!DOCTYPE html>`
> ”Hey, I’m an HTML file, so you should interpret me like an HTML file!”.

## The Head

> The head of the document is used to contain metadata about the page, but isn't displayed on the page like the data inside the body. The metadata defined in the head might include: the page title, descriptions of the page, styles, scripts, viewports, links, and more.

## The Title Tag

`<title>Cat - Wikipedia</title> `

- The title tag sets the title of the document. You can see the title displayed on the browser tab. It is also the title that gets displayed on search engines, and so it is important to pick clear, unique titles for each page.

## The `<meta>` Tag

- The `<meta>` tag sits within the `<head>` tag. It's purpose is to contain information about the web page itself. This may include - among other things - a description of the page, the author of the page, as well as keyword attributes for support of searches and determining whether or not the page will be cached in a web browser.

### The syntax for the meta element is as follows:

> `<meta name="description" content="The domestic cat is a small, typically furry, carnivorous mammal. They are often called house cats when kept as indoor pets or simply cats when there is no need..."> `

> `<meta name="keywords" content="Cats, pets, kittens, animals"> `

Another useful attribute is the charset attribute – this tells the browser what character set should be used for the page. The UTF-8 character set has a wider range of characters than the standard ASCII character set, which only had 127 supported characters. UTF-8 supports 256 characters, and has many of the commonly occuring characters and glyphs. UTF-8 has become the dominant character set on the web, accounting for up to 90% of websites.

`<meta charset="utf-8"/>`

# Structure and tags - The Body

**Everything visible on the page should go inside the body tag. The head is for all the extra information and styling for the page, but the HTML content that will be displayed on the page must be inside the body.
It's important to notice how elements are nested inside other tags in HTML. This is a fundamental concept of HTML. For example, a div tag is nested inside the body tag which is nested inside an HTML tag. Note below how nested elements are indented. This makes the code more easy to read.**

> `<html>`

> `<head>`

> `</head>`

> `<body>` > `<div>` > `Content` > `</div>`

> `</body>`

> `</html>`

# Semantic Elements and Document Structure

> The `main, section, article, aside, nav, header, and footer` elemets are all semantic HTML elements and, if used properly, will help you build robust, structured content that is available to everyone.

The `<main>` element - as its name implies - defines the main content of a given document. It should not include any elements that are NOT unique to the site, such as navigation, site logos, copyright information, and so forth:

`<main>`

`<h1>Headline</h1>`

`<p>Paragraph</p>`

`</main>`

The <section> element defines a block of HTML code that may be viewed as a section of a document. This is deliberately vague, as a section may be defined in a number of ways. Sections can represent chapters of a document, but also elements such as headers and footers:

`<section> `

`<h1>Headline</h1>`

` <p>Paragraph</p>`

`</section> `

The `<article>` element defines a block of HTML. As the name suggests, an article element should act as self-contained content which may stand on its own. This may include blog posts, news articles, editorials, etc. Like the section tag, the article element is rather vaguely defined as it may be employed in so many different ways. But the rule of thumb is a piece of unique content that may stand on its own.

The `<aside>` element is the equivalent of a sidebar in a magazine or newspaper. It contains information that is related to the element it is placed in:
`<aside> `

`<h1>Headline</h1>`

` <p>Paragraph</p>`

`</aside> `

The `<nav>` element is specifically used to hold the primary navigation elements of an HTML document.
`<nav><ul><li>Menu 1</li><li>Menu 2<li></ul></nav> `

`code`

<!-- link  -->

    ´<header>
    <h1>Heading 1</h1>
        <nav>
        <nav>
    </header>
    ´

The `<footer>` element may act as a footer for either a section or an entire HTML document. It may contain authorship and copyright information, as well as possible contact information and/or a sitemap.

<!-- link  -->

`code`

<!-- link  -->

    ´<footer>
    <p>Copyright &copy; 2017</p>
    </footer>
    ´

    `code`

<!-- link  -->

    ´<!DOCTYPE html>
    <html>
    <head>
    </head>
    <body>
        <main>
    <h1>This is a page about indenting.</h1>
    <p>It's easier to read when child items are indented to the right of their parent.</p>
        </main>
      </body>
        </html>

´

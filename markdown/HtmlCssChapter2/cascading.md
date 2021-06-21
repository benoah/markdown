# Inheritance, cascading, and how CSS is implemented

Let's start with a very simple example – we have already looked at examples of nested tags. Inside our `<body> tag we have some text, wrapped in a simple <p> tag. As you can see, the <p>` tag is nested inside the body tag:

     <body>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
    </body>

    We can choose to style the paragraph tag by using the p selector, like this:

                  p {
                    font-family: Helvetica, Arial, sans-serif;
                    }

                    h1 {
                    font-family: Helvetica, Arial, sans-serif;
                    }
                    h2 {
                    font-family: Helvetica, Arial, sans-serif;
                    }
                    h3 {
                    font-family: Helvetica, Arial, sans-serif;
                    }

                    body {
                    font-family: Helvetica, Arial, sans-serif;
                    }

                    h1 {
                    font-family: Times Roman, serif;
                    }

# Inheritance, cascading, and how CSS is implemented cont.

                    body {
                    font-family: serif;
                    }

                    ul li a{
                    font-family: sans-serif;
                    }

# Calculating specificity

In some cases you encounter a problem where a style you create does not apply. It’s good to understand how CSS style specificity is calculated so you can address this kind of issue.

- Inline style: 1000
- ID: 100
- Class, attribute, pseudo-class: 10
- Type Selector:1

# Styling images with CSS

## While we have primarily been focusing on styling other HTML elements, we may also use CSS to style images. This has a number of advantages, not in the least that using CSS means the images may be styled more easily.

# Width and Height

**For image widths you can choose between percentage and pixels. Using a percentage allows the image to scale depending on the size it is being viewed in. If you write "width: 400" it will be interpreted as 400 pixels and will be that wide regardless of where it is viewed. This will throw out your layout on mobile.**

- It's worth noting that in HTML5 height can only be defined in pixels. More often than not, you will use width and define it using a percentage and set height to auto.

                 img {
                width: 100%;
                height: auto;
                }

- Max-width allows you to set the maximum width you will allow an image (or div) to be. If you set "max-width: 700" it will keep the image at 700 pixels until the screen is smaller than 700 pixels and then it will scale down.

- If you use standard image sizes around your site, it might be worthwhile creating special classes for those sizes.

# Align to center

You can also center align an image by making it a block-level item with "display: block" and then setting the margin on the left and right to "auto".

# Background-image

             <!DOCTYPE html>
                    <html>
                    <head>
                    <style>
                    body {
                        background-image: url("van.png");
                        background-repeat: no-repeat;
                    }

                    div {
                        background-color: #eeeeee;
                        width: 500px;
                    }

                    </style>
                    </head>
                    <body>
                        <main>
                            <h1>Welcome to Van World</h1>
                        <p>We have the best deals on vans.</p>
                        </main>
                    </body>
                    </html>

# Styling images with CSS cont

## Styling images with CSS cont

## Opacity

- You can change the opacity of an image. The values can range from 0 to 1, with 0 being completely invisible and 1 being fully visible. It's often used in a pseudo class for a hover state, so that when a client is browsing the image will change on hover.

                img:hover{
                    opacity: 0.7;
                }

# Rounded Images

                    img {
                        border-radius: 50%;
                    }

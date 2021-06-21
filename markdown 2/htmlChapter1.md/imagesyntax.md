# Image Syntax

The image element is unique in that it has a number of particular attributes for image properties, as well as the fact that it is another HTML element that has no closing tag. The image element includes a src tag which identifies the source, or location of the image. This src tag is effectively a URL, and should be formatted as such.

If the image is on the same hard drive as the HTML page, a relative file path may be used. If not (for example, if the image is on an external website) an absolute file path may have to be used. Understanding the difference between absolute and relative paths is important. You would not use an absolute path to a file on your own computer, as this will ONLY work on your computer, and not once you upload the webpage and associated link.

Image elements have a number of other attributes, including attributes for the width and height of the image, as well as an alt tag. The alt attribute is specific to images, as it acts as a description of the images if the image cannot be downloaded or viewed. This is especially important for people with disabilities, so make sure this text provides a good description of what the image is!

Image dimensions are, as a default, in pixel values. For width and height, the image tag does not necessarily treat images proportionally. You can put in different values (other than the actual image width and height) and see how, based on the settings of the width and height attributes, images do not have to be proportional. However, if you include only one size attribute (that is, either width or height) in the image attribute, the other dimension will automatically keep the image in proportion.
Here is the syntax for an image element with a relative file path:@

> Here is the syntax for an image element with a relative file path:

`<img src="image.gif" width="544"height="250" alt="catimage"/> `

> Here is the syntax for an image element with an absolute file path:

`<img src="http://www.wikipedia.com/images/image.gif" width="544" height="250" alt="cat image"/> `

> For images that are purely decorative, the alt property may remain empty:
> `<img src="image.gif" width="544" height="250" alt=""/> `

> If you need to include a longer description of an image, you may use the longdesc property, which takes the form of an external link (a link to another HTML document):
> `<img src="image.gif" width="544" height="250" alt="cat image" longdesc="about-cats.html"/> `

> or an internal link (a link to an HTML element on the same page):
> `<img src="image.gif" width="544" height="250" alt="cat image" longdesc="#aboutCats"/> `

# jpg

### The first kind of compression is JPG, or sometimes referred to as JPEG. JPEG is an acronym that stands for Joint Photographers Expert Group. Given the name, it would probably not surprise you that JPEG compression is most effective on photographic images! Many image editing programs allow for JPEG compression, where the amount of compression may be set. The greater the compression, the smaller the file size of the image, but the quality of the image will also be lower. Applications like Photoshop allow you to determine the exact amount of image compression you need to apply to achieve a given file size.

## we have also

- Graphics Interchange Format (GIF) Image Compression
- Non-photographic images with JPEG and GIF compression
- PNG: Portable Network Graphics

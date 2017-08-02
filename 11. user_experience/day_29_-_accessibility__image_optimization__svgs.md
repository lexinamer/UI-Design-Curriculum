---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE5NCwiY29udGVudF90eXBlIjoiTGVzc29uIn0.lnqxtLLoF3B7ZxMUz5ebLZqLubsifxduq4vUsOKxVYk

title: >-
  Day 29 - Accessibility, Image Optimization, SVGs
description: >-
  Covers a variety of techniques for making websites accessible
---
## Accessibility
- ARIA
    + accessible rich internet applications
    + with interactivity on websites, there is no way of describing what is happening to a screen reader
    + enables developers to describe widgets in more detail
    + 3 attributes
        * roles
            - describe widgets not available in html 4
                + sliders, menu bars, tabs, and dialogs.
        * states
            - describe the current interaction state of an element, informing the assistive technology if it is busy, disabled, selected, or hidden
        * properties
            - describe characteristics of widgets, such as if they are draggable, have a required element, or have a popup associated with them
    + https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Web_applications_and_ARIA_FAQ
    + http://www.standardista.com/standards/wai-aria-accessible-rich-internet-applications-basics/
    + http://heydonworks.com/practical_aria_examples/
- Optimizing images for the web
    + Eliminate unnecessary images, leverage CSS where possible, use web fonts instead of encoded text images
        * is the image necessary?
        * is there another means to create the image 
            - CSS gradients
            - CSS can create a lot of the same effects with a fraction of the byte size
            - Web fonts are significantly more usable and smaller than images
    + Make sure you are using the proper format for the type of image
        * vector - zoom and resolution independent
            - use lines, points, and polygons to represent an image.
        * raster - should be used for complex scenes with lots of details
            - represent an image by encoding the individual values of each pixel within a rectangular grid.
            - you may need to save multiple versions of a raster image at various resolutions to deliver the optimal experience to your users (depending on screen resolution)
    + Optimizing for High Resolution Screens
        * HRS's have multiple device pixels per CSS pixel
        * HR images require more pixels, and more bytes
        * Image optimization techniques are the same regardless of resolution
        * Vector images are best for high resolution, but because raster images incode information per pixel, more pixels means more bytes
        * When you double the resolution of a screen, the total pixels doubles by 4
        * use vector images whenever possible
    + SVG 
        * Scalable Vector Graphics
        * XML based image format
        * Can embed SVG directly into the page, or as an external resource
        * SVG files hold a lot of information, so it's a good idea to minify them before using (https://github.com/svg/svgo) and GZIP compression
            - gzip can reduce the size of a file up to 70%
        * not all browsers support svg (must use png fallback/div fallback)
        * three ways to embed
            - img
                + need png fallback
            - code
                + need div fallback
            - object
                + can't use external stylesheets
    + Raster Optimization
        * each pixel holds a different rgba value
        * 256 shades per channel (red, green, blue, alpha)
        * if we know the dimensions of the grid, we can calculate the size (4bytes/px)
        * How to Optimize
            - Reduce bit depth (less than 256/pixel)
            - 50% compression if you reduce it to a total of 256 colors (8 bits) instead of 2563
            - Delta encoding - instead of storing individual pixel colors, it stores the difference between neighboring pixels.  If delta encoding is 0, you only have to store 1 bit for both pixels
                + can look at just immediate neighbors, or also larger chunks of pixels
    + Lossless vs Lossy images
        * Due to how the eye works, we can present a "representation" of an image (get rid of some information we don't see)
        * Lossy - a filter is applied that gets rid of some data
        * Lossless - pixel data is compressed
    + Scaled image assets
        * serve different images based on the browser size, don't rely on the browser to resize images
        * even 10px too large of an image can cost 2100px total
Examples:
https://github.com/TIY-ATX-UI-Design/Examples/tree/master/04-07-2016/svg-example

Resources:
- [Color Blindness Check (website)](http://colorfilter.wickline.org/)
- [Color Contrast Check](http://webaim.org/resources/contrastchecker/)
- [Photoshop Accessibility](http://www.adobe.com/accessibility/products/photoshop.html)
- [Web Accessibility with Google](https://webaccessibility.withgoogle.com/unit?unit=1)
- [ARIA Labels](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Web_applications_and_ARIA_FAQ)
- [Web Page Test](http://www.webpagetest.org/)

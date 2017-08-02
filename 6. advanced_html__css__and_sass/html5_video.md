---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE3NywiY29udGVudF90eXBlIjoiTGVzc29uIn0.yp-aKPFzldoXGliVet62h4IncHHq2EaKuD8ELP5hFZM

title: >-
  HTML5 Video
description: >-
  HTML5 video
---

# HTML5 Video
HTML5 video refers to a new HTML element `<video>` that was added to HTML5. Browsers that support the HTML5 `<video>` element can play video files natively, while previously they would have required a plugin like Flash to play video content.

### Example Code
``` html
<video poster="path/to/screenshot.jpg">
	<source src="path/to/video.webm" type="video/webm">
	<source src="path/to/video.ogg" type="video/ogg">
	<source src="path/to/video.mp4" type="video/mp4">
</video>
```
Note: to improve performance, you should always include the type attribute on your `<source>` elements. This allows the browser decide which file to use without first loading each file.

### Why do I need multiple formats for HTML5 video?
The HTML5 `<video>` element does not require multiple video formats, however different browsers (and browser versions) support different video container formats and codecs, so for maximum cross-compatibility we add multiple file formats in their own `<source>` elements as children of the `<video>` element.

### What are the best video formats for HTML5 video
For maximum browser compatibility you should include three formats in your HTML5 `<video>` elements:
- Webm: Webm (with VP8 video codec and Vorbis audio codec) is the preferred format for Chrome, Opera and Firefox 4+ as it provides the best compression to quality ratio of the available formats.
- Ogg: Ogg (with Theora video codec and Vorbis audio codec) is also fully supported in Chrome but has even earlier support in Firefox (supported since v3.5).
- Mp4: Mp4 (with H.264 video codec and AAC audio codec) is supported by most other browsers. Including the Mp4 format adds support for Internet Explorer 9+, Safari, iOS Safari, Android Browser, Opera and Chrome for Android.

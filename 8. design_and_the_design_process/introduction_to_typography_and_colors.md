---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE2OSwiY29udGVudF90eXBlIjoiTGVzc29uIn0.VhUWpEIGrxTdDQnzv4qflEJo2M5EsKbZvfTm3qBZ5_o

title: >-
  Introduction to Typography and Colors
description: >-
  Intro to all things typography and colors
---
# Typography
Typography in web design can strongly affect how people react to a project. Thoughtfully choosing the right font allows you to evoke a particular emotion or fit a certain style. The skillful use of typography commands the attention of your desired audience, communicates a key idea and motivates them to take action. Typography is not just about legibility. It is a blending of art and science and can serve a functional purpose. 

https://vtldesign.com/brand-development/graphic-design/importance-typography-part-1-fonts-speak-louder-words/

### History of Typography
- https://www.youtube.com/watch?v=wOgIkxAfJsk
- https://vimeo.com/69375692

### Anatomy of Typography 
![anatomy of type](http://www.designersinsights.com/wp-content/uploads/2012/03/Anatomy-of-Typography.png)


### Type and Styles
- Type: the design of the alphabet--the shape of the letters that make up the typestyle. 
- Font: the file that contains/describes the entire typeface.

#### Type Styles
- oldstyle (thick, i.e. NYT), 
- modern (slim), 
- slab serif (just serif), 
- sans serif (more modern than serif, but usually thicker than modern), 
- script (for themes, not as readable)
decorative (even more for themes, use sparingly)

### Typography on the web
Px, em and rem are all units of length used to define the size of elements on a webpage. You can use them across the board on divs, margins, padding, and so on, but in this article we’re going to concentrate on the sizing of type.
- **px:** pixels are the same size regardless of the size of anything else. In practice, they aren’t the same length everywhere because different devices treat them differently, but on each device a pixel is always the same. 16px on your laptop monitor is not the same as 16px on your iPad. Pixels are absolute but not consistent.
- **em:** Ems are a relative measure of length. The size of an em is relative to the font-size of its parent element. If you have a `<div>` with the font size is set to 16px, and a `<p>` element inside that div with a font-size set to 2em, the font-size of text in the `<p>` will be 32px.
- **rems:** Ems have a problem. Because everything is sized relative to its parent element, the meaning of an em changes as elements are nested. Rems, root ems, are always relative to the font-size of the `<html>` element. It doesn’t matter how deeply nested an element is, its rem lengths will always be a proportion of the font-size of `<html>.`

### Web fonts vs non Web fonts
- Fontawesome.io
- Google Fonts
- Typekit
- What the font?

<br>
# Color and Color Psychology
The use of color can dramatically affect moods, feelings, and emotions. It is a powerful communication tool and can be used to signal action, influence mood, and cause physiological reactions, which becomes especially important in design. 

### Color Theory 
- CMYK (Print Design) and RGB (Web Design)
- Tint (adding white) v. shades (adding black)
- Types of color relationship
    + Complementary
    + Triads
    + Analogous 
    + Monochromatic
    + Compound

<img src="http://www.motocms.com/blog/wp-content/uploads/2014/08/color-theory-infographic-paper-leaf.jpg" width="100%;">

### Hex Colors
A hex color is a six-digit hexadecimal number used in HTML, CSS, SVG, and other computing applications, to represent colors. The number represents the red, green and blue components of the color. One byte represents a number in the range 00 (none) to FF (full) in hexadecimal notation, or 0 (none) to 255 (full) in decimal notation.

![hex colors](https://www.smashingmagazine.com/wp-content/uploads/2012/09/hex-additive-and-subtractive.png)

### Color Moods
While perceptions of color are somewhat subjective, there are some color effects that have universal meaning. Colors in the red area of the color spectrum are known as warm colors and include red, orange and yellow.

These warm colors evoke emotions ranging from feelings of warmth and comfort to feelings of anger and hostility.

Colors on the blue side of the spectrum are known as cool colors and include blue, purple and green. These colors are often described as calm, but can also call to mind feelings of sadness or indifference.

![color](http://www.pamorama.net/corepam/wp-content/uploads/2013/04/guide-to-color-emotions.gif)

<br>
# In Class Exercise:
Using Google Fonts, create Codepens with an h1,h2,h3,and p using typographic and color principles based on one of the following themes
- Retro and Fun
- Rustic and Nostalgic
- Modern and Bold
- Minimalist and Classic

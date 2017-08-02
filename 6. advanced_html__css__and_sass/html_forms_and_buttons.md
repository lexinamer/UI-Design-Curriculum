---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE2NiwiY29udGVudF90eXBlIjoiTGVzc29uIn0.6UFhVEMwlOK-F9u-ndF12VoGgoA0rHjRSUrwGBZIkpo

title: >-
  HTML Forms and Buttons
description: >-
  Learning to create buttons and forms using HTML
---
## What is an HTML form?
HTML forms allow users to send data to the web site. Most of the time that data is sent to the web server, but the web page can also intercept it to use it on its own. Examples are surveys, account creation forms, contact forms, and order forms. 

An HTML Form is made of one or more widgets, which can be text fields (single line or multiline), select boxes, buttons, checkboxes, or radio buttons. Most of the time those widgets are paired with a label that describes their purpose.

## How to build a form
Use the `<form>` element as the container for your form, similar to how you create a list
```html
<form>
all form information goes here
</form>
```

Now you add widgets of your form using the `<input>` and `<label>` and `<textarea>` elements. There are many different types of input elements that you can choose from with the most common being text, checkbox, and radio.

HTML5 has brought a lot of different input types, which you can see a list [here](http://cdn.sixrevisions.com/demos/0345-new_html5_form_input_types/new-html5-form-input-types.html?)
 
```html
    <label for="name">Name:</label>
    <input type="text" id="name" name="user_name" />

    <label for="email">E-mail:</label>
    <input type="email" id="email" name="user_email" />

    <label for="message">Message:</label>
    <textarea id="message" name="user_message"></textarea>
```

You should always use the `for` because input fields without accompanying labels can lead to accessibility issues for those who rely on screen readers. If a screen reader comes across an input field without a label it will try to find some accompanying text to use as the label.

Finally, we add a `<button>` to submit the form.
```html
<button type="submit">Send</button>
```

The form will look like this with no styling that can be styled using CSS as normal.  
<iframe height='346' scrolling='no' src='//codepen.io/lexinamer/embed/yajKgN/?height=346&theme-id=0&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/lexinamer/pen/yajKgN/'>Form Example</a> by Lexi Namer (<a href='http://codepen.io/lexinamer'>@lexinamer</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

<br>This is a purely visual form that currently has no functionality. We would need to add a few more things and give the form some logic in order for it to work. This is usually accomplished using Javascript or PHP which we will get to later in the course. 

There are MANY more things you can do with forms, including [dropdowns](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select). 

[Mozilla HTML Form Guides](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms)
<br>

## A note on buttons
As we saw in the form, buttons can be achieved in HTML using the `<button>` element but can be more easily created in some cases (for example in menus) by styling the `<li>` tag to look like a button.

<iframe height='226' scrolling='no' src='//codepen.io/lexinamer/embed/ORkvzq/?height=226&theme-id=0&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/lexinamer/pen/ORkvzq/'>Simple Buttons</a> by Lexi Namer (<a href='http://codepen.io/lexinamer'>@lexinamer</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe> 

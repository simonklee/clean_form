# clean_form

A customizable and maintainable HTML form styled with CSS using
[less.js](https://github.com/cloudhead/less.js/).

## Features

 * Uses the least amount of HTML and CSS necessary to produce a form that is
   styled properly
 * No creativity or hacks
 * Fields that receive text are styled with a thin border
 * Buttons render natively on all platforms
 * `form > ul > li` HTML structure
 * Validates as HTML5

## Setup

1. Copy `clean_form.less` to your website directory.

2. Define form classes in a separate `less`-file. You can define these classes
   in `clean_form.less`, but keeping them in a separate file makes upgrades of
   clean_form a whole lot easier.

   `<form class="foo">` uses the default settings.

        form.foo {
            .clean_form;
        }

   `<form class="bar">` uses the default settings, but they are passed as
   arguments to `.clean_form`. Copy and paste the code below if you want to
   customize your form.

        form.bar {
            .clean_form(
                512px,      // form width
                256px,      // left side of form width
                256px,      // right side of form width
                #dfdfdf,    // field border-color
                1px,        // field border-size
                24px,       // field height
                24px,       // field margin-bottom
                96px,       // multiple select height
                192px);     // textarea height
        }

   `<form class="baz">` uses the default settings, except for the widths.

        form.baz {
            .clean_form(
                1024px,     // form width
                512px,      // left side of form width
                512px);     // right side of form width
        }

3. Compile your `less`-file.

4. Modify the structure of your HTML forms so that they match the one in
   `test.html`. Add the class attribute to the form elements with the class
   names that you’ve defined.

5. You probably also want to set the typography for all the form elements.

        body, input, select, textarea {
            font: 16px/1.5 sans-serif;
        }

## License

Copyright © 2010–2011, Alexander Teinum <ateinum@gmail.com>

Permission to use, copy, modify, and/or distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED “AS IS” AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH
REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND
FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT,
INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS
OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF
THIS SOFTWARE.

# clean_form

A customizable and maintainable HTML form styled with CSS using
[less.js](https://github.com/cloudhead/less.js/).

## Features

 * Easy to use
 * Looks great
 * No creativity or hacks
 * Fields that receive text are styled with a thin border
 * Buttons render natively on all platforms
 * `form > ul > li` HTML structure
 * Validates as HTML5

## Compatibility

 * All modern browsers
 * Internet Explorer 7 optionally
 * [Eric Meyer Reset](http://meyerweb.com/)

## Setup

1. Copy `clean_form.less` to your website directory.

2. Define form classes in a separate `less`-file, as it makes it easier to
   upgrade `clean_form.less`. Before you define anything, import
   `clean_form.less`.

        @import url('clean_form.less');

   This is the definition of a form using the default settings.

        form.foo {
            .clean_form;
        }

   However, you might want to define a customized form.

        form.bar {
            .clean_form(
                512px,      // form_width
                256px,      // form_left_width
                256px,      // form_right_width
                24px,       // li_margin_bottom
                16px,       // gutter_width
                #dfdfdf,    // input_border_color
                1px,        // input_border_size
                24px,       // input_height
                192px,      // textarea_height
                96px);      // select_multiple_height
        }

   It’s possible to set as many arguments that you like and use the default
   settings for the remaining arguments.

        form.baz {
            .clean_form(
                1024px,     // form_width
                512px,      // form_left_width
                512px);     // form_right_width
        }

3. Compile your `less`-file.

4. Modify the structure of your HTML forms so that they match the one in
   `test.html`.

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

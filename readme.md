# clean_form

A flexible [less.js](https://github.com/cloudhead/less.js/) mixin for styling two column HTML forms.


## Features

 * No hacks or creativity
 * Fields that receive text are styled with a thin border
 * Buttons render natively on all platforms
 * Left and right aligned labels are supported
 * Internet Explorer 7 support is optional
 * Compatible with [Eric Meyer Reset](http://meyerweb.com/)
 * Test validates as HTML5

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
                left,       // label_align
                512px,      // form_width
                256px,      // form_left_width
                256px,      // form_right_width
                16px,       // gutter_width
                16px,       // element_margin_bottom
                #dfdfdf,    // element_border_color
                1px,        // element_border_size
                24px,       // element_height
                192px,      // textarea_height
                96px);      // select_multiple_height
        }

   It’s possible to set as many arguments that you like and use the default
   settings for the remaining arguments.

        form.baz {
            .clean_form(
                left,       // label_align
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

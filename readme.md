# clean_form

Styles the most common HTML controls using less.js.

## Setup

1. Copy `clean_form.less` to your website directory.

2. Define as many form configurations as you need in a separate `less`-file.

        @import url('clean_form.less');

        form#foo {
            .clean_form;
        }

        form.bar {
            @cf_label_align:            left;
            @cf_form_width:             512px;
            @cf_form_left_width:        256px;
            @cf_form_right_width:       256px;
            @cf_gutter_width:           16px;
            @cf_element_margin_bottom:  16px;
            @cf_element_border_color:   #bfbfbf;
            @cf_element_border_size:    1px;
            @cf_element_height:         24px;
            @cf_textarea_height:        192px;
            @cf_select_multiple_height: 96px;

            .clean_form;
        }

        form.baz {
            @cf_label_align:            right;

            .clean_form;
        }

3. Compile your `less`-file. E.g. `lessc test.less test.css`.

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
